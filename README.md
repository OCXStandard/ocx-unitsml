![3DOCX.org logo](./docs/_static/logo.png)
# UnitsML XML unit markup schema 

## Introduction 
This schema was [originally developed and published by NIST](https://unitsml.nist.gov/).
The schema is used by the [OCX schema](https://github.com/OCXStandard/OCX_Schema) which is managed by the [OCX Consortium](https://3docx.org).
The UnitsML schema is publihsed by the OCX Consortium under the original [LICENSE](LICENSE).

## Changelog
  * [CHANGELOG.md](CHANGELOG.md)

## Project structure
<pre><code>
Root
└──ocx_unitsml         
   └───ocx_unitsml_0918
</code></pre>

## How to contribute
The schema file is maintained using an XML editor like Altova XMLSpy.
1. Installation: Simply download the schema files from the repository or clone it using git.
2. Create an [Issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue) for the proposed schema change. 
Follow [the recipe on the Wiki](https://github.com/OCXStandard/OCX_Schema/wiki) on how to register an issue.
3. Then create a branch from the issue, check out the branch and implement the proposed changes.
4. When the implementation is completed, create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).
4. The pull request will have to be approved by the [OCXStandard maintainer](https://github.com/orgs/OCXStandard/teams/ocx-schema-team?query=role%3Amaintainer) before it can be included in the working draft.

## Schema versioning
The UnitsML schema is following the Python [PEP 440 versioning recommendations](https://peps.python.org/pep-0440/).

Following PEP 440, the canonical public version identifiers MUST comply with the following scheme:

``
  [N!]N(.N)*[{a|b|rc}N][.postN][.devN]
``
see the [PEP 440](https://peps.python.org/pep-0440/) for a detailed explanation.

## ``tbump`` versioning tool

The Python [``tbump``](https://pypi.org/project/tbump/) tool is used to automate and bump schema versions. ``tbump`` also provides the possibility for pre- and post-commit actions.
The project config file ``pyproject.toml`` contains the tbump settings.

### Usage

Assume that the current schema version is ``0.9.18``. To bump the schema version to a new version  ``1.0.0`` version, the following command can be issued:

<pre><code>
> tbump 1.0.0
:: Bumping from 0.9.18 to 1.0.0
=> Would update current version in pyproject.toml
=> Would patch these files
- pyproject.toml:12 version = "0.9.18"
+ pyproject.toml:12 version = "1.0.0"
- pyproject.toml:31 current = "0.9.18"
+ pyproject.toml:31 current = "1.0.0"
- ocx_unitsml\__init__.py:1 __version__ = '0.9.18'
+ ocx_unitsml\__init__.py:1 __version__ = '1.0.0'
- ocx_unitsml\unitsmlSchema_lite.xsd:44 elementFormDefault="qualified" attributeFormDefault="unqualified" version="0.9.18">
+ ocx_unitsml\unitsmlSchema_lite.xsd:44 elementFormDefault="qualified" attributeFormDefault="unqualified" version="1.0.0">
+ ocx_unitsml\unitsmlSchema_lite.xsd:41 xmlns="urn:oasis:names:tc:unitsml:schema:xsd:UnitsMLSchema_lite-1.0.0"
- ocx_unitsml\unitsmlSchema_lite.xsd:43 targetNamespace="urn:oasis:names:tc:unitsml:schema:xsd:UnitsMLSchema_lite-0.9.18"
+ ocx_unitsml\unitsmlSchema_lite.xsd:43 targetNamespace="urn:oasis:names:tc:unitsml:schema:xsd:UnitsMLSchema_lite-1.0.0"
=> Would run these hooks before commit
* (1/1) $ databinding generate ./ocx_unitsml/unitsmlSchema_lite.xsd ocx_unitsml 1.0.0
$ git add --update
$ git commit --message Bump to 1.0.0
$ git tag --annotate --message v1.0.0 v1.0.0
$ git push --atomic origin main v1.0.0
:: Looking good? (y/N)

</code></pre>


## Schema databinding 
See [DATABINDING.md](DATABINDING.md) 

## Public License
The UnitsML standard is governed by the OASIS Intellectual Property Rights Policy (the License).

[Read the License](LICENSE)

Unless required by applicable law or agreed to in writing, the UnitsML standard and any derivative works re-distributed under the License
is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
The OCX Consortium is not liable to any use whatsoever of the distributed standard or derivative works based on the standard.


# Credits

[NIST](https://unitsml.nist.gov/) for the original schema development and [OASIS UnitsML TC](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=unitsml) for publishing the schema version ```1.0``` in 2011.
