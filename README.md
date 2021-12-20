# VCPR-ORG Public API
This public repository holds the [OpenAPI](https://github.com/OAI/OpenAPI-Specification) specification (currently **draft** status) for our public API for the management of veterinary treatment protocols.
You can view documentation generated from this spec at [http://api.vcpr.org](http://api.vcpr.org)

[Veterinary Protocol Manager:tm:](https://vcpr.org) provides apps that allow veterinarians to design and prescribe treatment protocols for their clients. Accounts are only available to veterinarians, but the public API described here allows third party developers to incorporate services to receive prescriptions and manage cases.

Funded by an SBIR grant from USDA-NIFA <img src="https://github.com/VCPR-ORG/publicAPI/blob/develop/assets/nifa_transparent.png" width="150">


## To Do

fdaSpecies -- should this be an array?

Parameters as array by name (not by in)

check application of proper nouns

### Security

Not sure if that declaration at line 20 works globally, i.e. may need to apply at each endpoint (see userLogin).

### Tags

May need to extend tags applied.

> Tagging strategy == multiple tags are OK but they need not be exhaustive. For example a Protocol can always contain Promises, so anything with a Protocol tag might also have Promise. Let's only use Promise if an endpoint operates directly on it. Use the most general tag applicable. NB there are proposals for tag nesting, so future OAS versions may have more flexibility.

- name: User
    description: Endpoints and models related to user management.
- name: Prescription
    description: Endpoints and models related to prescription management.
- name: Protocol
    description: Endpoints and models related to protocol management.
- name: Case
    description: Endpoints and models related to case management.
- name: Promise
    description: Endpoints and models related to promise management.

## Style notes

id > ID
user (users) > User (see [proper nouns](proper-nouns))
  Ditto other active components e.g. Prescription??

Endpoint & Security Schema description as sentence (i.e. with stop, starts caps).
  Endpoint starts with "This endpoint ..."

Summary description as fragment (no caps/no stop)

Property description as fragment (no caps (unless [proper noun](proper-nouns))/ no stop)
  UNLESS LONG e.g., duration after last treatment during which some act is prohibited. Most often this restricts when meat or milk may be sold for food.

Error description as sentence: Success with caps as fragment (Success – token refreshed or OK)
rest as per style == no caps & fragment

## Proper nouns / Active components of system

User
Protocol
Diagnosis
Dosage
ID
Prescription
Greenbook Drug
Treatment
Eligibility / Eligibilities
Case
Promise


## Testing

[Mayhem](https://mayhem4api.forallsecure.com/docs/fuzz-your-own.html)

Warning -- construction is right BUT do not hit the production server with this!

mapi run  VCPR1 100 "https://raw.githubusercontent.com/VCPR-ORG/publicAPI/develop/src/openapi.yaml" --url "https://test.VCPR.ORG"   --interactive
