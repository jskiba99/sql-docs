---
title: "Configure the (All) Level for Attribute Hierarchies | Microsoft Docs"
ms.custom: ""
ms.date: "03/14/2017"
ms.prod: analysis-services
ms.prod_service: "analysis-services"
ms.service: ""
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  
ms.component: multidimensional-tabular
ms.component: data-mining
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "All members"
  - "IsAggregatable property"
  - "topmost levels [Analysis Services]"
  - "(All) levels"
  - "AttributeAllMemberName property"
  - "levels [Analysis Services]"
  - "members [Analysis Services], All"
  - "AllMemberName property"
ms.assetid: 0cb35e6f-b10f-483d-b893-78f6ca3979fd
caps.latest.revision: 33
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
ms.workload: "Inactive"
---
# Database Dimensions - Configure the (All) Level for Attribute Hierarchies
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  In [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)], the (All) level is an optional, system-generated level. It contains only one member whose value is the aggregation of the values of all members in the immediately subordinate level. This member is called the All member. It is a system-generated member that is not contained in the dimension table. Because the member in the (All) level is at the top of the hierarchy, the member's value is the consolidated aggregation of the values of all members in the hierarchy. The All member often serves as the default member of a hierarchy.  
  
 The presence of an (All) level in an attribute hierarchy depends on the **IsAggregatable** property setting for the attribute and the presence of an (All) level in a user-defined hierarchy depends on the **IsAggregatable** property of the attribute at the top-most level of user-defined hierarchy. If the **IsAggregatable** property is set to **True**, an (All) level will exist. A hierarchy has no (All) level if the **IsAggregatable** property is set to **False**.  
  
## Establishing the Topmost Level  
 If the **IsAggregatable** property is set to **False** on the source attribute of a level in a hierarchy, then no aggregatable level can appear in the hierarchy above that level. A non-aggregatable level must be the topmost level of any hierarchy or the **IsAggregatable** property of the source attributes for any levels above it must also be set to **False**.  
  
## All Member and (All) Level  
 The single member of the (All) level is called the All member. The **AttributeAllMemberName**property on a dimension specifies the name of the All member for attributes in a dimension. The **AllMemberName** property on a hierarchy specifies the name of the All member for the hierarchy.  
  
## See Also  
 [Define a Default Member](../../analysis-services/multidimensional-models/attribute-properties-define-a-default-member.md)  
  
  
