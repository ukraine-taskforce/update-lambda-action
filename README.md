# update-lambda-action
## Usage
### With assuming an IAM Role (preferred)
```yml
      - uses: ukraine-taskforce/update-lambda-action@v0.0.1
        with:
          lambda-dir: ${{ env.LAMBDA_DIR }}/${{ matrix.lambda }}
          lambda-name: ${{ env.LAMBDA_NAME }}
          s3-bucket: ${{ env.S3_BUCKET }}
          s3-key: ${{ matrix.lambda }}.zip
          role-arn: ${{ secrets.DEPLOY_ROLE_ARN }}
```
### With AWS Access Keys
```yml
      - uses: ukraine-taskforce/update-lambda-action@v0.0.1
        with:
          lambda-dir: ${{ env.LAMBDA_DIR }}/${{ matrix.lambda }}
          lambda-name: ${{ env.LAMBDA_NAME }}
          s3-bucket: ${{ env.S3_BUCKET }}
          s3-key: ${{ matrix.lambda }}.zip
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```
