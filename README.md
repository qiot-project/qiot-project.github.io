# QIoT-Project Website Based on Jekyll

## Getting Started

These instructions will get you a copy of the qiot-project.github.io website up and running on your local machine for development and testing purposes.

### Installation
[Jekyll static site generator docs](https://jekyllrb.com/docs/).

1. Fork the [project repository](https://github.com/qiot-project/qiot-project.github.io), then clone your fork:

  ```sh
        git clone git@github.com:YOUR_USER_NAME/qiotio.github.io.git
```
2. Change into the project directory:

  ```sh
        cd qiot-project.github.io
```
3a. Pull and Run the [containerized version](https://hub.docker.com/r/jekyll/jekyll/) of the ruby bundler and jekyll runtime to install the required gems locally and run the jekyll server, using the [docker-compose file](https://raw.githubusercontent.com/qiot-project/qiot-project.github.io/develop/docker-compose.yaml) provided by the community: 

```sh
        docker-compose up
```
3b. Pull and Run the jekyll container manually:

```sh
        docker run --rm \
                --volume="$PWD:/srv/jekyll:Z" \
                --publish [::1]:4000:4000 \
                jekyll/jekyll \
                jekyll serve
```   
7. Now browse to http://localhost:4000

> If you encounter any unexpected errors during the above, please refer to the [troubleshooting](https://jekyllrb.com/docs/troubleshooting/#configuration-problems) page or the [requirements](https://jekyllrb.com/docs/installation/#requirements) page, as you might be missing development headers or other prerequisites.

**For more regarding the use of Jekyll, please refer to the [Jekyll Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/).**

### Deploying to Github Pages
The website deployment is automatically performed by GitHub Actions (when commits are pushed to the `develop` branch). 
If for some reason you need to deploy from your local machine, follow these instructions: 

1. Install the [act](https://github.com/nektos/act#installation) executable to run GitHub Actions locally
2. Run `act -s GITHUB_TOKEN=<GITHUB_TOKEN>`, where *<GITHUB_TOKEN>* needs to be replaced with a token that allows you to push to the https://github.com/qiot-project/qiotio.github.io repository.


## Writing a blog

To write a blog:

- create an author entry in [_data/authors.yaml](https://github.com/qiot-project/qiot-project.github.io/blob/develop/_data/authors.yaml)
    - `emailhash` is used to fetch your picture form the Gravatar service
- create an blog entry under [_posts](https://github.com/qiot-project/qiot-project.github.io/tree/develop/_posts)
    -the file name is `yyyy-mm-dd-slug.adoc`
- `category` must be **blog**. Other categories reserved to the project team you want to be aware of:
  - `announcement` - official project announcements
  - `project` - QIoT subprojects
  - `usecase` - Posts documenting the QIoT use-cases
- `tags` should be used with some care as an archive page is created for of them. Below are some basic rules to try follow:
  - add a tech specific, like `kafka`, if your post has a significant mention/relevance to that technology.
  - tags is space separated list `tags:extension grpc`
  - tags must be in lowercase
- it's in asciidoc format, there is an example as shown with [2021-03-17-quarkus-native-on-a-raspberry-pi.adoc](https://github.com/qiot-project/qiot-project.github.io/blob/develop/_posts/2021-03-17-quarkus-native-on-a-raspberry-pi.adoc)
  - Be aware that the `date` attribute in the asciidoc preamble defines when the article will be published. Use a present date while writing your article to test locally, then switch to the actual target date before submitting. 
- send a pull request against the develop branch and voilà

## Contributing

Please read [CONTRIBUTING.md](https://github.com/qiot-project/qiotio.github.io/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License

This website is licensed under the [Creative Commons Attribution 3.0](https://creativecommons.org/licenses/by/3.0/).

## Get in touch with the QIoT Team:

**Website**: qiot-project.github.io

**Email**: qiotproject@google.com

**Mailing list**: qiotproject@googlegroups.com

**Twitter**: @qiotproject

**Slack**: [<img src="https://github.com/qiot-project/qiot-project.github.io/blob/develop/assets/images/main/Slack_RGB-149x61-87ef42a.png">](https://join.slack.com/t/quarkusforiottechteam/shared_invite/zt-nuajdyqf-NfQL0dcfCUjFSgoBNng11A)

**Weekly meeting**: [<img src="https://www.google.com/calendar/images/ext/gc_button1_en.gif">](https://calendar.google.com/event?action=TEMPLATE&amp;tmeid=dmFxMzFlZGkxOHVubDcyYm50bjdrcTJxYThfMjAyMTAzMjVUMTYwMDAwWiBxaW90cHJvamVjdEBt&amp;tmsrc=qiotproject%40gmail.com&amp;scp=ALL)

