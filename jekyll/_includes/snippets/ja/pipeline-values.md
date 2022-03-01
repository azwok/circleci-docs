| 変数                                      | タイプ   | 値                                                                                                                                                                                                                                                                        |
| --------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `pipeline.id`{:.env_var}                | 文字列型  | パイプラインを表す、[グローバルに一意のID](https://en.wikipedia.org/wiki/Universally_unique_identifier)。                                                                                                                                                                                    |
| `pipeline.number`{:.env_var}            | 整数型   | パイプラインを表す、プロジェクトで一意の整数の ID                                                                                                                                                                                                                                               |
| `pipeline.project.git_url`{:.env_var}   | 文字列型  | 現在のプロジェクトがホストされている URL 。 For example, `https://github.com/circleci/circleci-docs`                                                                                                                                                                                        |
| `pipeline.project.type`{:.env_var}      | 文字列型  | 小文字の VCS プロバイダ名。 例: “github”、“bitbucket”                                                                                                                                                                                                                                 |
| `pipeline.git.tag`                      | 文字列型  | パイプラインをトリガーするためにプッシュされた git タグの名前。 タグでトリガーされたパイプラインでない場合は、文字列は空です。                                                                                                                                                                                                       |
| `pipeline.git.branch`{:.env_var}        | 文字列型  | パイプラインをトリガーするためにプッシュされた git タグの名前。                                                                                                                                                                                                                                       |
| `pipeline.git.revision`{:.env_var}      | 文字列型  | 現在ビルドしている長い git SHA（４０文字）                                                                                                                                                                                                                                                |
| `pipeline.git.base_revision`{:.env_var} | 文字列型  | 現在ビルドしているものより前のビルドの長い git SHA （４０文字） **Note:** While in most cases  `pipeline.git.base_revision` will be the SHA of the pipeline that ran before your currently running pipeline, there are some caveats. ブランチの最初のビルドの場合、変数は表示されません。 また、ビルドが API からトリガーされた場合も変数は表示されません。 |
| `pipeline.in_setup`{:.env_var}          | ブール値型 | True if the pipeline is in the setup phase, i.e. running a [setup workflow]({{ site.baseurl }}/2.0/dynamic-config/).                                                                                                                                                     |
| `pipeline.trigger_source`{:.env_var}    | 文字列型  | The source that triggers the pipeline, current values are `webhook`, `api`, `scheduled_pipeline`                                                                                                                                                                         |
| `pipeline.schedule.name`{:.env_var}     | 文字列型  | The name of the schedule if it is a scheduled pipeline. Value will be empty string if the pipeline is triggerd by other sources                                                                                                                                          |
| `pipeline.schedule.id`{:.env_var}       | 文字列型  | The unique id of the schedule if it is a scheduled pipeline. Value will be empty string if the pipeline is triggerd by other sources                                                                                                                                     |
{: class="table table-striped"}