# Recommended project extensions

## 1. Validate rule enforcement

Create an isolated test virtual network, subnet, and low-cost test workload only if budget permits. Associate the NSG with the test subnet or NIC, then verify that the approved source succeeds and another source is denied.

## 2. Use safer administrative access

Compare direct SSH exposure with Azure Bastion, VPN-based administration, private endpoints, and just-in-time VM access. Document the operational and cost tradeoffs.

## 3. Add monitoring evidence

Use supported Azure network monitoring to capture allowed and denied traffic. Redact public IP addresses, subscription IDs, resource IDs, correlation IDs, and tenant information before adding screenshots.

## 4. Convert the configuration to Terraform

Define the resource group, NSG, and security rule as infrastructure as code. Use an input variable for the approved source CIDR, validate that it is appropriately restricted, run security scanning, and review `terraform plan` before deployment.

## 5. Add governance controls

Evaluate an Azure Policy that audits or denies NSG rules exposing SSH or RDP to `0.0.0.0/0`. Document any approved exceptions and their expiration dates.

