AU Realm FHIR implementation guide projects are required to follow specific publishing guidelines:
- **SHOULD** use AU Core profiles
- **SHOULD** use AU Base profiles and extensions

If a FHIR implementation guide cannot comply with an AU Core profile or reuse an AU Base extension, or fails to comply with an AU Base profile, it must document the variance.

The Variance Statement identifies where an AU Realm FHIR implementation guide does not meet the expectations set by AU Base and/or AU Core. It also identifies resources not profiled in AU Base or AU Core, facilitating the FHIR Work Group's assessment for potential further development. Additionally, the Variance Statement page indicates where the AU Realm FHIR IG fully complies with AU Base or AU Core.

The Variance Statement undergoes review and assessment by the FHIR Work Group as part of the FHIR IG balloting process. For more details on the requirements of a Variance Statement, refer to [AU FHIR IG Variance Requirements](https://confluence.hl7.org/display/HA/Process%3A++AU+FHIR+IG+Variance+Requirements).

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
