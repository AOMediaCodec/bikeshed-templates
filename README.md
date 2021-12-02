# bikeshed-templates

This repository contains templates to create AOM drafts or specifications using [Bikeshed](https://tabatkins.github.io/bikeshed/).


Each Bikeshed file shall start with the following:

```
<pre class='metadata'>
....
</pre>
```

The contents of the above shall have the following lines:

```
Group: AOM
```
This indicates that the spec will use the boilerplates from https://github.com/tabatkins/bikeshed-boilerplate

```
Status: WGA
```
The status can be among the following:
* WGD: for working group draft
* WGA: for approved working group draft
* FD: final deliverable


```
Title: The Best AOM specification ever
```
The title is mandatory


```
Shortname: my-aom-spec

```
The shortname should match the name of the repository in the AOMediaCodec organization of GitHub (e.g. AOMediaCodec/my-aom-spec). It is used to generate some links in the spec (link to the specification itself, link to the issue tracker, ...).


```
Date: 2021-04-30
```
The date should be updated everytime a change is made to the specification.


```
Editor: John Doe, ExampleCompany, jdoe@example-company.com

```
You can have as many `Editor` lines as needed. You may even have `Former Editor` lines.

```
Abstract: This is the spec abstract
```
A short description of what the spec is about.


Additional headers of the spec can be added by adding lines preceded with `!` for example:

```
!Previously approved version: <a href="v1.0.0.html">v1.0.0</a>
```

Special case for Final deliverable: the BS file must include:
```
Text Macro: SPECVERSION vX.Y.Z

```
This documents the version of the version of the spec. Any text can be used ("-errata 1", ...)


If you have bibliographic references that are not in specref.org you may include additional references directly in your Bikeshed file such as:
```
<pre class='biblio'>
{
    "MyRef": {
	  "href": "https://example.org/",
	  "id": "MyRef",
	  "title": "Some other specification",
	  "publisher": "Someone"
    }
}
</pre>

```

You may define terms that will be automatically to external specifications using the following syntax:
```
<pre class="anchors">
url: http://somereference.example.org; spec: Some_Reference; type: dfn;
    text: one term
    text: another_term
    text: yet another one
```

