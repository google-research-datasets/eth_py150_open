# eth_py150_open
A redistributable subset of the ETH Py150 corpus [https://www.sri.inf.ethz.ch/py150], introduced in the ICML 2020 paper 'Learning and Evaluating Contextual Embedding of Source Code' [https://proceedings.icml.cc/static/paper_files/icml/2020/5401-Paper.pdf].

This release only makes available a manifest that selects some of the files in
the original ETH Py150 corpus. The manifest was composed by tracking down the
license of each included GitHub repository, and selecting only the files from
those repositories with one of the following licenses:

* 'apache-2.0',
* 'lgpl-2.1',
* 'epl-1.0',
* 'isc',
* 'bsd-3-clause',
* 'bsd-2-clause',
* 'mit',
* 'gpl-2.0',
* 'cc0-1.0',
* 'lgpl-3.0',
* 'mpl-2.0',
* 'unlicense',
* 'gpl-3.0'

We have excluded files from repositories that no longer appear in public GitHub,
that have licenses that do not appear in this license list, that
mix licenses, or that apply the license incorrectly.

We provide 3 JSON-formatted manifest files, one for each split (`dev`, `eval`,
and `train`). The `dev` and `train` splits correspond to the `train` split of
the original ETH Py150 corpus, and is a 90--10 split by file. If no validation
split is required, users may combine the `dev` and `train` splits into a single
`train` split.

Each manifest is a list of file specifications with the following fields:
* `filepath`: string; the full path (within GitHub) of a file retained from the original ETH Py150 Dataset.
* `license`: string (one of 'apache-2.0', 'lgpl-2.1', 'epl-1.0', 'isc', 'bsd-3-clause', 'bsd-2-clause', 'mit', 'gpl-2.0', 'cc0-1.0', 'lgpl-3.0', 'mpl-2.0', 'unlicense', 'gpl-3.0'); the license under which the file was released on GitHub.

To use this manifest, one may download the ETH Py150 repository from its
original location, and then retain only the files with the file paths included
in the corresponding manifest we release.

The sizes of three splits are as follows:
| Dataset split | Number of source files |
| :-------------: | ----------------------: |
| `dev`         | 8302 |
| `train`       | 74749 |
| `eval`        | 41457 |


