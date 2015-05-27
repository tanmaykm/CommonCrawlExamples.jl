# CommonCrawlExamples

These are some toy examples using [CommonCrawl.jl](https://github.com/tanmaykm/CommonCrawl.jl), suitable for demonstratons.

## Simple Distributed Indexing and Searching

The index simply represents documents where each word in the vocabulary appears, without any relevance score.

- Make sure you have your AWS access keys setup in the file `~/.awssecret` (ref: [AWS Security Credentials](http://docs.aws.amazon.com/AWSSecurityCredentials/1.0/AboutAWSCredentials.html) and [AWS.jl](https://github.com/amitmurthy/AWS.jl))
- `Pkg.clone("https://github.com/tanmaykm/CommonCrawlExamples.jl.git")`
- `using CommonCrawlExamples`
- `setup_folders(true) # use true to discard cached files and indexes and rebuild afresh, false to reuse`
- `create_index(5) # index 5 archives`
- `search_index("search terms") # search for any of the words`

To index in parallel:
- Ensure CommonCrawlExamples is available on all nodes
- Use `addprocs` to add required number of cores
- `setup_folders(true) # create or cleanup work folders on all nodes`
- `create_index` and `search_index` delegate tasks to worker nodes
