# VCPR-ORG Public API
This public repository holds the [OpenAPI](https://github.com/OAI/OpenAPI-Specification) specification (currently **draft** status) for our public API for the management of veterinary treatment protocols.
You can view documentation generated from this spec at [http://api.vcpr.org](http://api.vcpr.org)

[Veterinary Protocol Manager:tm:](https://vcpr.org) provides apps that allow veterinarians to design and prescribe treatment protocols for their clients. Accounts are only available to veterinarians, but the public API described here allows third party developers to incorporate services to receive prescriptions and manage cases.

Funded by an SBIR grant from USDA-NIFA <img src="https://github.com/VCPR-ORG/publicAPI/blob/develop/assets/nifa_transparent.png" width="150">

# DairyVets-API Documentation Notes
Taking base API docs for improvement

## To Do

fdaSpecies -- should this be an array?

Parameters as array by name (not by in)

check application of proper nouns

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

