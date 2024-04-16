aws iam help

aws iam create-group --group-name "YOUR_GROUP_NAME"

aws iam create-user --user-name "YOUR_USER_NAME"

aws iam add-user-to-group --user-name "YOUR_USER_NAME" --group-name "YOUR_GROUP_NAME"

aws iam get-group --group-name "YOUR_GROUP_NAME"

aws iam attach-user-policy --user-name "YOUR_USER_NAME" --policy-arn "YOUR_POLICY_ARN"

aws iam list-policies --query `Policies[?PolicyName=="`YOUR_POLICY_NAME`"].Arn` --output text

aws iam attach-group-policy --group-name "YOUR_GROUP_NAME" --policy-arn "YOUR_POLICY_ARN"

aws iam list-attached-group-policies --group-name "YOUR_GROUP_NAME"

aws iam create-login-profile --user-name "YOUR_USER_NAME" --password "YOUR_PASSWORD" --password-reset-required

aws iam get-user --user-name "YOUR_USER_NAME"

aws iam create-policy --policy-name "YOUR_POLICY_NAME" --policy-document "YOUR_FILE_NAME"

aws iam create-access-key --user-name "YOUR_USER_NAME"
