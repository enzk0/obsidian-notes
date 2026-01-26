
***Highlight changes and send new paper to Sir***
### Chapter 1 Changes
---
- statement of the problem, as there is no **bridge** between statement of the problem and general objectives
	- clearly state what is the **gap**
	- there is no **specific problem getting addressed**
	- based on literature, rddlgn has only been tested on machine translation but not yet on formal languages
	- answer the question? **why formal languages** (reason this out)
	- say that we can't find any other existing 

- objectives goals:
	- implement rddlgn
	- separate rddlgn evaluation, and rddlgn evaluation with other architectures
	- state the metrics for both evaluations
	- "this is the metrics we used because that this is the gold standard in evaluating AI"

- objectives specifications:
	1. remove **optimize**, this implies a baseline performance between the original model and new model
	2. remove **gather data**, indicate how to pre-process data; if no data pre-processing needed, we can exclude this objective
	3. train rddlgn and evaluate rddlgn alone, both based on data prepared, with respective metrics
	4. compare and evaluate rddlgn with others RNN architectures with given similar inputs, with the respective metrics too
		- metrics: generalizability, accuracy (expressivity and inductive bias), computational

- research questions, should be inline with the objectives
	1. how do we implement RDDLGN? (solve in chap 3)
	2. how do we pre-process the Flare? (solve in chap 3)
	3. how well does it do alone given Flare input after training? (solve in chap 4)
	4. how does it fare compared to other RNN architectures with given similar inputs? (solve in chap 4)

- conceptual framework, sums up the flow, tells the reader the flow
	- **the flow:** flare -> pre-process flare for rddlgn -> evaluate rddlgn -> input similar data to other architectures -> and evaluate
	- remove **data gathering**

- scope and limitation, should not be written like RRL, should be a narration
	- should contain two things: what we will do, and what we will not do
		- like it should reflect the data, the models, and the boundaries
		- it should not mention data collection, strictly state that FLARE will be used
		- should clarify...
		- remove unnecessary (fpgas, chuchu, nvidia platforming)
		- specify metrics of evaluation
		- mention compute limits (certain pc with hardware)

- for Flare that needs to be stated,
	- needs to be fed into a process library
		- epoch, learning rate, size
	- we have to modify a bit?

### For Chapter 2
---
studies to strengthen the conceptual framework

- comment is we somehow teach AI
- modify so that it should only show works related to the topic

### For Chapter 3
---
- no data collection

- for research design, should reflect conceptual framework

- subsection 3.2 libraries and framework as implementation

- 3.3 Data Preparation should the preprocessing

- find papers that formal languages can justify the specific epoch, batch size

- make rddlgn model evaluation

- make rddlgn model comparison towards other models