Deletes all the schedule tasks in AWS ECS by an app name prefix passed by $STEP_APP_NAME

wercker.yml:

steps:
    - cashrewards/aws-ecs-delete-all-scheduled-tasks@0.0.9: 
       name: Removing scheduled tasks for $STEP_APP_NAME
       key: $STEP_AWS_ACCESS_KEY_ID
       secret: $STEP_AWS_SECRET_ACCESS_KEY
       region: $STEP_AWS_DEFAULT_REGION
       app-name: $STEP_APP_NAME
