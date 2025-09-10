
---

#### What is Aeroflex Quick Calculation App?
- It is a mobile app created by Aeroflex.
	- Aeroflex creates EPDM Insulators
- The quick calculation app is made for engineers, contractors and HVAC designers.
- Its features are calculating the right insulation thickness for pipes, ducts, and tanks.
	- Mainly to prevent condensation and reduce heat loss/gain.
	- The app provides graphs and charts to see calculations and estimations.
	- User's can edit certain fields for calculation
	- User's can export a pdf in respect to the calculations, generating a report.

#### What is the picture all about?
- I think that it contains the specified inputs, the calculated results or outputs, and the calculation/mathematical formulas that will be used
- It is for like a calculation tool for insulation.


> [!NOTE] Some Terms
> 1. **HVAC**; stands for Heating, Ventilation, and Air Conditioning
> 	- Considered as a system designed to control indoor environmental conditions like temp, humidity, air quality, air movement, etc.
> 2. **EPDM**; stands for Ethylene Propylene Diene Monomer
> 	- A synthetic rubber that is used in the construction industry. Insulators, roofing, waterproofing, sealing, and etc.



### Inputs (by module)

**A) *Condensation control (pipes/ducts)***
- **System type:** pipe (copper/steel/PVC), duct (rectangular/round).
- **Size:** nominal pipe size & schedule/OD; or duct WxH/diameter & length.
- **Medium & temp:** chilled water/refrigerant; operating fluid temp (°C).
- **Ambient:** dry-bulb (°C), relative humidity (%) (to prevent condensation).
- **Air movement:** still/ventilated; air velocity near surface (optional).
- **Surface/jacket emissivity:** bare elastomeric vs. cladded (optional).
- **Insulation product:** grade (EPDM), available thickness steps.
- **Thermal conductivity (k):** curve at mean temp (built-in library).
- **Vapor permeability** (for notes; elastomeric is a built-in vapor retarder).  
    _(These mirror Aeroflex’s own guidance on condensation thickness inputs.)_

**B) *Heat loss/heat gain / R-value***
- **Thickness** (by multiple), k-value at mean temperature.
- **Inner/outer temps**, convection coefficients or presets.
- **Length/area** for total W or kWh impact.  
    _(Aeroflex publishes simple R = thickness / k guidance for flat surfaces.)_

**C) *Tanks/Vessels (optional)***
- **Geometry:** cylinder (D×L) or rectangle (L×W×H).
- **Surface temp target** or heat-flow target.
- **Ambient & operating temps, RH**.

---
### Outputs
- **Required insulation thickness** (nearest available size) to prevent condensation.
- **Surface temperature** at selected thickness & dew-point margin (°C).
- **Heat loss/heat gain** (W per m or per m²; for total entered run/area).
- **R-value** by selected thickness at mean temp (by module).
- **BOM/Material list**: number of tubes/box by ID/thickness or sheet m² (cutting allowance), plus recommended adhesive/tape/accessories.
- **Notes/assumptions**: k-value reference temp, ambient assumptions, safety factor, product data links.
- **Export**: PDF/PNG, CSV for BOM.

---
### Calculation logic (essentials)
- **Dew point** from ambient DBT & RH (Magnus/Tetens).
- **Radial conduction** through cylindrical layers; external convection & radiation; iterate thickness until surface T > dewpoint.
- **Mean temperature** for k (T_in + T_out)/2; actual Aeroflex EPDM k(T) from internal table. _(Aeroflex tech guidance uses this reference mean temp (by thickness))._
- **Flat surfaces**: R = thickness/k (empirical or SI).
- **Note**: R-values from k via NIA MIDG or by conduction calculator for validation.