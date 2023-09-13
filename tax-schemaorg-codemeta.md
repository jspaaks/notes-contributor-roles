# schema.org / CodeMeta

Probably fixable with Role "decorator" irrespective of what CFF ends up using: https://github.com/citation-file-format/cffconvert/issues/366

Note that CodeMeta 3.0 defines a list of suggested `roleName`s to be used within the `Role` context. I could not find a description of these terms BTW, but here they are:

|     | CodeMeta term   | note                                                                                                                                                    |
| --- | ---             | ---                                                                                                                                                     |
| 1.  | `Design`        | CodeMeta themselves annote this with "algorithm", I assume to exclude things like graphical design                                                      |
| 2.  | `Architecture`  |                                                                                                                                                         |
| 3.  | `Debugging`     | I assume this means working on fixing a bug that has been reported or is otherwise known                                                                |
| 4.  | `Maintenance`   |                                                                                                                                                         |
| 5.  | `Coding`        |                                                                                                                                                         |
| 6.  | `Documentation` |                                                                                                                                                         |
| 7.  | `Testing`       |                                                                                                                                                         |
| 8.  | `Support`       | I assume this is contributors providing support to others about the software, as opposed to contributors arranging support to sustain the project.      |
| 9.  | `Management`    |                                                                                                                                                         |

From: https://github.com/cdemeta/blob/19a4de2deb55ab7c907984bc9333f45eb5f50412/properties_description.csv#L61

Notes:

1. I'm not sure that CodeMeta 3.0 is considered "released" despite there being a GitHub release.
