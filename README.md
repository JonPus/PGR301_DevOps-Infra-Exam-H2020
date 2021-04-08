# PGR301_DevOps-Infra-Exam-H2020 - Terraform Infrastructure [![Build Status](https://travis-ci.com/JonPus/PGR301_DevOps-Infra-Exam-H2020.svg?token=WNYDyxATS1ezQLqAT1RT&branch=master)](https://travis-ci.com/JonPus/PGR301_DevOps-Infra-Exam-H2020)

`Eksamen i PGR301 DevOps i skyen, kandidatnummer:	10007`

## Exam Grade: A

Denne repositoryen er koblet sammen med min Github repository [JonPus/PGR301-DevOps-Exam-H2020](https://github.com/JonPus/PGR301-DevOps-Exam-H2020)

### Google Cloud

1. Lag en egen IAM Service Account for Terraform med rettighetene

- `Container Registry Agent`
- `Storage Admin`
- `Cloud Run Admin`
- `Service Account User`

2. Last ned nøkkelfilen til den nye IAM Service Account brukeren og endre navnet til `google-key.json` og kjør kommandoen `travis encrypt-file google-key.json --add` i terminalen i prosjekt directorien.

2. Lag en Cloud Storage Bucket som skal oppbevaring av forskjellige Docker imagen av de forskjellige versjonen av applikasjonen.

3. Kjør travis encrypt <ENV.VAR>=<VALUE> på følgende API nøkler for å hemmeliggjøre de.
  * `Google Cloud` sin `IAM Service account` token.
  * `StatusCake` sin API token
  * `OpsGenie` sin API token
  * `LOGZ.io` sin API token og URL addresse.
  
 4. Legg de krypterte verdiene i .travis.yml filen.

## StatusCake 

<a href="https://www.statuscake.com" title="Website Uptime Monitoring"><img src="https://app.statuscake.com/button/index.php?Track=5745939&Days=1&Design=2" /></a>

*"[StatusCake](https://www.statuscake.com/) provides website monitoring and sends alerts when a user's website goes down or is experiencing other technical problems such as being slow to load."*

Med SAAS løsningen StatusCake så kan man se hvordan applikasjonen forholder seg på nettet, der vi kan sjekke når den er av og på.

## OpsGenie 

*"[OpsGenie](https://www.atlassian.com/software/opsgenie) is a modern incident management platform that ensures critical incidents are never missed, and actions are taken by the right people in the shortest possible time. Opsgenie receives alerts from your monitoring systems and custom applications and categorizes each alert based on importance and timing."*

Med OpsGenie så kan vi via Terraform opprette folk til å passe på at ting går som det skal på applikasjonen, og at uventet nedetid kan fikses med e ngang via at OpsGenue kontakter den riktige personen til den riktige jobben.

