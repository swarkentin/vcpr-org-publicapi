# VCPR-ORG Public API
This public repository holds the [OpenAPI](https://github.com/OAI/OpenAPI-Specification) specification (currently **draft** status) for our public API for the management of veterinary treatment protocols.
You can view documentation generated from this spec at [http://api.vcpr.org](http://api.vcpr.org)

[Veterinary Protocol Manager:tm:](https://vcpr.org) provides apps that allow veterinarians to design and prescribe treatment protocols for their clients. Accounts are only available to veterinarians, but the public API described here allows third party developers to incorporate services to receive prescriptions and manage cases.

Funded by an SBIR grant from USDA-NIFA <img src="https://github.com/VCPR-ORG/publicAPI/blob/develop/assets/nifa_transparent.png" width="150">

## Usage Notes
- Endpoint `tags` indicate  which general class(es) of users are authorized for that endppoint, though there are often additional restrictions and SAOR admins have access to all endpoints. Restrictions include, for example, limiting data that is accessible through an endpoint to a subset marked as accessible to a specific user.


