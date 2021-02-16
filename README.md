# cloud-blueprints
Cloud Computing Blueprints

```bash
docker run -it -p7474:7474 -p7687:7687 -v $(PWD)/cloud-taxonomy/taxonomy:/home/ymlgraph/taxonomy -v $(PWD)/blueprints:/home/ymlgraph/blueprints -v $(PWD)/report:/home/ymlgraph/report nextmetaphor/yaml-graph

yaml-graph load -s taxonomy -s blueprints
```