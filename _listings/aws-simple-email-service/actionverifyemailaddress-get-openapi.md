---
swagger: "2.0"
x-collection-name: AWS Simple Email Service
x-complete: 0
info:
  title: AWS Simple Email Service API Verify Email Address
  version: 1.0.0
  description: Verifies an email address.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetIdentityVerificationAttributes:
    get:
      summary: Get Identity Verification Attributes
      description: Given a list of identities (email addresses and/or domains), returns
        the verification status and (for domain identities) the verification token
        for each identity.
      operationId: getIdentityVerificationAttributes
      x-api-path-slug: actiongetidentityverificationattributes-get
      parameters:
      - in: query
        name: Identities.member.N
        description: A list of identities
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=VerifyDomainDkim:
    get:
      summary: Verify Domain Dkim
      description: Returns a set of DKIM tokens for a domain.
      operationId: verifyDomainDkim
      x-api-path-slug: actionverifydomaindkim-get
      parameters:
      - in: query
        name: Domain
        description: The name of the domain to be verified for Easy DKIM signing
        type: string
      responses:
        200:
          description: OK
      tags:
      - Domains
  /?Action=VerifyDomainIdentity:
    get:
      summary: Verify Domain Identity
      description: Verifies a domain.
      operationId: verifyDomainIdentity
      x-api-path-slug: actionverifydomainidentity-get
      parameters:
      - in: query
        name: Domain
        description: The domain to be verified
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=VerifyEmailAddress:
    get:
      summary: Verify Email Address
      description: Verifies an email address.
      operationId: verifyEmailAddress
      x-api-path-slug: actionverifyemailaddress-get
      parameters:
      - in: query
        name: EmailAddress
        description: The email address to be verified
        type: string
      responses:
        200:
          description: OK
      tags:
      - Email Addresses
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---