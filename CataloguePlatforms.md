# Catalogue of Platforms that facilitate Open Science Software

## Development

Open, colaborative development is typically facilitated by
_source code management (SCM)_ tools, which typically also
bundle _issue/task tracking_ and
_continuous integration/continuous deployment (CI/CD)_
features.

Organizations may self-host an SCM, Issue tracking, CI/CD suite
or may rely on public managed services.

Examples of open-source suites for self-hosting include:
- GitLab, https://about.gitlab.com
- Kallithea, self-hosted only: https://kallithea-scm.org

Examples of public managed services include:
- GitLab: https://about.gitlab.com
- GitHub: https://github.com
- Bitbucket: https://bitbucket.org
- GNU Savannah, only for GPL-licensed projects:
  https://savannah.gnu.org


## Preservation

We consider two aspects of software preservation: on the one hand
preserving the source code of the software as a text that can be
inspected, copied from, and re-used in different projects;
and on the other hand preseving the software as a complete tool
that can be executed to reproduce results.

### Source code

Preseving the source code without the requirement that it can be
compiled and executed is not unlike preserving and other binary data:
the source code needs to be made available at a persistent repository,
ideally with versioning, with the guarantee that the same
software/version identifier will always refer to the exact same source
code.

This fuctionality can, to some extend, be offered by SCM systems
themselves as they serve tarballs of tagged versions. However,
repository tags are revokable and the same tag can be made to point to
a different point in the repository's history; furthermore
repositories can be renamed, moved to a different SCM service, or
removed altogether. For these reasons, it is advisable that source
code tarballs of specific importance (e.g., the version used to
process data and derive published results) are also deposited at a
repository of the same kind as those used for articles or datasets.

Again, these can be either self-hosted at an organization or public
managed services. Some of the latter (like Zenodo) have the advantage
that they refuse to take down or alter artefacts once they have been
published and assigned a persistent identifier.

Examples of open-source suites for self-hosting include:
- DSpace: https://github.com/DSpace  
- Invenio, the software used for Zenodo:
  https://github.com/inveniosoftware
- CKAN: https://github.com/ckan
- Dataverse: https://github.com/IQSS/dataverse 
- Software Heritage: https://github.com/SoftwareHeritage 

Examples of managed services include:
- Zenodo public service: https://zenodo.org
- Software Heritage: https://softwareheritage.org
- Academic publishers that offer the option to archive
  supplementary material


### Executable Software

Software depends on its build environment (kernel, libraries,
compiler), and as the environment evolves software must be maintained
or it will soon become impossible to build and execute.

There are various efforts to create dependency-free packages of the
complete environment so that unmaintained software can be executed in
virtualized copies of obsolete environments.

Examples include lightweight virtualization environments of varying
specificity:
- Python Virtual Environments bundle all dependencies either as
  references or as downloaded and installed environments that
  no longer rely on PyPI:
  https://docs.python.org/3/library/venv.html
- Reana, for porting applications for the usual scientific workflow
  managers (CWL, snakemake) to the usual K8s/Docker/Ceph Cloud
  environment: https://www.reana.io
- Docker containers for virtualizing Linux-based build and execution
  environments: https://docker.com

Naturally, all these depend on some minimal maintenance, as the core
environment (Python installation, Linux kernal, etc.) is not bundled.
The most future-proof option is to archive disk images of
Virtual Machines that contain the complete environment of the
software, although even this depends on the existence of hypervisors
that are able to create appliances (VMs) from the specific image
format.
  


**Publishing**  
- OJS: https://github.com/pkp/ojs
- EpiSciences: https://github.com/CCSDForge/episciences  

**Management**
- Plans
  - Software Management Plan: https://biohackrxiv.org/k8znb/ (an implementation available through the SMW https://smw.ds-wizard.org/)
- Platforms
  - RO-Hub: https://github.com/rohub 

**Registry**
- bio.tools: https://bio.tools/
- WorkflowHub: https://workflowhub.eu/

**Infrastructures**
- JupyterLabs: https://github.com/jupyterlab/jupyterlab
- helix: https://hellenicdataservice.gr/main/


**Processing & Analysis**  
- Jupyter Notebooks: https://github.com/jupyter/notebook 
- OpenRefine:https://github.com/OpenRefine/OpenRefine 
- Amnesia: https://github.com/dTsitsigkos/Amnesia 

**Assessing**  
- FAIR
  - Software Observatory: https://openebench.bsc.es/observatory/
  - FAIR Maturity Model: https://github.com/rd-alliance/FAIR-data-maturity-model-WG 
  - F-UJI: https://github.com/pangaea-data-publisher/fuji 
  - FAIR Evaluator: https://github.com/FAIRsharing/FAIR-Evaluator-FrontEnd 

- Impact
  - Bip!Finder: https://github.com/schatzopoulos/bip-finder-api 

**Assigning Persistent Identifiers**  
- Datacite / DOI: https://github.com/datacite 
- ORCID: https://github.com/ORCID/ORCID-Source 
- Handle: https://www.handle.net/hnr_documentation.html 

**Using Controlled vocabularies**  
- Schema.org: https://github.com/schemaorg/schemaorg 
- Metadata: https://github.com/rd-alliance/metadata-catalog-v2 

**Licensing**  
- Software Package Data Exchange (SPDX): https://spdx.dev/
- LCT: https://lct.ni4os.eu 
