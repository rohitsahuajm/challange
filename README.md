This code creates a Pod with the name my-pod and sets the replicas value to 3. 
It then defines a template for the Pod that includes three containers, each with a different name (POD A, POD B, and POD C) 
and memory limit (400Mi, 200Mi, and 400Mi, respectively).

The volumeMounts section specifies that each container should mount a volume named 
csv-data at the path /app/data.csv with a subPath of data.csv. This will make the CSV file available 
to each container at the specified path.

The volumes section defines a volume named csv-data that is sourced from a ConfigMap named my-csv. 
You will need to create the my-csv ConfigMap separately and add the CSV file data to it.

ConfigMap named my-csv with a single data item named data.csv..

With these YAML files, you can apply them to your Kubernetes cluster using kubectl apply -f <filename>.yaml command.
