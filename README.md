# Ads

This is a view on how our organization builds out the Amazon Ad tech stack. This layered view with the framework below helps us think through what should be built as shared components versus custom applications. Multiple custom ad products, built on top of common ad tech services.

- Ad Products will own features that are specific to an ad product such as integrations to third party agencies. At times, a feature may originate for a team (e.g. Sponsored Products) and then extended to work for other offerings. In this case, we can either pull it into Ad Tech services or let it continue to run within a team and resource the team to support broader use cases. 
- Ad Tech Services are core advertising components that share most of the functionality across multiple products. The justification to pull something into this layer is either to improve overall organizational velocity and/or improve advertiser experience by way of consistency across products. In the case of attribution and reporting, it is important to the customer experience that we enable a unified view across products. In the case of Targeting, Media management etc., it helps with overall developer velocity.  These components should have the capability to plug in custom modules and metrics.
- Shared capabilities refers to services that are not ad tech specific but need to be solved for the advertising domain in a consistent way. Key examples are: 1) Identity, 2) Billing, 3) Experimentation, and 4)Fraud detection.  (The core component is agnostic to the ad domain but we’ll extend to create a version that supports Ad Tech)
- Core Managed Infrastructure is leveraging Native AWS (and in other cases PROD/MAWS) to provide the technology for persistence, propagation and exploration.

![image](https://github.com/user-attachments/assets/9a7058de-ce20-4cbe-836e-30a66687c168)
