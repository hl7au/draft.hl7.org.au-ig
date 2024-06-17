<div class="stu-note" markdown="1">
The HL7 Australia FHIR Working Group has introduced a [Proposal: AU Base & AU Core Variance process](https://confluence.hl7.org/pages/viewpage.action?pageId=227217286) that sets expectations for all HL7 AU FHIR implementation guides to:
- be compliant with AU Core profiles. Implementation guides that are unable to comply with AU Base Core profiles are expected to document these variances.
- to be compliant with AU Base profiles and extensions. Implementation guides that are unable to comply with AU Base profiles or reuse AU Base extensions are expected to document these variances.

To be compliant with an AU Core profile implies that the profiles within the downstream implementation guides satisfy the expectations established by AU Core profile. Instances that are valid against the downstream implementation guide profile are automatically valid against the AU Core profile. Compliance expectations are set at profile only support, ensuring systems build and conform to defined profiles for data representation without the requirement to implement AU Core interactions. It is important to note that stating compliance with AU Core profiles does not guarantee full conformance.

To be compliant with AU Base, instances that are valid against downstream implementation guide profiles are, by default, considered compliant with the AU Base profile.

The AU Base and AU Core variance process is currently being developed: [https://confluence.hl7.org/display/HA/**+DRAFT+**+Process%3A++AU+Realm+FHIR+IG+Variance+Requirements](https://confluence.hl7.org/display/HA/**+DRAFT+**+Process%3A++AU+Realm+FHIR+IG+Variance+Requirements). Guidance provided here is subject to change as the process matures.
</div>

### Example: A FHIR IG states no variance from AU Base and AU Core
> #### Variance from AU Base
> This implementation guide has no variance (i.e. fully compliant) from AU Base FHIR Implementation Guide version 4.2.0-preview.  
>
> #### Variance from AU Core
> This implementation guide has no variance (i.e. fully compliant) from AU Core FHIR Implementation Guide version 0.3.0-ballot.  


### Example: A FHIR IG states variance from AU Core
> #### Variance from AU Base
> This implementation guide has no variance (i.e. fully compliant) from AU Base FHIR Implementation Guide version 4.2.0-preview. 
>
> #### Variance from AU Core
> A summary of variances between profiles defined in this implementation guide and profiles defined in AU Core FHIR IG version 0.3.0-ballot:
> - [AU PractitionerRole Profile](practitionerrole-profile.html): Variance from AU Core PractitionerRole.
>   - Cardinality: PractitionerRole.identifier:medicareProvider cardinality is 0..*. Unable to use AU Core PractitionerRole  profile as it supports 0..1 Medicare Provider Number identifier slices.
>   - Removed Must Support: PractitionerRole.location
>
> #### Additionally Profiled Resources
This implementation guide profiles the following resources that are not profiled in AU Core:
>  - [Diagnostic Service Requesting Base](https://build.fhir.org/ig/hl7au/au-fhir-erequesting/branches/scaffold/StructureDefinition-erequesting-diagnostic-request-base.html)
>  - [Diagnostic Service Requesting Pathology](https://build.fhir.org/ig/hl7au/au-fhir-erequesting/branches/scaffold/StructureDefinition-erequesting-diagnosticrequest-pathology.html)
>  - [Diagnostic Service Requesting Radiology](https://build.fhir.org/ig/hl7au/au-fhir-erequesting/branches/scaffold/StructureDefinition-erequesting-diagnosticrequest-radiology.html)
