# Cloud Load Test Client
Cloud Load Test Client to trigger and import load test run results

1. Build the solution in VS
2. Update the CloudLoadTestingClient.exe.config (present in MainClient/bin/Debug or MainClient/bin/Release) to update the following settings:

        <add key="ElsOnlineAccountUrl" value="https://{VsoAccountProdAccount}.vsclt.visualstudio.com" />
        <add key="VSOnlineAccountPersonalAccessToken" value="{YourPersonalAccessToken}" />

3. Run the following command to download the results:

   CloudLoadTestingClient.exe /downloadresult <YourRunId>
4. The location of the results file (ltrar) would be output. Import this into the load test results store.
