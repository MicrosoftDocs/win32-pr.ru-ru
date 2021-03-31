---
title: сервицемоникерсампле
description: В этом примере показан клиент, который можно использовать с образцом TCP MetadataExchange. Он использует моникер службы WCF.
ms.assetid: cfcff5ee-c0e1-4694-831e-fed0bd0e9855
keywords:
- API веб-служб Windows Сервицемоникерсампле
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3188b41df830f55e77e151c5be9413a986a5dcf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329795"
---
# <a name="servicemonikersample"></a><span data-ttu-id="de59d-107">сервицемоникерсампле</span><span class="sxs-lookup"><span data-stu-id="de59d-107">ServiceMonikerSample</span></span>

<span data-ttu-id="de59d-108">В этом примере показан клиент, который можно использовать с образцом TCP MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="de59d-108">This sample shows a client which can be used with the TCP MetadataExchange sample.</span></span> <span data-ttu-id="de59d-109">Он использует моникер службы WCF.</span><span class="sxs-lookup"><span data-stu-id="de59d-109">It utilizes WCF service moniker.</span></span>

-   [<span data-ttu-id="de59d-110">PurchaseOrderClient.vbs</span><span class="sxs-lookup"><span data-stu-id="de59d-110">PurchaseOrderClient.vbs</span></span>](#purchaseorderclientvbs)

## <a name="purchaseorderclientvbs"></a><span data-ttu-id="de59d-111">PurchaseOrderClient.vbs</span><span class="sxs-lookup"><span data-stu-id="de59d-111">PurchaseOrderClient.vbs</span></span>


```VB
set obj = GetObject("service:mexAddress='net.tcp://localhost/example/mex', address='net.tcp://localhost/example', contract='IPurchaseOrder', contractNamespace='http://example.org', binding=PurchaseOrderBinding, bindingNamespace='http://example.org'")
for i = 1 to 100
 orderId = obj.Order(i,"Pencil", date)
 Wscript.Echo orderId, date
Next 


```



 

 




