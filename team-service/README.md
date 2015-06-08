# Team Service Mock

Knows users, their teams and the cloud accounts they have access to.

## Usage

With node

    git checkout https://github.com/zalando-stups/mocks/tree/master/team-service
    cd team-service/src
    node server.js

With Docker

    docker run stups/mock-team-service

### Accepted environment variables

* `ENV_USER_SOURCE`: Path to a CSV file where user and their team are listed
* `ENV_TEAM_SOURCE`: Path to a CSV file where the teams and their cloud account id are listed.
* `ENV_TOKENINFO_URL`: URL of /tokeninfo endpoint to check OAuth2 access tokens.

## File formats

### user.csv

    # user id, team id
    npiccolotto,stups
    test,stups
    iam,greendale

### team.csv

    # team id, description, cloud account id, dn
    stups,Cloud Engineers,84849249,some-dn
    greendale,Identity Managers,5813148535,other-dn

## API

See [swagger.yml](swagger.yml).