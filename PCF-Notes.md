[Back to README](README.md)
#### PCF
https://console.run.pivotal.io/

* publish an app using `cf push` which uses `manifest.yml`
* Download and install the Cloud Foundry CLI https://console.run.pivotal.io/tools
* Follow the instructions under **GETTING STARTED**

To get info from terminal use `cf logs soap-add --recent`

`cf target -o "org-name" -s "name-of-space"`

`cf spaces`

<hr>
#### Using Blue-Green Deployment to Reduce Downtime and Risk
https://docs.pivotal.io/pivotalcf/devguide/deploy-apps/blue-green.html

Step 1: Push an App
`cf push Blue -n demo-time`

Step 2: Update App and Push
`cf push Green -n demo-time-temp`

Step 3: Map Original Route to Green
`cf map-route Green example.com -n demo-time`

Step 4: Unmap Route to Blue
`cf unmap-route Blue example.com -n demo-time`

Step 5: Remove Temporary Route to Green

You can now use cf `unmap-route` to remove the route to `demo-time-temp.example.com`. You can also decommission Blue, or keep it in case you need to roll back your changes.

``

``

``

``
