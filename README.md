# Bioacoustics

## Mapping bioacoustic datasets to Camtrap DP

This repository is dedicated to **testing** the suggested modifications ([Wiel et al. 2026](https://hdl.handle.net/11250/5343743)) to [Camera Trap Data Package (Camtrap DP)](https://camtrap-dp.tdwg.org/) by the bioacoustic community. We aim to evaluate these changes by mapping datasets to Camtrap DP.

All proposed suggestions are logged as issues in the [Camtrap DP repository](https://github.com/tdwg/camtrap-dp/milestone/4), where the standard is maintained.

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

    ├─ README.md                                 : Description of this repository
    ├─ LICENSE                                   : Repository license
    ├─ .gitignore                                : Files and directories to be ignored by git
    └── datasets
        └── project_name                         : Folder per project
            ├─ src
            │   └─ acoustic_to_camtrapdp.Rmd     : Source script
            └─ data
                ├─ raw                           : Source data, input for mapping script
                ├─ interim                       : Intermediate Camtrap DP - GENERATED
                └─ processed                     : Final Camtrap DP - GENERATED
        

## How to contribute

This repository is open to contributions from the community. 

### Map a bioacoustic dataset to Camtrap DP

If you have a bioacoustic dataset that you would like to map to Camtrap DP, please follow the guidelines below.

1.  Create a fork for your project.
2.  Create a folder in `datasets` with the name of your project. Follow the repo structure.
3.  Create a pull request to merge your changes into the main branch.

If you map your data in `R`, you can make use of the template:
1.  Copy the `acoustic_to_camtrapdp.Rmd` file to your project folder.
2.  Edit the `acoustic_to_camtrapdp.Rmd` file to include your project-specific code.
3.  Run `acoustic_to_camtrapdp.Rmd` to generate the Camtrap DP files.
4.  Throughout all the previous steps: commit your changes and push to your branch. You don’t need to wait to commit until you're finished.

### Help shape the standard

Updates to Camtrap DP are still under discussion and have not been finalized. These discussions take place in the [Camtrap DP repository](https://github.com/tdwg/camtrap-dp). You can share feedback in the [Camtrap DP milestone issues](https://github.com/tdwg/camtrap-dp/milestone/4) or [open a new issue](https://github.com/tdwg/camtrap-dp/issues/new).

## Relevant sources

- [Camtrap DP - documentation website](https://camtrap-dp.tdwg.org/)
- [Camtrap DP - GitHub](https://github.com/tdwg/camtrap-dp)
- [Safe and Sound Summary report](https://hdl.handle.net/11250/5343743)
- [Recording Wildlabs webinar: A standard for bioacoustic data - Safe and Sound](https://wildlabs.net/en/event/standard-bioacoustic-data-safe-and-sound)
- [Wildlabs discussion - Safe and soud](https://wildlabs.net/discussion/safe-and-sound-standard-bioacoustic-data)
- [Collection of use-cases](https://docs.google.com/document/d/14xhtmahleHlPPDMSNpRm6TkHq8AbuOOsLqTUNjYI2zA/edit?tab=t.qocym0lvapag#heading=h.avhlbhurvh3v)
- [Mapping InsectAI data to Camtrap DP](https://github.com/camera-traps/insectai)


# Contacts

sanne.govaert@inbo.be

julia.wiel@nina.no



This work is carried out under the auspices of the Boring Fund 2024 with funding from WILDLABS and Arm Ltd.
