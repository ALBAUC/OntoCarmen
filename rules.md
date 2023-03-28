# Rules


## CamelliaRequiresMediumSecurityLevel

DELETE {
  ?sf ontocarmen:hasSecurityLevel ?sl .
}

INSERT {
  ?sf ontocarmen:hasSecurityLevel ontocarmen:MediumSecurityLevel .
}

WHERE{
   ?sf a ontocarmen:SecurityFeature .
   ?sf ontocarmen:hasSecurityLevel ?sl .
   FILTER (?sl != ontocarmen:MediumSecurityLevel) .
   ?sf ontocarmen:hasSecurityConstraint ?sc .
   ?sc a ontocarmen:Cipher .
   ?sc ontocarmen:typeCipher "Camellia" .
}


## ChaCha20RequiresVeryHighSecurityLevel

DELETE {
  ?sf ontocarmen:hasSecurityLevel ?sl .
}

INSERT {
  ?sf ontocarmen:hasSecurityLevel ontocarmen:VeryHighSecurityLevel .
}

WHERE{
   ?sf a ontocarmen:SecurityFeature .
   ?sf ontocarmen:hasSecurityLevel ?sl .
   FILTER (?sl != ontocarmen:VeryHighSecurityLevel) .
   ?sf ontocarmen:hasSecurityConstraint ?sc .
   ?sc a ontocarmen:Cipher .
   ?sc ontocarmen:typeCipher "Camellia" .
}


## AES128GCMRequiresHighSecurityLevel

DELETE {
  ?sf ontocarmen:hasSecurityLevel ?sl .
}

INSERT {
  ?sf ontocarmen:hasSecurityLevel ontocarmen:HighSecurityLevel .
}

WHERE{
   ?sf a ontocarmen:SecurityFeature .
   ?sf ontocarmen:hasSecurityLevel ?sl .
   FILTER (?sl != ontocarmen:HighSecurityLevel) .
   ?sf ontocarmen:hasSecurityConstraint ?sc .
   ?sc a ontocarmen:Cipher .
   ?sc ontocarmen:typeCipher "AES128GCM" .
}


## ConfidentialityRequiresChannel

INSERT {
    ?ch a :Channel .
    ?sf :hasSecurityConstraint ?ch 
}

WHERE {
    ?sf a :SecurityFeature .
    ?sf :hasProperty ?p .
    ?p :typeProperty "confidentiality" .

    FILTER NOT EXISTS {
        ?sf :hasSecurityConstraint ?sc .
        ?sc a :Channel }
}





## SSLTSLRequiresCipher

SecurityFeature
- SecurityConstraint
    - Channel = SSLTSL
- SecurityConstraint
    - Cipher



