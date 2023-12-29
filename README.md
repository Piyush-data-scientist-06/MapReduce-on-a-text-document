# MapReduce-on-a-text-document
Practically applied MapReduce concepts in a real-world data processing scenario using Python.
## Dataset selection:
Chosen a large dataset (textual document on 'What is a Statistical Project?') that requires significant computational resources to process. <br>
PyPDF2 for PDF processing, re for regular expressions, defaultdict from collections for easier data management, Pool from multiprocessing for parallel processing, and time for tracking execution times, are the important libraries that have been used. 
## Problem statement:
We perform a word count analysis on the text data extracted from the PDF. We will count the frequency of each word using the MapReduce model.
# Approach:
The approach taken in this MapReduce job involves a parallelized computation to perform a word count on a large text dataset. The code utilizes Python's multiprocessing capabilities to distribute the map and reduce tasks across multiple worker processes. The performance of this parallelized approach is compared with a non-parallelized (sequential) execution. The objective is to understand the impact of process pooling on the execution time of the MapReduce job.
# Tasks to perform:
## Implement MapReduce:
- Use the provided parallel_map_reduce function as a starting point.
- Develop a custom map function specific to your problem statement.
- Develop a corresponding reduce function. <br>

## Performance analysis:
- Run the MapReduce job on your dataset.
- Measure the execution time and compare it with a non-parallelized approach.
- Analyze the scalability of your solution by varying the pool_size parameter. <br>

## Report Writing:
- Document your approach, code, results, and observations.
- Discuss the scalability and efficiency of the MapReduce model based on your findings.
- Reflect on the challenges faced and potential improvements. <br>

# Results and Observations:
Performance Analysis Times: {1: 0.028107404708862305, 2: 0.027884244918823242, 4: 0.048342227935791016, 8: 0.12561392784118652, 'non_parallel': 0.0005130767822265625}
From the output, the following observations can be made:
- The non-parallelized approach has the fastest execution time at approximately 0.00051 seconds.
- With a single process in the pool (which effectively makes it sequential), the execution time is around 0.028 seconds, which is slower than the non-parallelized run.
- As the pool size increases to 2, the execution time decreases slightly to 0.0278 seconds, indicating that some benefit is gained from parallel processing. <br>

However, further increasing the pool size to 4 and 8 results in increased execution times, 0.0483 and 0.125 seconds, respectively. This suggests that there is an overhead associated with managing a larger number of processes that outweighs the benefits of parallelism for this task.

