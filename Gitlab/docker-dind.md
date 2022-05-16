```
build:
  image: docker:latest
  stage: build
  services:
    - docker:dind
  before_script:
    - echo "$CI_GITLAB_TOKEN" | docker login -u $CI_REGISTRY_USER --password-stdin $CI_REGISTRY
  script:
    - docker info
    - docker build --pull -t indiamart-practice/indiamart-proj . 
    - docker push registry.gitlab.com/indiamart-practice/indiamart-proj
    ```
