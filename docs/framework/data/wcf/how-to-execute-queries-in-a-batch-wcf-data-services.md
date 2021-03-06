---
title: "How to: Execute Queries in a Batch (WCF Data Services)"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-oob"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "WCF Data Services, batch requests"
ms.assetid: 3b4db7df-bd33-43a1-8ea4-63a18e131f97
caps.latest.revision: 2
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
---
# How to: Execute Queries in a Batch (WCF Data Services)
By using the [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] client library, you can execute more than one query against the data service in a single batch. For more information, see [Batching Operations](../../../../docs/framework/data/wcf/batching-operations-wcf-data-services.md).  
  
 The example in this topic uses the Northwind sample data service and autogenerated client data service classes. This service and the client data classes are created when you complete the [WCF Data Services quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## Example  
 The following example shows how to call the <xref:System.Data.Services.Client.DataServiceContext.ExecuteBatch%2A> method to execute an array of <xref:System.Data.Services.Client.DataServiceRequest%601> objects that contains queries that return both `Customers` and `Products` objects from the Northwind data service. The collection of <xref:System.Data.Services.Client.QueryOperationResponse%601> objects in the returned <xref:System.Data.Services.Client.DataServiceResponse> is enumerated, and the collection of objects contained in each <xref:System.Data.Services.Client.QueryOperationResponse%601> is also enumerated.  
  
 [!code-csharp[Astoria Northwind Client#BatchQuery](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#batchquery)]
 [!code-vb[Astoria Northwind Client#BatchQuery](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#batchquery)]  
  
## See Also  
 [WCF Data Services Client Library](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
