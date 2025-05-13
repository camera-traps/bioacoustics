# Bioacoustics

## Mapping bioacoustic datasets to Camtrap DP

This repository is dedicated to testing the [suggested modifications](https://docs.google.com/document/d/1bPODHowsJtEkI8z8GQJKoywU9EWALt_d2ldMNvqA0hM/edit?tab=t.0#heading=h.f8q281dn4opv) to Camtrap DP by the bioacoustic community. We aim to evaluate these changes by mapping datasets to Camtrap DP.

## Background: Safe and Sound pilot project

The "Safe and Sound" pilot project explored the feasibility of establishing a standard for Passive Acoustic Monitoring (PAM) data, building upon the [Camera Trap Data Package (Camtrap DP)](https://camtrap-dp.tdwg.org/), a community-driven data exchange format for camera trap data.

To better understand the types of data generated and their applications, we invited bioacousticians to contribute datasets and share their specific needs. Simultaneously, we analyzed existing PAM standards and databases to identify what information is captured and how it is structured.

**Our findings revealed that Camtrap DP is well-suited for sharing bioacoustic data within the acoustic community and for publishing datasets to GBIF.** There is no need to develop a separate standard. With a few adaptations, the acoustic standard can be seamlessly integrated into Camtrap DP.

The next phase involves testing how these proposed changes impact the entire data lifecycle—from data production to publication, and ultimately to how the data is consumed and analyzed by various tools.

## Scope of the standard

The standard must take into account the diversity of bioacoustics uses and users.
PAM is applied differently across mediums (air, water, soil) and realms (terrestrial, subterranean, marine, and freshwater). In each realm, various recorders/sensors are used (microphone, geophone, hydrophone). Moreover, the methods applied and habits for analysing the data vary (data collection protocols, algorithms, manual/automatic processing) due to the different constraints of each medium.

The two main aspects of PAM are bioacoustics and ecoacoustics. Bioacoustics focuses on the sounds produced by a single species. It aims to describe the library of sounds associated with the behaviour of the organism studied. Ecoacoustics considers the soundscape as a whole, looking at species composition and including non-biological sounds (geophony and anthrophony).
Therefore, datasets from bioacoustics and ecoacoustics are structured in different ways. Bioacoustics datasets are often fragmented into shorter sequences containing the sound events of interest. Ecoacoustics datasets are generally continuous recordings over a day, month, or year.

From the people collecting data in the field to the final report, professionals with different competencies handle the data. They all have different needs, resources, and skills (technicians, software and hardware developers, data scientists, computer scientists, biologists, ecologists). The metadata that circulates among them should be understandable. Furthermore, at several steps of data processing, this information must be both human- and machine-readable.

## Repo structure

The repository structure is based on [Cookiecutter Data
Science](http://drivendata.github.io/cookiecutter-data-science/). Files
and directories indicated with `GENERATED` should not be edited
manually.

    ├─ README.md                         : Description of this repository
    ├─ LICENSE                           : Repository license
    ├─ .gitignore                        : Files and directories to be ignored by git
    ├─ src
    │   ├─ insectai_to_camtrapdp.Rmd     : Empty source script to copy
    │   └─ project_name                  : Folder per project
    │       └─ insectai_to_camtrapdp.Rmd : Source script per project
    └─ data
        └─ project_name                  : Folder per project
            ├─ raw                       : Source data, input for mapping script
            ├─ interim                   : Intermediate Camtrap DP - GENERATED
            └─ processed                 : Final Camtrap DP - GENERATED

## How to contribute

This repository is open to contributions from the community. If you have a bioacoustic dataset that you would like to map to Camtrap DP, please follow the guidelines below.

1.  Create a branch for your project.
2.  Create a folder in `src` with the name of your project.
3.  Copy the `acoustic_to_camtrapdp.Rmd` file to your project folder.
4.  Create a folder in `data` with the name of your project.
5.  Copy your raw data to the `raw` folder.
6.  Edit the `acoustic_to_camtrapdp.Rmd` file to include your project-specific code.
7.  Run `acoustic_to_camtrapdp.Rmd` to generate the Camtrap DP iles.
8.  Throughout all the previous steps: commit your changes and push to your branch. You don’t need to wait to commit until your finished.
9.  Create a pull request to merge your changes into the main branch.

## Relevant sources

- [Camtrap DP - documentation website](https://camtrap-dp.tdwg.org/)
- [Camtrap DP - Github](https://github.com/tdwg/camtrap-dp)
- [Safe and soud](https://wildlabs.net/discussion/safe-and-sound-standard-bioacoustic-data)
- [Summary report](https://docs.google.com/document/d/1bPODHowsJtEkI8z8GQJKoywU9EWALt_d2ldMNvqA0hM/edit?tab=t.0#heading=h.7z7cgy7v2giy)
- [Collection of use-cases](https://docs.google.com/document/d/14xhtmahleHlPPDMSNpRm6TkHq8AbuOOsLqTUNjYI2zA/edit?tab=t.qocym0lvapag#heading=h.avhlbhurvh3v)
- Comment and reply to comments in the working document [Suggested Camtrap DP changes](https://docs.google.com/document/d/17qTjZdw8ohqfK0lSH9DPCXiJcSqSAeFRyUdWcYCdwRc/edit?tab=t.0)
- [Mapping InsectAI data to Camtrap DP](https://github.com/camera-traps/insectai)

## Webinar

In this webinar, we present an acoustic extension of Camtrap DP and outline the plan for further development of the standard. Participants will be invited to join the discussion.

📅 5 Jun 2025 4:00 pm ~ 5:00 pm CEST (UTC +2)

🎥 Recording available

📝 [Register](https://wildlabs.net/event/standard-bioacoustic-data-safe-and-sound)


# Contacts

sanne.govaert@inbo.be

julia.wiel@nina.no



This work is carried out under the auspices of the Boring Fund 2024 with funding from WILDLABS and Arm Ltd.
