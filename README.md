Tack för din feedback! Nedan hittar du den uppdaterade README-filen:

---

# oppna

**oppna** is a service designed to quickly provide developers with a new Kubernetes cluster. Created in Sweden by the founders of the Open School Platform, it offers a simple and efficient solution for creating, scaling, and managing Kubernetes clusters.

## Getting Started

To create a new k3s cluster, simply use the following command:

```bash
npx oppna create cluster
```

The system will generate a new cluster and provide you with a kubeconfig to connect to your cluster. You will see an output similar to the following:

```bash
Creating your Kubernetes cluster...
Cluster created successfully!
IP Addresses: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
DNS Name: hopeful-diamond.oppna.se
Please use the following command to connect to your cluster:
npx oppna cluster config
```

You can now connect to your cluster using the generated kubeconfig. For example, to run a pod with the Ubuntu image and get a shell, use:

```bash
npx oppna run -it pod --image=ubuntu
```

You will see an output similar to this:

```bash
Creating pod with Ubuntu image...
Pod created successfully. Now entering the shell:
root@ubuntu-pod:~#
```

To scale your cluster up or down to a minimum of three nodes, use:

```bash
npx oppna cluster scale --workers=4
```

## Why oppna?

Oppna is designed to be user-friendly and removes the hassle of managing servers and clusters. The service is hosted in Sweden/EU, ensuring compatibility with EU data laws.

Similar to Vercel's model, oppna allows you to share your project with colleagues with a simple command in your repository for a straightforward monthly cost.

The first 14 days are free when you sign in with BankID. After the trial period, the cost is 300 SEK per node per month, or 900 SEK per month for a basic cluster with three small nodes.

## Requirements

To use oppna, you will need to have [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed. Additionally, you will need an SSH key for login and BankID for authentication.

## Support and Contributions

If you encounter any issues or have questions, please don't hesitate to create an issue on GitHub. We also welcome contributions to the project.
