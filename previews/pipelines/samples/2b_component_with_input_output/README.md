
This is a component that has inputs and outputs with the corresponding pipeline job. 

```
# az ml job create --file pipeline.yml
Command group 'ml job' is experimental and under development. Reference and support levels: https://aka.ms/CLI_refstatus
Uploading data:   0%|                                                                                                   | 0.00/500 [00:00<?, ?B/s]
Uploading src:   0%|                                                                                                  | 0.00/1.02k [00:00<?, ?B/s]
Custom pipeline job names are not supported yet. Please refer to the created pipeline job using the name: 029c2422-d403-4194-bdeb-78967cfca623
creation_context:
  created_at: '2021-09-28T23:28:33.457700+00:00'
  created_by: Joe Zhou
  created_by_type: User
description: Component with inputs and outputs
display_name: hungry_papaya_qxlhs7cy
experiment_name: 2b_component_with_input_output
id: azureml:/subscriptions/<sub-id>/resourceGroups/<resource-group-name>/providers/Microsoft.MachineLearningServices/workspaces/<ws-name>/jobs/ccde1727-c8b0-4daa-9ebc-c1312f16a60c
inputs:
  pipeline_sample_input_data:
    dataset: azureml:a4727c11-4ff4-4409-8c4f-0f1510e9c118
    mode: ro_mount
jobs:
  hello_python_world_job:
    component: azureml:a1b3366d-2f84-424d-8a82-173c24013783:1
    compute: azureml:cpu-cluster
    inputs:
      sample_input_data: ${{inputs.pipeline_sample_input_data}}
    outputs:
      sample_output_data: ${{outputs.pipeline_sample_output_data}}
    overrides: {}
    type: component
name: ccde1727-c8b0-4daa-9ebc-c1312f16a60c
outputs:
  default:
    mode: rw_mount
  pipeline_sample_output_data:
    mode: upload
properties:
  azureml.git.dirty: 'True'
  azureml.parameters: '{}'
  azureml.pipelineComponent: pipelinerun
  azureml.runsource: azureml.PipelineRun
  mlflow.source.git.branch: main
  mlflow.source.git.commit: d6abde2eaa9b9d996bcb2b18e391e7f62fed4a11
  mlflow.source.git.repoURL: https://github.com/Azure/azureml-previews
  runSource: MFE
  runType: HTTP
resourceGroup: <resource-group-name>
services:
  Studio:
    endpoint: https://ml.azure.com/runs/ccde1727-c8b0-4daa-9ebc-c1312f16a60c?wsid=/subscriptions/<sub-id>/resourcegroups/<resource-group-name>/workspaces/<ws-name>&tid=72f988bf-86f1-41af-91ab-2d7cd011db47
    job_service_type: Studio
  Tracking:
    endpoint: azureml://master.api.azureml-test.ms/mlflow/v1.0/subscriptions/<sub-id>/resourceGroups/<resource-group-name>/providers/Microsoft.MachineLearningServices/workspaces/<ws-name>?
    job_service_type: Tracking
settings:
  continue_run_on_step_failure: false
status: Preparing
tags:
  azureml.pipelineComponent: pipelinerun
type: pipeline
```
