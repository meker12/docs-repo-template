# Contributor guidelines

**Note::** 
   To use this template, view source and make the following updates or replacements:
   
   - Replace ``{{repo.name}}`` with the name you assigned to the repo.
   - Replace or delete {{folder.name}}
   
     The ``{{folder.name}}`` variable appears in links to the content files in the repo. If your repo contains more than one Sphinx project, for example content for v1 and v2 of an API, the content goes in separate folders inside the api-docs folder. In this case, update the folder.name to point to the current version. If you only have one version, delete the following pattern ``{{folder.name}}\``.  If the repo has more than one version, link to the current version, and add a 
     note to the project description guide that points to the folder for the older version. If one of the versions, is in beta or early release, indicate that in the note.



These guidelines provide the general process for maintaining source code that
builds the Rackspace {{product-name}} developer documentation.

- [Project description](#project-description)
- [Updating and adding content](#updating-and-adding-content)
- [General style guidelines](#general-style-guidelines)
- [Submitting your content](#submitting-changes)
- [Previewing changes](#previewing-changes)

##Project description
<!-- Provide as little or as much information about architecture as needed to help
contributors figure out which file to update.-->

This project is developed and built by using the
[Python Sphinx documentation generator](http://sphinx-doc.org/). Content is
written in [reStructuredText](http://sphinx-doc.org/rest.html), which is the
markup syntax and parser component of
[Python Docutils](http://docutils.sourceforge.net/index.html).

Source files for the Sphinx documentation project are in the ``api-docs``
directory. Following are the key files that define project and content
architecture:

**Note::** Fon new projects, update the source for this table with the information for your project. Replace {{repo-name}} with the name of your repo. If you have multiple Sphinx doc projects in the same repo, replace {{folder-name}} with the name of the project folder. You'll also need to add information for both projects in this contributing document.  If you only have one project in the ``api-docs`` folder, remove {{folder-name}}/ from the source file target URL.

Content | File
--- | ---
|Index page for the main content structure| [index.rst](https://github.com/rackerlabs/{{repo.name}}/blob/master/api-docs/{{folder-name}}/index.rst)
|Getting Started index| [getting-started/index.rst](https://github.com/rackerlabs/{{repo-name}}/blob/master/api-docs/{{folder-name}}/getting-started/index.rst.rst)
|General API information index|[general-api-info/index.rst](https://github.com/rackerlabs/{{repo-name}}/blob/master/api-docs/{{folder-name}}/general-api-info/index.rst)
|API Reference index|[api-reference/index.rst](https://github.com/rackerlabs/{{repo-name}}/blob/master/api-docs/{{folder-name}}/api-reference/index.rst)
|API operations methods, including code samples|[api-reference/methods](https://github.com/rackerlabs/{{repo-name}}/tree/master/api-docs/{{folder-name}}/api-reference/methods)
|Release notes index|[release-notes/index.rst](https://github.com/rackerlabs/{{repo-name}}/blob/master/api-docs/{{folder-name}}/release-notes/index.rst)
|Sphinx documentation configuration file| [conf.py](https://github.com/rackerlabs/{{repo-name}}/blob/master/api-docs/{{folder-name}}/conf.py) (For new projects, replace the following values in the conf.py with values for your API project: ``product``= name of the API service, ``v#``= contract version, ``v#.r#``= ``release number``)
|Linux and OS X build script|``Makefile``|
|Windows build script|``make.bat``|
|Install requirements for building locally|[requirements.txt](https://github.com/rackerlabs/docs-common/blob/master/requirements.txt)


## Updating and adding content

Contributions are submitted, reviewed, and accepted by using GitHub pull
requests, following the [GitHub workflow](GITHUBING.md) for this repository.

To update existing source files or add new ones, follow the
[GitHub workflow](GITHUBING.md) for this repository.

* Update source files by using the GitHub editor or any plain text editor.
* Format source files with
  [reStructuredText syntax](http://www.sphinx-doc.org/en/stable/rest.html).
* For quick syntax checking, try the
[Online reStructuredText editor](http://rst.ninjs.org/).

## General style guidelines

When you add or update content, use the following general style guidelines,
which are described in detail in [Style guidelines for technical content]( \
https://github.com/rackerlabs/docs-rackspace/tree/master/style-guide):

- Use [sentence-style capitalization](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/a-l-style-guidelines.md#cap-sentence-style) for titles and headings
- Use consistent [text formatting](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/m-z-style-guidelines.md#text-formatting)
- Write clear and consistent [code examples](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/a-l-style-guidelines.md#code-examples)
- Use [active voice](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#use-active-voice)
- Use [present tense](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#use-present-tense)
- Write to the user by using [second person and imperative mood](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#write-to-user)
- Write clear and consistent [step text](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/m-z-style-guidelines.md#tasks-steps)
- Clarify [pronouns](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#clarify-pronouns) such as *it*, *this*, *there*, and *that*
- Clarify [gerunds and participles](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#clarify-gerunds-and-participles)
- Use [consistent terminology](https://github.com/rackerlabs/docs-rackspace/blob/master/style-guide/basic-writing-guidelines.md#use-consistent-terminology)

<!-- Adding build from source guidelines until we can provide a link to
automated gh-pages output, or to the staging URL that Ash is working on.
-->

# Submitting changes

When you've completed your changes, submit a pull request. Someone on the
Information Development team will review your PR.
- Minor updates and corrections get a quick review to ensure that content is
  error-free and doesn't introduce other issues.
- More complex changes or additions require both technical and editorial review.

Depending on the review feedback, you might be asked to make additional changes.

After content has been reviewed and approved, the updates can be merged to the
master branch. The merge triggers the build and deploy process. Typically, new
content is available on developer.rackspace.com within a minute or two after it
is merged. Larger updates might take a bit longer.

## Previewing changes

When you submit a pull request, the Strider build process creates a preview of
your changes in a staging environment. After the build process completes, the
following message displays in the pull request comments with a link to the
content: ``Your content preview is now ready.``

You can also build the project locally using the [Sphinx documentation
generator](http://sphinx-doc.org/). For details, see
[Building from source](https://github.com/rackerlabs/docs-rackspace/blob/master/doc/tools/build-from-source.rst).
