ElasticSearch in a Docker container
=========
Instant ElasticSearch server using Docker and the trusted build of ElasticSearch

Dependencies
---

[Vagrant](https://www.vagrantup.com/downloads.html) (>=1.6)

[Docker](https://docs.docker.com/installation/#installation)

- For OSX: I was successful with [boot2docker](https://github.com/boot2docker/osx-installer/releases). If you have issues with boot2docker or prefer a lightweight approach, try [this](http://zaiste.net/2014/02/lightweight_docker_experience_on_osx/).



To Get Started
---

1. Clone the repository `git clone git@github.com:18F/docker-es.git`
2. Tell Vagrant where to find Docker by setting `export DOCKER_HOST=tcp://localhost:2375`
3. Be sure docker is running (if using boot2docker run `boot2docker init` and `boot2docker up`) and pull down the trusted build from the docker registry with `docker pull dockerfile/elasticsearch`.
4. Fire up Vagrant with `vagrant up --provider=docker` from the project root.
5. Test elasticsearch with `curl -X GET 'http://localhost:9200/_status?pretty=true'`


Roadmap
---
- Coming soon


Contributing
---

1. Fork it
2. Create your feature branch (`git checkout -b feature/my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

### Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
