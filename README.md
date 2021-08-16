# cloud-blueprints
Cloud Computing Blueprints

```bash
# create a yaml-graph container mounting the report and definition directories
docker run -it -p7474:7474 -p7687:7687 -v $(PWD)/cloud-taxonomy/taxonomy:/home/ymlgraph/taxonomy -v $(PWD)/blueprints:/home/ymlgraph/blueprints -v $(PWD)/report:/home/ymlgraph/report nextmetaphor/yaml-graph

# validate the definitions
yaml-graph validate -s taxonomy -s blueprints -f taxonomy/definition-format.yml 

# load into the graph
yaml-graph load -s taxonomy -s blueprints 

# generate reports

#
yaml-graph report --fields report/fields.yaml --template report/template.gohtml > report/cloud-taxonomy.html

# report by blueprint-category
yaml-graph report --fields report/by-blueprint-category/fields.yaml --template report/by-blueprint-category/template.gohtml > report/by-blueprint-category/by-blueprint-category.html
```