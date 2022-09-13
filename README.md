# Job Hunt
This is offer detail and reference material used for interview practice.

## Results

### Offers
_Format: company, role, location, annual comp range_
- Bridgewater Associates, ML Research Engineer, remote, 400-450k
- Dropbox, IC3 MLE, remote, 400-450k
- Two Sigma, L3 SWE, NYC, 400-450k
- Amazon, L5 MLE, NYC or remote, 400-450k
- Kensho Technologies, Sr. MLE, remote, 350-400k
- Spotify, Sr. MLE, remote, 300-350k
- Bloomberg AI, Research Engineer, NYC, 300-350k
- Disney Streaming, Sr. MLE, remote, 300-350k
- Mailchimp, Sr. MLOps Eng., remote, 250-300k
- Other companies,Sr. MLE, 200-250k

### Waiting
- Google, L4 SWE-ML
- Meta, IC4 MLE

### Cancelled
- Atlassian
- Pinterest
- Etsy
- Uber
- Doordash
- Bytedance / Tiktok
- Cerberus Capital
- ScaleAI

### Rejections
- D. E. Shaw
- Reddit
- Hudson River Trading
- Roblox
- Zoom
- Quora
- Citadel, Jane Street, Stripe, Roku, Microsoft, Snap

## Preparation

Overall prep took about 1-2 months and I started interviewing at around the 1.5 month mark. I first started with coding and then started everything else once I was comfortable with Leetcode. The most challenging type of interview turned out to be system design and ML system design, because the exposure to scalable systems is pretty limited in Gamma in my experience. These interviews are _**especially important**_ as you target senior+ level ML roles in tech.

I went through a lot of material during prep so I'll try to highlight only the stuff that I thought were useful for interviews.

### Algorithms & Data Structures
- Started with [Elements of Programming Interviews in Python](https://www.amazon.com/Elements-Programming-Interviews-Python-Insiders/dp/1537713949); did every question in the main sections and practiced writing out solutions in one go in a simple text editor
- Got Leetcode Premium and practiced [Blind 75](https://leetcode.com/discuss/general-discussion/460599/blind-75-leetcode-questions) then worked through the top 100 tagged questions for the companies I was interviewing with
- Did about 450 problems in total and kept a failure log to revisit patterns that I missed
- It's good to know some trivia on advanced data structures like k-d trees, bloom filters, segment trees, Fenwick trees, as they pop up once in a while
- For hedge funds you'll need to know some CS fundamentals, e.g. heap vs. stack memory, garbage collection, multithreading vs. multiprocessing

### ML Coding
Some roles require ML specific coding rounds, which is usually one of
- Implement k-means from scratch (VERY popular question; I've been asked this so many times I can recite it from memory)
- Implement gradient descent from scratch for simple functions
- Implement Naïve Bayes from scratch

### System Design
- Started with [Sys Design Primer](https://github.com/donnemartin/system-design-primer) and [Grokking Sys Design](https://www.educative.io/courses/grokking-the-system-design-interview) to familiarize myself with key concepts and flow
- Worked through the videos on [CodeKarle](https://www.codekarle.com/) and [SystemDesignInterview](https://www.youtube.com/c/SystemDesignInterview) which provided a lot more depth
- Honestly I never got very good at them so look elsewhere for resources too

### ML System Design
- Started with regular system design so I knew basic building blocks of a scalable system (e.g. Kafka, Redis, Cassandra)
- Read some blogs and courses for foundational knowledge
  - [ML Systems Design Interview Guide](http://patrickhalina.com/posts/ml-systems-design-interview-guide/)
  - [Stanford CS329s Course Slides](https://stanford-cs329s.github.io/2021/syllabus.html)
  - [GCloud: Modern MLOps Architecture](https://cloud.google.com/architecture/mlops-continuous-delivery-and-automation-pipelines-in-machine-learning) (followed this as deployment pattern)

  - [Grokking the Machine Learning Interview](https://www.educative.io/courses/grokking-the-machine-learning-interview) (a lot of useful example solutions)
  - [Uber: Michelangelo](https://www.uber.com/blog/michelangelo-machine-learning-platform/) (used this for all Feature Store designs in my interviews)
    ![image](https://github.gamma.bcg.com/storage/user/3188/files/0ea672b7-56b4-4eb8-8e17-627602e2f121)

- Understand tradeoffs and motivations behind key design decisions, e.g. for online feature store, in what scenarios would Redis make more sense than Cassandra and vice versa?
- Deep dive into recommender systems since they're the most common type of ML system to be asked
  - [System Design for Recommendations and Search](https://eugeneyan.com/writing/system-design-for-discovery/) (used this architecture as template for most interviews)
    ![image](https://github.gamma.bcg.com/storage/user/3188/files/bf03197c-1d89-4481-a160-7c528a2dfa5a)

  - Understand key concepts and components:
    - Embeddings and how to generate them (e.g. two-tower networks is the standard modern approach)
    - Approximate nearest neighbor indexing and search
    - Learning-to-rank models; difference between pointwise, pairwise, and listwise
    - Evaluation metrics: rank-aware and classification metrics
- Made a template to follow so I don't miss anything during interviews:
  ```
  - Objective
    - Purpose, requirements, how it'll be used, etc.
  - Modeling
    - Input data source, truth label source (label generation is usually an important topic)
    - Data preparation (including sampling scheme, train-test split scheme)
    - Feature engineering
    - Model approach / task definition (always mention a baseline / heuristic as starting point before main ML model)
    - Offline evaluation metrics
  - System Design
    - High level design for training (offline) and inference (real-time)
    - Experimentation and online evaluation
    - Addressing scalability, availability, and latency
  ```

### ML Theory
- Review your favorite ML and DL course notes from school
- Know your tradeoffs and fundamentals
  - L1 vs. L2 regularization and their geometric interpretations
  - LSTM vs. Transformers; what scenarios would you prefer LSTM?
  - What exactly does a language model aim to do? What are some ways to train one?
  - Why BatchNorm? Why dropout?
  - SGD vs. minibatch gradient descent
  - Maximum Likelihood vs. Maximum a Posteriori
  - Deep learning vs. Tree-based models
  - Random Forest vs. GBT
  - Different types of encodings and when to use them
- Other random topics that came up
  - Semi-supervised learning
  - Multi-label classification
  - K-means initialization schemes and convergence

### Behavioral
- Prepare stories using the STAR method but also make sure to include technical aspects such as:
  - Hardest bug / technical challenge
  - Most innovative thing you've done
  - Time when you built something that had impact outside of your immediate project
- Out of my 3 years of work here, I'd say bulk of the stories came from maybe 6-8 months of work because a lot of projects just weren't meaty / technical enough
- Use [Amazon's leadership principles](https://www.levels.fyi/blog/amazon-leadership-principles.html) or the framework in Cracking the Coding Interview book as a way of organizing your stories

## Misc notes

- Vast majority of my applications were cold applies on Linkedin or company's job site, but I did try to get referrals from Gamma alums or from strangers on Blind when possible
- If I were to do this again, I'd study and practice system design more so I could understand the technologies better and be more polished

Hope this helps and best of luck in your future search!!
