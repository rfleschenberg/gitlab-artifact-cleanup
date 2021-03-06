gitlab-artifact-cleanup
=======================

Currently (as of GitLab 8.12) there are no admin tools for cleaning up
build artifacts (see issue [#18351]). This script erases build artifacts
using the GitLab API.

## Requirements
- [`python-gitlab`] - Python GitLab API client *(At least version 0.16)*
- [`python-dateutil`] - A robust ISO-8601 timestamp parser, among other things
- [`pytz`] - Timezone info *(Only required if you are using Python 2)*

## Usage
This script leverages the [`python-gitlab` config file][python-gitlab-config].
Just like the `gitlab` CLI tool, you can specify a non-default Gitlab server
with the `-g`/`--gitlab` option.

You can specify any number of projects with the `-p`/`--project` option:

    $ gitlab-artifact-cleanup --project jreinhart/artifact-test --project jreinhart/python-gitlab

Or, you can cleanup all projects visible to you:

    $ gitlab-artifact-cleanup --all-projects

Builds for tags are never removed.

## License

This software is released under the [MIT License](https://opensource.org/licenses/MIT).

[#18351]: https://gitlab.com/gitlab-org/gitlab-ce/issues/18351
[d4a24a5c4d]: https://github.com/gpocentek/python-gitlab/commit/d4a24a5c4dc54ac03b917723347047e3995afcc9

[`python-gitlab`]: https://github.com/gpocentek/python-gitlab
[python-gitlab-config]: http://python-gitlab.readthedocs.io/en/stable/cli.html#configuration
[`python-dateutil`]: https://dateutil.readthedocs.io/en/stable/
[`pytz`]: http://pythonhosted.org/pytz/
