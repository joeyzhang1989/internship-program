# Static Documentation Site Using facebook open source template engine [docusaurus] (https://github.com/facebook/docusaurus)

## Highlights
* Set up using no time with provided template writing By React with ability to customized and extend
* Markdown format `GitHub Flavored Markdown (GFM)` support and building support to convert markdown to HTML (https://docusaurus.io/docs/en/doc-markdown)
* Versioning for docs use a single command (https://docusaurus.io/docs/en/versioning)
* Embedded support for algolia search (https://www.algolia.com/) used by a lot of public official documentation site for example (https://reactjs.org/), (https://babeljs.io/) and more and translation option(no need for us)
* Continuously support from the community with new versions and fix, also keep up with React changes.
* Support for Docker and Docker compose
* Good documentation

## Why we need
1. It is pretty
2. It is used by a lot of open-source framework
3. It provides features we need and ability to integrate with our existing pipeline and tools: Gitlab, stash(For git control). bamboo for site deployment and Docker support for projects like Pcaas-NG and DD. 
4. Readme is stash repo is ugly and Confluence search is crap. 

## It is feasible and with the ability to provide more values

* The algolia provided DOC search support that comes with open source tools we could use and later even benefits other projects like DMCA (https://github.com/algolia/docsearch)

The basic is simple, docsearch utilizing the algolia index populated by the algolia crawler `Algolia crawler 24 hours access interval only for public accessible site` to store the doc site content and later served for front-end search components. Doc Search is open source but algolia index is not free, but for small usage like us, it could be free (https://www.algolia.com/pricing/)

The issue is our doc site will be behind the firewall and will never be pubilic accessible to the rest of the world, and more importantly, we do not want to. 

So we could use the docsearch-scraper open-source crawler listed below to crawl our doc site and send the site structure and content to algolia index. (https://docsearch.algolia.com/docs/run-your-own/)

The concern is only how safe is the algolia index (https://www.algolia.com/doc/faq/security-privacy/is-my-data-encrypted-and-secured/)

If we still not convinced and feel secure to use algolia index we could try to use ES to replace the algolia (https://blog.patricktriest.com/text-search-docker-elasticsearch/) and just use the algolia open-source front-end elements`instant search supported for vue, angular and react`
[react-instantsearch-github]: https://github.com/algolia/react-instantsearch/
[vue-instantsearch-github]: https://github.com/algolia/vue-instantsearch
[instantsearch-angular-github]: https://github.com/algolia/angular-instantsearch

The extra values for other projects are customized the docsearch-scraper a bit to fit the structure of our web application like DMCA to provide the search for the contents in the sites. 

## Conclusion and why it fits the internship program 
Overall, it is achievable by an Intern by setting the right scope. We will need one with front-end experience, know python and have basic knowledge of DOCKER, git, and ability to write at least java APIs if we want to add login or other feature in Spring Boot.  

- [algolia/docsearch](https://github.com/algolia/docsearch) contains the `docsearch.js` code source and the
  documentation website.
- [algolia/docsearch-configs](https://github.com/algolia/docsearch-configs) contains the JSON files representing all the
  configs for all the documentations DocSearch is powering
- [algolia/docsearch-scraper](https://github.com/algolia/docsearch-scraper) contains the crawler we use to extract data
  from your documentation. The code is open-source and you can run it from
  a Docker image



