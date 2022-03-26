> creating a project roadmap the entire team can follow
> details and goals are outlines in order to meet the requirements laid out by the organization

 - Create a project plan
 - Develop a resource plan
 - Define goals and performance measures
 - Communicate roles and responsibilities to team members
 - Build out workflows
 - Anticipate risks and create contingency plans

> Next Phase project kickoff meeting
> outlines the project objectives to all stakeholders involved

### To do for pm

  - Establish goals and deliverables
  - Identify your team members and assign tasks
  - Develop a draft project plan
  - Define which metrics will be used to measure project success
  - Identify and prepare for potential roadblocks
  - Establish logistics and schedules for team communication
  - Choose your preferred project management methodology
  - Ensure your team has access and knowledge of the relevant tools
  - Schedule the meeting
  - Set the agenda and prepare the slides




### magento2/adobe commerce Hardware/tech stack requirement benchmark 
##### Example

- SKUs: 1000
- product type: simple+configurable?
- Visitors per day/month: 500
- peak visitors/time: 1500-2000
- Transactions: 200
- storeview:2
- website:

#### Hardware recommendations

- CPU

> N[Cores] = (N[Expected Requests] / 2) + N [Expected Cron Processes]

- Memory

single server = 2GB or pipeline deployment + 2GB + 1GB web node
Scenarios and expected PHP memory requirements:
* Webnode serving only storefront pages: 256 MB
* Webnode serving admin pages with a large catalog: 1 GB
* Magento 2 cron indexing a site with a large catalog: >256 MB [advanced setup](https://devdocs.magento.com/guides/v2.4/performance-best-practices/advanced-setup.html)
* Magento 2 compile and deploy of static assets: 756 MB
* Magento 2 performance toolkit profile generation: >1 GB PHP RAM, >16 MB MySQL TMP_TABLE_SIZE & MAX_HEAP_TABLE_SIZE settings

##### MySQL
To effectively leverage MySQL data indexation, the amount of memory available should be, at minimum, close to half the size of the data stored in the database

##### Caches
If you are deploying multiple Magento 2 and using Redis or Varnish for your caches, please keep the following principles in mind:

* Varnish full page cache memory invalidation is effective, recommend enough memory allocated to Varnish to hold your most popular pages in memory
* Session cache is a good candidate to configure for a separate instance of Redis. Memory configuration for this cache type should consider the site’s cart abandonment strategy and how long a session should expect to remain in the cache
* Redis should have enough memory allocated to hold all other caches in memory for optimal performance. Block cache will be the key factor in determining the amount of memory to configure. Block cache grows relative to number of pages on a site (number of skus x number of store views)

##### Network bandwidth

Sufficient network bandwidth is one of the key requirements for data exchange between web nodes, database(s), caching/session servers, and other services. Because Magento 2 effectively leverages caching for high performance, your system can actively exchange data with caching servers like Redis. If Redis is located on a remote server, you must provide a sufficient network channel between web nodes and the caching server to prevent bottlenecks on read/write operations.


#### [Software recommendations](https://devdocs.magento.com/guides/v2.4/performance-best-practices/software.html)



