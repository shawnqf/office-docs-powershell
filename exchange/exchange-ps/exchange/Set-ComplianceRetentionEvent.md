---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
online version: https://learn.microsoft.com/powershell/module/exchange/set-complianceretentionevent
applicable: Security & Compliance
title: Set-ComplianceRetentionEvent
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
---

# Set-ComplianceRetentionEvent

## SYNOPSIS
This cmdlet is available only in Security & Compliance PowerShell. For more information, see [Security & Compliance PowerShell](https://learn.microsoft.com/powershell/exchange/scc-powershell).

Use the Set-ComplianceRetentionEvent cmdlet to modify compliance retention events in the Microsoft Purview compliance portal.

## SYNTAX

### Identity
```
Set-ComplianceRetentionEvent [-Identity] <PolicyIdParameter> -Action <SearchJobType>
 [-AssetId <String>]
 [-Comment <String>]
 [-Confirm]
 [-DomainController <Fqdn>]
 [-EventTags <MultiValuedProperty>]
 [-EventType <ComplianceRuleIdParameter>]
 [-ExchangeAssetIdQuery <String>]
 [-SharePointAssetIdQuery <String>]
 [-WhatIf] [<CommonParameters>]
```

### AdaptiveScopeLocation
```
Set-ComplianceRetentionEvent [-Identity] <PolicyIdParameter> -Action <SearchJobType>
 [-AssetId <String>]
 [-Comment <String>]
 [-Confirm]
 [-DomainController <Fqdn>]
 [-EventTags <MultiValuedProperty>]
 [-EventType <ComplianceRuleIdParameter>]
 [-ExchangeAssetIdQuery <String>]
 [-SharePointAssetIdQuery <String>]
 [-WhatIf] [<CommonParameters>]
```

### TeamLocation
```
Set-ComplianceRetentionEvent [-Identity] <PolicyIdParameter> -Action <SearchJobType>
 [-AssetId <String>]
 [-Comment <String>]
 [-Confirm]
 [-DomainController <Fqdn>]
 [-EventTags <MultiValuedProperty>]
 [-EventType <ComplianceRuleIdParameter>]
 [-ExchangeAssetIdQuery <String>]
 [-SharePointAssetIdQuery <String>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
To use this cmdlet in Security & Compliance PowerShell, you need to be assigned permissions. For more information, see [Permissions in the Microsoft Purview compliance portal](https://learn.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center-permissions).

## EXAMPLES

### Example 1
```powershell
{{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Identity
The Identity parameter specifies the compliance retention event that you want to modify. You can use any value that uniquely identifies the event. For example:

- Name
- Distinguished name (DN)
- GUID

```yaml
Type: PolicyIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Action
{{ Fill Action Description }}

```yaml
Type: SearchJobType
Parameter Sets: (All)
Aliases:
Accepted values: Search, Report
Applicable: Security & Compliance

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssetId
The AssetId parameter specifies the Property:Value pair found in the properties of SharePoint or OneDrive for Business documents that's used for retention. For example:

- Product codes that you can use to retain content for only a specific product.
- Project codes that you can use to retain content for only a specific project.
- Employee IDs that you can use to retain content for only a specific person.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
The Comment parameter specifies an optional comment. If the value contains spaces, enclose the value in quotation marks (").

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: `-Confirm:$false`.
- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
This parameter is reserved for internal Microsoft use.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventTags
The EventTags parameter specifies the GUID value of the labels tha are associated with the compliance retention event. Run the following command to see the available GUID values: `Get-ComplianceTag | Format-Table Name,GUID`.

You can specify multiple values separated by commas.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventType
The EventType parameter specifies the GUID value of the event that will start the retention period for labels that use this event type. Run the following command to see the available GUID values: `Get-ComplianceRetentionEventType | Format-Table Name,GUID`.

```yaml
Type: ComplianceRuleIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeAssetIdQuery
The ExchangeAssetIdQuery parameter specifies the keywords that are used to scope Exchange content for the compliance retention event. For details, see [Keyword queries and search conditions for Content Search](https://learn.microsoft.com/microsoft-365/compliance/keyword-queries-and-search-conditions).

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharePointAssetIdQuery
The SharePointAssetIdQuery parameter specifies one or more the Property:Value pairs that you've specified in the properties (also known as Columns) of SharePoint and OneDrive for Business documents to scope the compliance retention event.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch doesn't work in Security & Compliance PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
