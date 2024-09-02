# CS854-Fall24: Advanced Topics in Computer Systems --- Model Serving Systems for GenAI

## Administrivia
* Lectures: DC2568, Friday: 1:30 PM – 4:20 PM

### Instructor
[Hong Zhang](https://hongzhangblaze.github.io/) 
Email: honzhang at uwaterloo dot ca
Office: DC3530 (office hours by appointment)

Presentation slides and paper summaries should be emailed to the email address above.

## Course Description
Generative AI (GenAI) applications are revolutionizing the world. The latest GenAI models such as GPT-4 have achieved unprecedented performance in various tasks such as code generation, text classification, and problem reasoning. However, serving GenAI applications, i.e., deploying trained GenAI models on a compute cluster and conducting model inference for incoming user requests, presents challenges in systems design. 

This seminar-based course will introduce you to the key concepts and the state-of-the-art in model serving systems for emerging Generative AI (GenAI) and encourage you to think about either building new tools or applying an existing one in your own research. The course will cover various important topics for serving systems for GenAI, including efficient batching, memory/cache management, request scheduling and load balancing, and compound AI systems such as Retrieval-Augmented Generation. Note that this course is **NOT focused on AI methods**. Instead, we will focus on how to build efficient serving systems for existing AI methods. 


### Prerequisites
Students are expected to have strong programming skills and have completed at least one undergraduate-level systems-related course, such as Operating Systems, Databases, Distributed Systems, or Computer Networks. While an undergraduate course in Machine Learning or Artificial Intelligence would be beneficial, it is not a requirement.

### Textbook and Exams
This course has **no** textbooks or exams.
We will read recent papers to understand trends and important topics in serving systems for GenAI.

## Tentative Schedule and Reading List
*This is an evolving list and the schedule is subject to changes.* 

| Date    | Readings                       | Presenter | Summary | Reviewer
| --------| -------------------------------| --------- | ------- | -------
| Sept 6  | **Introduction** | Hong
|         | [How to Read a Paper] (http://svr-sk818-web.cl.cam.ac.uk/keshav/papers/07/paper-reading.pdf) 
|         | [How to Give a Bad Talk] (http://www.cs.berkeley.edu/~pattrsn/talks/BadTalk.pdf) 
|         | [Writing Reviews for Systems Conferences] (http://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf)
|         | [LLM Inference Serving: Survey of Recent Advances and Opportunities] (https://arxiv.org/pdf/2407.12391)
|         | [Towards Efficient Generative Large Language Model Serving: A Survey from Algorithms to Systems] (https://arxiv.org/pdf/2312.15234)   
|         | [The Datacenter as a Computer] (https://link.springer.com/book/10.1007/978-3-031-01761-2) (Chapters 1 and 2, optional)
|         | [The Llama 3 Herd of Models] (https://arxiv.org/abs/2407.21783) (optional)
| Sept 13 | **Serving Systems for GenAI _vs._ traditional DNN** 
|         | [The Illustrated Transformer] (https://jalammar.github.io/illustrated-transformer/) (Required) | Xiaodian
|         | [The Illustrated GPT2] (https://jalammar.github.io/illustrated-gpt2/) (optional)
|         | [Attention is All You Need] (https://dl.acm.org/doi/10.5555/3295222.3295349) (optional)
|         | [Serving DNNs like Clockwork: Performance Predictability from the Bottom Up] (https://www.usenix.org/system/files/osdi20-gujarati.pdf) (Required) 
|         | [Orca: A Distributed Serving System for Transformer-Based Generative Models] (https://www.usenix.org/system/files/osdi22-yu.pdf) (Required) 
| Sep 20  | **Memory Management**
|         | [Efficient Memory Management for Large Language Model Serving with PagedAttention] (https://dl.acm.org/doi/10.1145/3600006.3613165) (Required)
|         | [vAttention: Dynamic Memory Management for Serving LLMs without PagedAttention] (https://arxiv.org/abs/2405.04437) (Required)
|         | [FlexGen: High-Throughput Generative Inference of Large Language Models with a Single GPU] (https://proceedings.mlr.press/v202/sheng23a.html) (Required) 
| Sep 27  | **Prefill _vs._ Decode**
|         | [Distserve: Disaggregating Prefill and Decoding for Goodput-optimized Large Language Model Serving](https://dl.acm.org/doi/10.1145/3600006.3613165) + [Splitwise: Efficient generative LLM inference using phase splitting] (https://arxiv.org/pdf/2311.18677) (Required)
|         | [SARATHI: Efficient LLM Inference by Piggybacking Decodes with Chunked Prefills] (https://arxiv.org/pdf/2308.16369) +  [Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://arxiv.org/pdf/2403.02310) (Required) 
|         | 
| Sep 27  | **Parallelism**
|         | [AlpaServe: Statistical Multiplexing with Model Parallelism for Deep Learning Serving] (https://www.usenix.org/system/files/osdi23-li-zhuohan.pdf) (Required)
|         | [Liger: Interleaving Intra- and Inter-Operator Parallelism for Distributed Large Model Inference] (https://dl.acm.org/doi/abs/10.1145/3627535.3638466) (Required)
|         | [LoongServe: Efficiently Serving Long-context Large Language Models with Elastic Sequence Parallelism (https://proceedings.mlr.press/v202/sheng23a.html(https://arxiv.org/pdf/2404.09526) (Required) 




(pipeline)



| Oct 15  | **Cache Management**
|         | [InfiniGen: Efficient Generative Inference of Large Language Models with Dynamic KV Cache Management](https://arxiv.org/pdf/2406.19707) (Required)
|         | [CacheGen: KV Cache Compression and Streaming for Fast Large Language Model Serving](https://arxiv.org/abs/2310.07240)(Required)
|         | [Cost-Efficient Large Language Model Serving for Multi-turn Conversations with CachedAttention] (https://arxiv.org/abs/2403.19708) (Required)
|         | [Infinite-LLM: Efficient LLM Service for Long Context with DistAttention and Distributed KVCache] (https://arxiv.org/abs/2401.02669) (Optional)
|         | [Stateful Large Language Model Serving with Pensieve] https://arxiv.org/pdf/2312.05516 (Optional)






| Sep  27 | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://openreview.net/forum?id=B1ckMDqlg) (Required)
|         | [Transformers are SSMs: Generalized Models and Efficient Algorithms Through Structured State Space Duality](https://openreview.net/forum?id=ztn8FCR1td) (Required)
|         | [DeepSeek-V2: A Strong, Economical, and Efficient Mixture-of-Experts Language Model](https://arxiv.org/abs/2405.04434)
| Sep 10  | **No Lecture: Work on Project Proposals**
|         | [Worse is Better](https://en.wikipedia.org/wiki/Worse_is_better) (Required)
| Sep 12  | **No Lecture: Work on Project Proposals**
|         | [Hints and Principles for Computer System Design](https://arxiv.org/abs/2011.02455) (Required)
|         | **Pre-Training**
| Sep 17  | [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://dl.acm.org/doi/10.1145/3458817.3476209) (Required)
|         | [Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://www.usenix.org/conference/osdi22/presentation/zheng-lianmin) 
|         | [Oobleck: Resilient Distributed Training of Large Models Using Pipeline Templates](https://dl.acm.org/doi/10.1145/3600006.3613152) (Required)
|         | [MegaScale: Scaling Large Language Model Training to More Than 10,000 GPUs](https://www.usenix.org/conference/nsdi24/presentation/jiang-ziheng)
| Sep 19  | [PyTorch FSDP: Experiences on Scaling Fully Sharded Data Parallel](https://dl.acm.org/doi/abs/10.14778/3611540.3611569) (Required)
|         | [RingAttention with Blockwise Transformers for Near-Infinite Context](https://openreview.net/forum?id=WsRHpHH4s0)
|         | [Tutel: Adaptive Mixture-of-Experts at Scale](https://proceedings.mlsys.org/paper_files/paper/2023/hash/5616d34cf8ff73942cfd5aa922842556-Abstract-mlsys2023.html) (Required)
| Sep 24  | [ZeRO-Infinity: Breaking the GPU Memory Wall for Extreme Scale Deep Learning](https://dl.acm.org/doi/10.1145/3458817.3476205) (Required)
|         | [Reducing Activation Recomputation in Large Transformer Models](https://proceedings.mlsys.org/paper_files/paper/2023/hash/80083951326cf5b35e5100260d64ed81-Abstract-mlsys2023.html) (Required)
|         | [GaLore: Memory-Efficient LLM Training by Gradient Low-Rank Projection](https://openreview.net/forum?id=hYHsrKDiX7)
| Sep 26  | [FastFlow: Accelerating Deep Learning Model Training with Smart Offloading of Input Data Pipeline](https://dl.acm.org/doi/abs/10.14778/3579075.3579083) (Required)
|         | [Rail-only: A Low-Cost High-Performance Network for Training LLMs with Trillion Parameters](https://arxiv.org/abs/2307.12169) (Required)
|         | [Lazarus: Resilient and Elastic Training of Mixture-of-Experts Models with Adaptive Expert Placement](https://arxiv.org/abs/2407.04656)
|         | **Post-Training**
| Oct  1  | [LoRA: Low-Rank Adaptation of Large Language Models](https://openreview.net/forum?id=nZeVKeeFYf9) (Required)
|         | [LIMA: Less Is More for Alignment](https://arxiv.org/abs/2305.11206) 
|         | [The Llama 3 Herd of Models (Section 4)](https://arxiv.org/abs/2407.21783) (Required)
|         | **Inference**
| Oct  3  | [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://dl.acm.org/doi/10.1145/3600006.3613165) (Required)
|         | [vAttention: Dynamic Memory Management for Serving LLMs without PagedAttention](https://arxiv.org/abs/2405.04437) (Required)
|         | [FlexGen: High-Throughput Generative Inference of Large Language Models with a Single GPU](https://proceedings.mlr.press/v202/sheng23a.html)
| Oct  8  | [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://openreview.net/forum?id=mZn2Xyh9Ec) (Required)
|         | [FlashDecoding++: Faster Large Language Model Inference with Asynchronization, Flat GEMM Optimization, and Heuristics](https://proceedings.mlsys.org/paper_files/paper/2024/hash/5321b1dabcd2be188d796c21b733e8c7-Abstract-Conference.html)
|         | [SpecInfer: Accelerating Large Language Model Serving with Tree-based Speculative Inference and Verification](https://dl.acm.org/doi/10.1145/3620666.3651335) (Required)
| Oct 10  | [Splitwise: Efficient Generative LLM Inference Using Phase Splitting](https://ieeexplore.ieee.org/abstract/document/10609649) (Required)
|         | [DistServe: Disaggregating Prefill and Decoding for Goodput-optimized Large Language Model Serving](https://www.usenix.org/conference/osdi24/presentation/zhong-yinmin)
|         | [Llumnix: Dynamic Scheduling for Large Language Model Serving](https://www.usenix.org/conference/osdi24/presentation/sun-biao) (Required)

| Oct 17  | [Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services](https://arxiv.org/abs/2404.16283) (Required)
|         | [Fairness in Serving Large Language Models](https://www.usenix.org/conference/osdi24/presentation/sheng) (Required)
|         | [Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://www.usenix.org/conference/osdi24/presentation/agrawal)
| Oct 22  | **Mid-Semester Presentations**
| Oct 24  | **Mid-Semester Presentations**
| Oct 29  | **No Lecture: Recalibrate Projects**
| Oct 31  | **No Lecture: Work on Projects**
| Nov  5  | **No Lecture: Work on Projects**
| Nov  7  | [dLoRA: Dynamically Orchestrating Requests and Adapters for LoRA LLM Serving](https://www.usenix.org/conference/osdi24/presentation/wu-bingyang) (Required)
|         | [Mixture of LoRA Experts](https://openreview.net/forum?id=uWvKBCYh4S) (Required)
|         | [MuxServe: Flexible Spatial-Temporal Multiplexing for Multiple LLM Serving](https://openreview.net/forum?id=R0SoZvqXyQ)
| Nov 12  | [AWQ: Activation-aware Weight Quantization for On-Device LLM Compression and Acceleration](https://proceedings.mlsys.org/paper_files/paper/2024/hash/42a452cbafa9dd64e9ba4aa95cc1ef21-Abstract-Conference.html) (Required)
|         | [LLM in a flash: Efficient Large Language Model Inference with Limited Memory](https://arxiv.org/abs/2312.11514) (Required)
|         | [SpotServe: Serving Generative Large Language Models on Preemptible Instances](https://dl.acm.org/doi/10.1145/3620665.3640411)
|         | **Grounding**
| Nov 14  | [Improving Language Models by Retrieving from Trillions of Tokens](https://proceedings.mlr.press/v162/borgeaud22a.html)
|         | [Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection](https://openreview.net/forum?id=hSyW5go0v8) (Required)
|         | [Fast Vector Query Processing for Large Datasets Beyond GPU Memory with Reordered Pipelining](https://www.usenix.org/conference/nsdi24/presentation/zhang-zili-pipelining) (Required)
|         | **GenAI (for) Systems**
| Nov 19  | [Parrot: Efficient Serving of LLM-based Applications with Semantic Variable](https://www.usenix.org/conference/osdi24/presentation/lin-chaofan) (Required)
|         | [The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/)
|         | [Automatic Root Cause Analysis via Large Language Models for Cloud Incidents](https://dl.acm.org/doi/10.1145/3627703.3629553) (Required)
|         | **Power and Energy Optimizations**
| Nov 21  | [Perseus: Reducing Energy Bloat from Large Model Training](https://arxiv.org/abs/2312.06902) (Required)
|         | [DynamoLLM: Designing LLM Inference Clusters for Performance and Energy Efficiency](https://arxiv.org/abs/2408.00741) (Required)
|         | [Characterizing Power Management Opportunities for LLMs in the Cloud](https://dl.acm.org/doi/abs/10.1145/3620666.3651329)
|         | **Ethical Considerations**
| Nov 26  | [Sociotechnical Safety Evaluation of Generative AI Systems](https://arxiv.org/abs/2310.11986) (Required)
|         | [On the Dangers of Stochastic Parrots: Can Language Models be too Big?🦜](https://dl.acm.org/doi/abs/10.1145/3442188.3445922) (Required) 
|         | [Foundation Models and Fair Use](https://arxiv.org/abs/2303.15715)
| Nov 28  | **No Lecture: Thanksgiving Recess**
| Dec  3  | **No Lecture: Work on Posters**
|         | [How to Write a Great Research Paper](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/) (Required)
| Dec  5  | **Final Poster Presentations**<br>TBA


## Policies


### Groups
All activities of this course will be performed in **groups of 2-3 students**.

### Required Reading
Each lecture will have **two required reading that everyone must read**.  
There will be *one or more optional related reading(s)* that only the presenter(s) should be familiar with.
They are optional for the rest of the class.

### Student Lectures
The course will be conducted as a seminar. 
Only one group will present in each class.
Each group will be assigned *at least one lecture* over the course of the semester. 
Presentations should last **at most 40 minutes** without interruption.
However, presenters should expect questions and interruptions throughout. 

In the presentation, you should:

* Provide necessary background and motivate the problem.
* Present the high level idea, approach, and/or insight (using examples, whenever appropriate) in the required reading as well as the additional reading. 
* Discuss technical details so that one can understand key details without carefully reading.
* Explain the differences between related works.
* Identify strengths and weaknesses of the required reading and propose directions of future research.

*The slides for a presentation must be emailed to the instructor team at least 24 hours prior to the corresponding class.* 
Use Google slides to enable in-line comments and suggestions.

### Lecture Summaries
Each group will also be assigned to **write summaries for at least one lectures**. 
The summary assigned to a group will not be the reading they gave the lecture on.

A paper summary must address the following four questions in sufficient details (2-3 pages):

* What is the problem addressed in the lecture, and why is this problem important?
* What is the state of related works in this topic?
* What is the proposed solution, and what key insight guides their solution?
* What is one (or more) drawback or limitation of the proposal?
* What are potential directions for future research?

*The paper summary of a paper must be emailed to the instructor team within 24 hours after its presentation.* 
**Late reviews will not be counted.** 
You should use [this format](Summaries/Template.md) for writing your summary.
Use Google doc to enable in-line comments and suggestions.

*Allocate enough time for your reading, discuss as a group, write the summary carefully, and finally, include key observations from the class discussion.*

### Post-Presentation Panel Discussion 
To foster a deeper understanding of the papers and encourage critical thinking, each lecture will be followed by a panel discussion. 
This discussion will involve three distinct roles played by different student groups, simulating an interactive and dynamic scholarly exchange.

#### Roles and Responsibilities

1. **The Authors**
- Group Assignment: The group that presents the paper and the group that writes the summary will play the role of the paper's authors.
- Responsibility: As authors, you are expected to defend your paper against critiques, answer questions, and discuss how you might improve or extend your research in the future, akin to writing a rebuttal during the peer-review process.


2. **The Reviewers**
- Group Assignment: Each group will be assigned to one slot to play the role of reviewers.
- Responsibility: Reviewers critically assess the paper, posing challenging questions and highlighting potential weaknesses or areas for further investigation. 
Your goal is to engage in a constructive critique of the paper, simulating a peer review scenario.

 
3. **Rest of the Class**
- Responsibility: 
  - You are required to [submit](https://forms.gle/Us8pr5o4R4TtzMzU7) **one insightful question** for each presented papers before each class. 
  - During the panel discussions, feel free to actively **ask questions** and engage in the dialogue. 

### Participation
Given the discussion-based nature of this course, participation is required both for your own understanding and to improve the overall quality of the course.
You are expected to attend **all** lectures (you may skip up to 2 lectures due to legitimate reasons), and more importantly, participate in class discussions.

A key part of participation will be in the form of discussion in Piazza.
The group in charge of the summary should initiate the discussion and the rest should participate.
Not everyone must have add something every day, but it is expected that everyone has something to say over the semester.

### Project
You will have to complete substantive work an instructor-approved problem and have original contribution.
Surveys are not permitted as projects; instead, each project must contain a survey of background and related work.

You must meet the following milestones (unless otherwise specified in future announcements) to ensure a high-quality project at the end of the semester:

* Form a group of 2-3 members and [declare your group's membership and paper preferences](https://forms.gle/t8n6V9ewJoDWTaSL9) by **January 23**. After this date, we will form groups from the remaining students.
* Turn in a 2-page draft proposal (including references) by **February 9**. Remember to include the names and Michigan email addresses of the group members. 
* Each group must present mid-semester progress during class hours on **March 12 and March 14**.
* Each group must turn in an 8-page final report and your code via email **on or before 6:00PM EST on May 1.** The report must be submitted as a PDF file, with formatting similar to that of the papers you've read in the class. The self-contained (i.e., include ALL dependencies) code must be submitted as a zip file. Each zip file containing the code must include a README file with a step-by-step guide on how to compile and run the provided code.
* You can find how to access GPU resources [here](./Resources/Starting%20with%20Cloudlab).

## Tentative Grading
|                         | Weight | 
| ------------------------| ------:| 
| Paper Presentation      | 15%    | 
| Paper Summary           | 15%    | 
| Participation           | 10%    | 
| Project Report          | 40%    | 
| Project Presentations   | 20%    | 


## Acknowledgement
*The course is inspired by CSE 585: Advanced Scalable Systems for Generative AI (UMich), CS8803: Systems for AI - LLMs(Gatech), and CS 598: Systems for Generative AI (UIUC).

