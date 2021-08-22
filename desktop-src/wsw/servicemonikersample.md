---
title: сервицемоникерсампле
description: В этом примере показан клиент, который можно использовать с образцом TCP MetadataExchange. Он использует моникер службы WCF.
ms.assetid: cfcff5ee-c0e1-4694-831e-fed0bd0e9855
keywords:
- API веб-служб сервицемоникерсампле Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dffac8b7eb4c9bdb92d4622452c15d56f53a514ba94fa908d38e1232dfec95f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026172"
---
# <a name="servicemonikersample"></a>сервицемоникерсампле

В этом примере показан клиент, который можно использовать с образцом TCP MetadataExchange. Он использует моникер службы WCF.

-   [PurchaseOrderClient.vbs](#purchaseorderclientvbs)

## <a name="purchaseorderclientvbs"></a>PurchaseOrderClient.vbs


```VB
set obj = GetObject("service:mexAddress='net.tcp://localhost/example/mex', address='net.tcp://localhost/example', contract='IPurchaseOrder', contractNamespace='http://example.org', binding=PurchaseOrderBinding, bindingNamespace='http://example.org'")
for i = 1 to 100
 orderId = obj.Order(i,"Pencil", date)
 Wscript.Echo orderId, date
Next 


```



 

 




