# The CJAM github pages site

This site is mostly for creating a QA environment for 350org/cjam-client.

Run the site locally with with `jekyll serve`

When you want to add a new test page/embed, make a new file in both /dev and /prod folders, copying the format of the others, and it will show up on the main menu.

## Markdown format for embed pages

[See the cjam-client's main repo for documentation of different embed codes and options.](https://github.com/350org/cjam-client#embedding-options)

```yaml
---
layout: default
title: Enter your Descriptive title here
codes: |
  data-src-show-events-period="past|today|future" # "today,future"
  data-src-lang="en|fr|pt|de|es|ru|tr"            # only one
  data-src-zoom="[zoom level]"                    # e.g. 5
  data-src-latlong="[lat],[long]"
  data-src-search="[location search string]"
  data-src-layers="events,local-groups,regional-hubs,annotations"
  data-src-source="[source code]"
  data-src-referrer="[referrer code]"
  data-src-event-sources="action-kit|action-network|google-sheet"
  data-src-date-range-start="YYYY-MM-DD"
  data-src-date-range-end="YYYY-MM-DD"
  data-src-campaign-names="[campaign-names]"
version: develop # or production
---
Then below, write a text description of what this does. The codes will be printed out below, so no need to duplicate them here.
```

Make sure you add pages to both the `dev` and `prod` folders (there is no automatic way to generate both at once, and anyway you may be testing slightly different options, if options are changing).
