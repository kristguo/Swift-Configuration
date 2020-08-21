| **Confifiguration Parameters—Description**                   | Abbr. | Range           | Default              |
| :----------------------------------------------------------- | ----- | --------------- | -------------------- |
| **parallelism.default**-The default parallelism to use for programs that have no parallelism specifified. | PLDT  | 1-12            | 1                    |
| **jobmanager.heap.mb** - JVM heap size (in megabytes) for the JobManager. | JMHP  | 1024-6144       | 1024                 |
| **taskmanager.heap.mb** - JVM heap size (in megabytes) for the TaskManager. | TMHP  | 2048-6144       | 1024                 |
| **taskmanager.memory.off-heap** - the task manager allocates memory which is used for sorting, hash tables, and caching of intermediate results outside of the JVM heap. | TMOH  | false, true     | false                |
| **taskmanager.memory.fraction** - The relative amount of memory that the task manager reserves for sorting, hash tables, and caching of intermediate results. | TMFT  | 0.1-0.9         | 0.7                  |
| **taskmanager.memory.segment-size** - The size of memory buffers used by the memory manager and the network stack in bytes. | TMSS  | 2KB - 2M        | 32KB                 |
| **taskmanager.runtime.hashjoin-bloom-fifilters** - Flag to activate/ deactivate bloom fifilters in the hybrid hash join implementation. | TRHB  | false, true     | false                |
| **taskmanager.runtime.sort-spilling-threshold** - A sort operation starts spilling when this fraction of its memory budget is full. | TRSS  | 0.1 - 0.9       | 0.8                  |
| **taskmanager.runtime.max-fan** - The maximal fan-in for external merge joins and fan-out for spilling hash tables. | TRMF  | 80 - 300        | 128                  |
| **taskmanager.network.memory.fraction** - Fraction of JVM memory to use for network buffers. | TNMF  | 0.1 - 0.9       | 0.1                  |
| **taskmanager.net.num-arenas** - the number of Netty arenas (same to taskmanager. numberOfTaskSlots). | TNNA  | 1-4             | #slot                |
| **taskmanager.net.server.numThreads** - The number of Netty server thread (same to taskmanager. numberOfTaskSlots). | TNSN  | 1-4             | #slot                |
| **taskmanager.net.client.numThreads** - The number of Netty client threads (same to taskmanager. numberOfTaskSlots). | TNCN  | 1-4             | #slot                |
| **blob.fetch.num-concurrent** - The number concurrent BLOB fetches (such as JAR fifile downloads) that the JobManager serves | BFNC  | 50 - 200        | 50                   |
| **blob.fetch.retries** - The number of retries for the TaskManager to download BLOBs (such as JAR fifiles) from the JobManager. | BFRT  | 50 - 200        | 50                   |
| **akka.framesize** - Maximum size of messages which are sent between the JobManager and the TaskManagers | AKFS  | 6M - 21M        | 10M                  |
| **akka.watch.threshold** - Threshold for the DeathWatch failure detector. | AKWT  | 8 - 21          | 12                   |
| **taskmanager.network.memory.min** - Minimum memory size for network buffers in bytes. | TNMI  | 32M - 1024M     | 64M                  |
| **taskmanager.network.memory.max** - Minimum memory size for network buffers in bytes. | TNMA  | 1024M - 4096M   | 1024M                |
| **taskmanager.net.sendReceiveBufferSize** - The Netty send and receive buffer size(defaul to the system buffer size). | TNRB  | 763659- 1527317 | #system buffer sizes |
| **blob.fetch.backlog** - The maximum number of queued BLOB fetches (such as JAR fifile downloads) that the JobManager allows. | BFBL  | 500 - 3000      | 1000                 |
| **jobmanager.tdd.offlfload.minsize** - Maximum size of the TaskDeploymentDescriptor’s serialized task and job information to still transmit them via RPC. | JTOM  | 900 - 4096      | 1024                 |
| **fs.overwrite-fifiles** - Specififies whether fifile output writers should overwrite existing fifiles by default. | FSOF  | false, true     | false                |
| **fs.output.always-create-directory** - File writers running with a parallelism larger than one create a directory for the output fifile path and put the different result fifiles (one per parallel writer task) into that directory. | FOAC  | false, true     | false                |
| **compiler.delimited-informat.max-line-samples** - The maximum number of line samples taken by the compiler for delimited inputs. | CDIA  | 9 - 20          | 10                   |
| **compiler.delimited-informat.min-line-samples** - The minimum number of line samples taken by the compiler for delimited inputs. | CDII  | 2-8             | 2                    |
| **compiler.delimited-informat.max-sample-len** - The maximal length of a line sample that the compiler takes for delimited inputs. | CDAL  | 1M - 10M        | 2M                   |
