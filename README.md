![3DOCX.org logo](./docs/_static/logo.png)
# UnitsML XML unit markup schema 

## Introduction 
This schema was [originally developed and published by NIST](https://unitsml.nist.gov/)
The schema is used by the [OCX schema](https://github.com/OCXStandard/OCX_Schema) managed by the [OCX Consortium](https://3docx.org).

## Changelog
  * [CHANGELOG.md](CHANGELOG.md)


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

</code></pre>


## Naive databinding
A set of Python dataclasses are autogenerated after each version release, see [databindings](databinding.rst)

### Generating databindings

## Public License
The UnitsML standard is governed by the OASIS Intellectual Property Rights Policy (the License).

[Read the License](LICENSE)

[LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, the 3Docx standard and software distributed under the License
is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
The OCX Consortium is not liable to any use whatsoever of the distributed standard or software based on the standard.

See the License for the specific language governing permissions and limitations under the License.

# Credits

[NIST](https://unitsml.nist.gov/) for the original schema development and [OASIS UnitsML TC](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=unitsml) for publishing the schema version ```1.0``` in 2011.
