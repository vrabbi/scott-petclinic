# Accelerator Log

## Options
```json
{
  "enableTekton" : true,
  "gitFQDN" : "github.com",
  "gitUser" : "vrabbi",
  "pipelineName" : "developer-defined-tekton-pipeline",
  "projectName" : "scott-petclinic",
  "repositoryPrefix" : "ghcr.io/vrabbi",
  "tapGuiCondition" : true,
  "teamName" : "team-a"
}
```
## Log
```
┏ engine (Chain)
┃  Info Running Chain(Combo, UniquePath)
┃ ┏ engine.transformations[0] (Combo)
┃ ┃  Info Combo running as Chain(Merge(merge), UniquePath(UseLast))
┃ ┃ engine.transformations[0].merge (Chain)
┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┏ engine.transformations[0].merge.transformations[0] (Merge)
┃ ┃ ┃  Info Running Merge(Combo, Combo, Combo, Combo, Combo, Combo)
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃  Info Combo running as Chain(Include, Exclude)
┃ ┃ ┃ ┃ engine.transformations[0].merge.transformations[0].sources[0].<combo> (Chain)
┃ ┃ ┃ ┃  Info Running Chain(Include, Exclude)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[0].<combo>.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃  Info Will include [**/*]
┃ ┃ ┃ ┃ ┃ Debug .gitignore matched [**/*] -> included
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py matched [**/*] -> included
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh matched [**/*] -> included
┃ ┃ ┃ ┃ ┃ Debug Tiltfile matched [**/*] -> included
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml matched [**/*] -> included
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml matched [**/*] -> included
┃ ┃ ┃ ┃ ┗ Debug config/workload-without-tekton.yaml matched [**/*] -> included
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[0].<combo>.transformations[1] (Exclude)
┃ ┃ ┃ ┃ ┃  Info Will exclude [config/*.yaml, Tiltfile, README.md, catalog-info.yaml]
┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py didn't match [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh didn't match [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ Debug Tiltfile matched [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml matched [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml matched [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> excluded
┃ ┃ ┃ ┗ ┗ Debug config/workload-without-tekton.yaml matched [config/*.yaml, Tiltfile, README.md, catalog-info.yaml] -> excluded
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃  Info Combo running as Chain(Include, Chain(chain))
┃ ┃ ┃ ┃ engine.transformations[0].merge.transformations[0].sources[1].<combo> (Chain)
┃ ┃ ┃ ┃  Info Running Chain(Include, Chain)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[1].<combo>.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃  Info Will include [Tiltfile]
┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ Debug Tiltfile matched [Tiltfile] -> included
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┗ Debug config/workload-without-tekton.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[1].<combo>.transformations[1] (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[1].<combo>.transformations[1].transformations[0] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [tanzu-java-web-app->scott-petclinic]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[1].<combo>.transformations[1].transformations[1] (ReplaceText)
┃ ┃ ┃ ┗ ┗ ┗  Info Will replace [your-registry.io/project->ghcr.io/vrabbi]
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2] (Combo)
┃ ┃ ┃ ┃  Info Condition (#enableTekton) evaluated to true
┃ ┃ ┃ ┃  Info Combo running as Chain(Include, Chain(chain))
┃ ┃ ┃ ┃ engine.transformations[0].merge.transformations[0].sources[2].<combo> (Chain)
┃ ┃ ┃ ┃  Info Condition (#enableTekton) evaluated to true
┃ ┃ ┃ ┃  Info Running Chain(Include, Chain)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃  Info Will include [config/workload-with-tekton.yaml]
┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug Tiltfile didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml matched [config/workload-with-tekton.yaml] -> included
┃ ┃ ┃ ┃ ┗ Debug config/workload-without-tekton.yaml didn't match [config/workload-with-tekton.yaml] -> excluded
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1] (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(RewritePath, ReplaceText, ReplaceText, ReplaceText, ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[0] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┗ Debug Path 'config/workload-with-tekton.yaml' matched '^(?<folder>.*/)?(?<filename>([^/]+?|)(?=(?<ext>\.[^/.]*)?)$)' with groups {ext=.yaml, folder=config/, filename=workload-with-tekton.yaml, g0=config/workload-with-tekton.yaml, g1=config/, g2=workload-with-tekton.yaml, g3=workload-with-tekton.yaml, g4=.yaml} and was rewritten to 'config/workload.yaml'
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [tanzu-java-web-app->scott-petclinic]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [your-registry.io/project->ghcr.io/vrabbi]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[3] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [github.com->github.com]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[4] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [sample-accelerators->vrabbi]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[2].<combo>.transformations[1].transformations[5] (ReplaceText)
┃ ┃ ┃ ┗ ┗ ┗  Info Will replace [developer-defined-tekton-pipeline->developer-defined-te...(truncated)]
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[3] (Combo)
┃ ┃ ┃ ┃  Info Condition (#enableTekton == false) evaluated to false
┃ ┃ ┃ ┗ null ()
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[4] (Combo)
┃ ┃ ┃ ┃  Info Combo running as Chain(Include, Chain(chain))
┃ ┃ ┃ ┃ engine.transformations[0].merge.transformations[0].sources[4].<combo> (Chain)
┃ ┃ ┃ ┃  Info Running Chain(Include, Chain)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[4].<combo>.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃  Info Will include [README.md]
┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┃ Debug Tiltfile didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┗ Debug config/workload-without-tekton.yaml didn't match [README.md] -> excluded
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[4].<combo>.transformations[1] (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(ReplaceText)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[4].<combo>.transformations[1].transformations[0] (ReplaceText)
┃ ┃ ┃ ┗ ┗ ┗  Info Will replace [tanzu-java-web-app->scott-petclinic]
┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[5] (Combo)
┃ ┃ ┃ ┃  Info Combo running as Chain(Include, Chain(chain))
┃ ┃ ┃ ┃ engine.transformations[0].merge.transformations[0].sources[5].<combo> (Chain)
┃ ┃ ┃ ┃  Info Running Chain(Include, Chain)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[5].<combo>.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃  Info Will include [catalog-info.yaml]
┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/tanzu_tilt_extensions.py didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug .tanzu/wait.sh didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug Tiltfile didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ Debug catalog-info.yaml matched [catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ Debug config/workload-with-tekton.yaml didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┗ Debug config/workload-without-tekton.yaml didn't match [catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[5].<combo>.transformations[1] (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(ReplaceText, RewritePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[5].<combo>.transformations[1].transformations[0] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [default-team->team-a, tanzu-java-web-app->scott-petclinic]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].merge.transformations[0].sources[5].<combo>.transformations[1].transformations[1] (RewritePath)
┃ ┃ ┗ ┗ ┗ ┗ Debug Path 'catalog-info.yaml' matched '^(?<folder>.*/)?(?<filename>([^/]+?|)(?=(?<ext>\.[^/.]*)?)$)' with groups {ext=.yaml, folder=null, filename=catalog-info.yaml, g0=catalog-info.yaml, g1=null, g2=catalog-info.yaml, g3=catalog-info.yaml, g4=.yaml} and was rewritten to 'catalog-info.yaml'
┃ ┗ ╺ engine.transformations[0].merge.transformations[1] (UniquePath)
┗ ╺ engine.transformations[1] (UniquePath)
```
