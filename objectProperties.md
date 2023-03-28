
OBJECT PROPERTIES


assetTypeHasAssetType
∃ assetTypeHasAssetType Thing ⊑ AssetType
⊤ ⊑ ∀ assetTypeHasAssetType AssetType

deviceHasInfrastructure
∃ deviceHasInfrastructure Thing ⊑ Device
⊤ ⊑ ∀ deviceHasInfrastructure Infrastructure

hasAppAndService
∃ hasAppAndService Thing ⊑ AssetType
⊤ ⊑ ∀ hasAppAndService AppAndService

hasAssetType
∃ hasAssetType Thing ⊑ SecurityRequirement
⊤ ⊑ ∀ hasAssetType AssetType

hasDevice
∃ hasDevice Thing ⊑ AssetType
⊤ ⊑ ∀ hasDevice Device

hasInformation
∃ hasInformation Thing ⊑ AssetType
⊤ ⊑ ∀ hasInformation Information

hasInfrastructure
∃ hasInfrastructure Thing ⊑ AssetType
⊤ ⊑ ∀ hasInfrastructure Infrastructure

hasPlatform
∃ hasPlatform Thing ⊑ AssetType
⊤ ⊑ ∀ hasPlatform Platform

hasProperty
∃ hasProperty Thing ⊑ SecurityFeature
⊤ ⊑ ∀ hasProperty Property

hasSecurityConstraint
∃ hasSecurityConstraint Thing ⊑ SecurityFeature
⊤ ⊑ ∀ hasSecurityConstraint SecurityConstraint

hasSecurityFeature
∃ hasSecurityFeature Thing ⊑ SecurityRequirement
⊤ ⊑ ∀ hasSecurityFeature SecurityFeature

hasSecurityLevel
∃ hasSecurityLevel Thing ⊑ SecurityFeature
⊤ ⊑ ∀ hasSecurityLevel SecurityLevel

hasSustainabilityLabel
∃ hasSustainabilityLabel Thing
⊤ ⊑ ∀ hasSustainabilityLabel SustainabilityLabel

hasUser
∃ hasUser Thing ⊑ AssetType
⊤ ⊑ ∀ hasUser User

informationHasInfrastructure
∃ informationHasInfrastructure Thing ⊑ Information
⊤ ⊑ ∀ informationHasInfrastructure Infrastructure

infrastructureHasDevice
∃ infrastructureHasDevice Thing ⊑ Infrastructure
⊤ ⊑ ∀ infrastructureHasDevice Device

infrastructureHasInformation
∃ infrastructureHasInformation Thing ⊑ Infrastructure
⊤ ⊑ ∀ infrastructureHasInformation Information

isLessSecureThan
∃ isLessSecureThan Thing ⊑ SecurityLevel
⊤ ⊑ ∀ isLessSecureThan SecurityLevel

isLessSustainabilityThan
∃ isLessSustainabilityThan Thing ⊑ SustainabilityLabel
⊤ ⊑ ∀ isLessSustainabilityThan SustainabilityLabel

isMoreSecureThan
∃ isMoreSecureThan Thing ⊑ SecurityLevel
⊤ ⊑ ∀ isMoreSecureThan SecurityLevel

isMoreSustainabilityThan
∃ isMoreSustainabilityThan Thing ⊑ SustainabilityLabel
⊤ ⊑ ∀ isMoreSustainabilityThan SustainabilityLabel

propertyHasSecurityConstraint
∃ propertyHasSecurityConstraint Thing ⊑ Property
⊤ ⊑ ∀ propertyHasSecurityConstraint SecurityConstraint

securityConstraintHasProperty
∃ securityConstraintHasProperty Thing ⊑ SecurityConstraint
⊤ ⊑ ∀ securityConstraintHasProperty Property
