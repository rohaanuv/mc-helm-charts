# mc-helm-charts

helm charts and deployment using Github Actions
## Step 1: Install Gatekeeper
```
helm repo add gatekeeper https://open-policy-agent.github.io/gatekeeper/charts
helm repo update
helm install gatekeeper gatekeeper/gatekeeper --namespace gatekeeper-system --create-namespace
```

## Step 2: Install Constraint Template
```
kubectl apply -f constraintemplates.yaml       
```
## Step 3: Install Constraint

```
kubectl apply -f constraints.yaml       
```

## Step 4: Create a values.yaml 


## Step 5: Install & Apply to create a namespace
```
helm install namespace-governance ./accion-gatekeeper-namespace-policy -f values.yaml

```