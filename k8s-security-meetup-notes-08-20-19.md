#  Kubernetes Security Best Practices

### Speed and security:
- labels and annotations
	- Allow for faster querying
### Scan for CVs(?)
### k8s best practices
- Always upgrade
	- Make sure your own the latest stable version
	- Keep up to date w/ security an major API announcements
- RBAC
	- Enable Role-Based Access Control
	- Who can access the cluster and what permissions they have
	- Look for `cluster admin`
- Namespaces
	- Think of it as projects / soft boundaries
	- Creating separate namespaces is an important first level of isolation b/w components
- Network policies
	- By default, it's wide open. Everything is talking to everything
	- Network policies allow you to control network access into and out of your containerized applications
	- Make sure your application talks to what it's designed to talk to
	- Specifed in the YAML
- Cluster-wide Pod Security Policy
	- Admission Control
	- eg. you can block privileged mode, host networking, or containers running as root.
- Harden Node Security
	- Ensure the host is secure and configured correctly
	- Control network access to sensitive ports (eg. 10250 & 10255)
	- Minimize admin access to Kubernetes nodes
- Audit Logging
	- Make sure these are enabled in case something happens
	- Monitor for anomalous/unwanted API calls, authorization failures "Forbidden"
	
### Tips
- Adopt a "style guide" for infrastructure
- Automate your infrastructure
- Design for zero-trust
- Adopt consistent abstractions
- Get past default settings (Most people who use k8s don't customize probably b/cuz of the learning curve)

### Contact
- James@stackrox.com
- https://www.stackrox.com
