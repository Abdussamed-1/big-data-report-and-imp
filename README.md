# Big Data — Readings, Research & Implementations

> You don't really understand something until you can build it from scratch.

This repo is a personal workspace where I keep everything related to my journey through the world of big data — notes from readings and research, code I write to solidify concepts, and hands-on experiences with systems like Apache Spark and Apache Hadoop. The idea is to learn by doing, and to document that process honestly.

Nothing here is "final" or "polished." Some notes will be incomplete, some code could be written better. That's fine. The point is to make progress visible.

---

## Repository Layout

```
big-data-report-and-imp/
│
├── Reports/               # Summaries and notes from books, papers, and articles
│   ├── papers/             # Classic academic papers (GFS, MapReduce, Bigtable...)
│   └── books/              # Book notes
│
├── concepts/               # Theoretical notes written in my own words
│
├── hadoop/                 # Everything Hadoop-related
│   ├── setup/              # Installation notes and config files
│   ├── hdfs/               # HDFS experiments
│   └── mapreduce/          # MapReduce examples
│
├── spark/                  # Apache Spark experiments
│   ├── setup/              # Spark setup and environment prep
│   ├── rdd/                # RDD-based operations
│   ├── dataframes/         # DataFrame and Dataset APIs
│   ├── streaming/          # Spark Structured Streaming
│   └── ml/                 # Machine learning experiments with MLlib
│
├── projects/               # More complete end-to-end mini projects
│
└── resources.md            # Useful links, tools, and references
```

> Note: This structure will evolve over time. When I'm unsure where something belongs, I check this layout before creating new folders.

---

## Why This Repo?

Taking notes while learning helps me figure out what I actually understand versus what I just recognize. Big data systems are especially tricky that way — they sound intuitive until you try to set one up, and then everything falls apart in surprisingly educational ways.

The first time I set up Hadoop, I spent hours stuck on a `JAVA_HOME` issue. Running a Spark job on a cluster turned into a battle with executor memory configurations. I want to document moments like these too — because they don't show up in official docs, but they're right in the middle of how real learning happens.

---

## What's Covered

### Readings & Research

I'm starting with the foundational academic papers that shaped modern distributed data systems. Three papers from Google in the early 2000s are essential groundwork:

- **The Google File System** (Ghemawat et al., 2003) — the inspiration behind HDFS
- **MapReduce: Simplified Data Processing on Large Clusters** (Dean & Ghemawat, 2004) — the foundation of Hadoop MapReduce
- **Bigtable: A Distributed Storage System for Structured Data** (Chang et al., 2006) — the inspiration behind HBase

Beyond those, I'm also following the **Resilient Distributed Datasets** paper (the origin story of Spark) and more recent work on streaming and real-time processing.

### Apache Hadoop

I'm learning Hadoop by actually setting it up and breaking things. Starting from pseudo-distributed mode and working toward a multi-node cluster setup. Topics I'm working through:

- Installation and configuration (`core-site.xml`, `hdfs-site.xml`, `mapred-site.xml`, `yarn-site.xml`)
- Reading and writing files on HDFS
- Classic MapReduce examples (Word Count, inverted index, etc.)
- YARN for resource management

### Apache Spark

Spark offers a much richer API than Hadoop MapReduce and runs significantly faster for iterative workloads. I'm working through it layer by layer — from low-level RDDs up to Structured Streaming:

- **RDD API** — Spark's core abstraction; understanding transformations vs. actions
- **DataFrame / Dataset API** — Higher-level, SQL-like operations
- **Spark SQL** — Querying DataFrames directly with SQL
- **Structured Streaming** — Real-time data processing on a stream-as-a-table model
- **MLlib** — Distributed machine learning algorithms

### Ecosystem

Tools I plan to explore over time:

| Tool | What It Does |
|---|---|
| Apache Hive | SQL-like querying over large datasets on HDFS |
| Apache Kafka | High-throughput, real-time message streaming |
| Apache HBase | Distributed, column-oriented NoSQL database |
| Apache ZooKeeper | Coordination service for distributed systems |
| Apache Flink | Alternative engine for both stream and batch processing |

---

## Environment

Most experiments are running on my local machine for now. Eventually I plan to move toward Docker-based isolated environments and possibly managed cluster setups on a cloud provider.

**Tools I'm using:**
- Java 11 / Python 3.x
- Apache Hadoop 3.x
- Apache Spark 3.x
- Jupyter Notebook (with PySpark kernel for Spark experiments)
- Docker (for environment isolation)

---

## Resources

Starting points I've found genuinely useful:

**Books**
- *Learning Spark* — Jules S. Damji et al. (O'Reilly) — the best hands-on intro to Spark
- *Hadoop: The Definitive Guide* — Tom White (O'Reilly)
- *Designing Data-Intensive Applications* — Martin Kleppmann — approaches big data from a systems design perspective; essential reading

**Papers**
- [The Google File System](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
- [MapReduce](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
- [Resilient Distributed Datasets (Spark)](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)

**Official Docs**
- [Apache Spark Documentation](https://spark.apache.org/docs/latest/)
- [Apache Hadoop Documentation](https://hadoop.apache.org/docs/stable/)

---

## Status

This repo is actively growing. Whenever I learn something new, run into an interesting failure, or understand something differently than before, I add it here. The commit history is essentially a learning journal.

---

*Samet — 2026*
