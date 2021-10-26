==============
pipeline_utils
==============

This is the entry point for a collection of utilities available as commands:

  - :ref:`deploy_pipeline <deploy_pipeline>`

Usage:

.. code-block:: bash

    pipeline_utils [COMMAND] [ARGS]

.. _deploy_pipeline:

deploy_pipeline
+++++++++++++++

Utility to automatically deploy a pipeline.

Usage:

.. code-block:: bash

    pipeline_utils deploy_pipeline --ff-env FF_ENV --repos REPOS [REPOS ...] [OPTIONAL ARGS]

Arguments:

--ff-env FF_ENV       environment to use for deployment
--repos REPOS [REPOS ...]
                      list of repos to deploy, must follow expected
                      structure (see docs)

Optional Arguments:

--keydicts-json KEYDICTS_JSON
                      path to file with key dicts for portal auth in json
                      format
--cwl-bucket CWL_BUCKET
                      cwl-bucket to use for deployment
--account ACCOUNT     account to use for deployment
--region REGION       region to use for deployment
--project-uuid PROJECT_UUID
                      uuid for project to use for deployment
--institution-uuid INSTITUTION_UUID
                      uuid for institution to use for deployment
--post-software       post | patch Software objects
--post-file-format    post | patch FileFormat objects
--post-file-reference
                      post | patch FileReference objects
--post-workflow       post | patch Workflow objects
--post-metaworkflow   post | patch MetaWorkflow objects
--post-cwl            upload cwl files
--post-ecr            create docker images and push to ECR
--del-prev-version    delete previous versions information