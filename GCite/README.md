# GCite: Graph Enhanced Contextual Citation Dataset
GCite is a contextual citation dataset with different types of citation relationships, categorized by citation position. 
* Our dataset covers 4.8K paper nodes with full texts and connected by 25K citation edges.
* The body texts of one paper are divied into four sections (namely 1. Introduction, 2. Related Work, 3. Method and 4. Experiment) and all the citation position are labeled by the citation contained sectio type.
## papers_withtext schema
```
[
...,
{
  "id": 8,
  "titile": "Title of one paper...",
  "abstract": "Abstract of one paper...",
  "body_text": {
    "1": "Introduction section texts...",
    "2": "Related work section texts...",
    "3": "Method section texts...",
    "4": "Experiment section texts..."
  }
}
...,
]
```
## data schema
```
{
  "src": 8, #index of cited paper
  "dst": 5, #index of citing related work
  "cite_label": 1, #citing position label (1. Citation in Introduction section, 2. Citation in Related Work section, 3. Citation in Method section and 4. Citation in Experiment section)
  "cite_text": "Citation texts..."
}
```
## author2index schema
```
{
  "id": ["authors"]
}
```
## venue2index schema
```
{
  "id": "venue"
}
```
