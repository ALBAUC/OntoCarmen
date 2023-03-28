# Reglas SPARQL


## CamelliaRequiresMediumSecurityLevel

?sf a :SecurityFeature .
?sf :hasSecurityLevel ?sl .
FILTER (?sl != :MediumSecurityLevel) .

?sf :hasSecurityConstraint ?sc .
?sc a :Cipher .
?sc :typeCipher "Camellia" .

=>
DELETE
?sf :hasSecurityLevel ?sl .

INSERT
?sf :hasSecurityLevel :MediumSecurityLevel .


## ChaCha20RequiresVeryHighSecurityLevel

## AES128GCMRequiresHighSecurityLevel



## ConfidentialityRequiresChannel

?sf a :SecurityFeature .
?sf :hasProperty ?p .
?p :typeProperty "confidentiality" .

FILTER NOT EXISTS {
    ?sf :hasSecurityConstraint ?sc .
    ?sc a :Channel }

=>

INSERT
?ch a :Channel .
?ch :typeChannel "HTTPS" .
?sf :hasSecurityConstraint ?ch 



    


## SSLTSLRequiresCipher

SecurityFeature
- SecurityConstraint
    - Channel = SSLTSL
- SecurityConstraint
    - Cipher



