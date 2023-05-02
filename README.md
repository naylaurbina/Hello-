# Docs for the Azure Web Apps Deploy action: https://github.com/Azure/webapps-deploy

# More GitHub Actions for Azure: https://github.com/Azure/actions

 

#CMST385

#Deploy HTML Files to AppService - Principles of Web Design and Technology

name: Deploy HTML Files to AppService - CMST385

on:

  push:

     branches:

      - main

jobs:

  build-and-deploy:

    runs-on: windows-latest

     steps:

      uses: actions/checkout@main

    - name: Deploy to Azure Web App

      uses: azure/webapps-deploy@v1

      with:

       app-name: CMST385-murbinalizama

                  slot-name: 'production'

     # publish-profile: ${{ secrets.AppServiceCMST385 }}
