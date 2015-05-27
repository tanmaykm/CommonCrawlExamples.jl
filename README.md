# CommonCrawlExamples

[![Build Status](https://travis-ci.org/tanmaykm/CommonCrawlExamples.jl.svg?branch=master)](https://travis-ci.org/tanmaykm/CommonCrawlExamples.jl)

- Make sure you have your AWS access keys setup in the file `~/.awssecret` (ref: https://github.com/amitmurthy/AWS.jl)
- `Pkg.clone("https://github.com/tanmaykm/CommonCrawlExamples.jl.git")`
- `using CommonCrawlExamples`
- `setup_folders(clean=true) # use true to discard cached files and indexes and rebuild afresh`
- `create_index(5) # index 5 archives`
