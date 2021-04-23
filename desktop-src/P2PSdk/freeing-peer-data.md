---
description: Все указатели, возвращаемые функциями одноранговой инфраструктуры, должны быть освобождены с помощью Пирграффридата или Пирфридата.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Освобождение данных однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080795"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="892c2-103">Освобождение данных однорангового узла</span><span class="sxs-lookup"><span data-stu-id="892c2-103">Freeing Peer Data</span></span>

<span data-ttu-id="892c2-104">Все указатели, возвращаемые функциями одноранговой инфраструктуры, должны быть освобождены с помощью [**пирграффридата**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) или [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="892c2-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="892c2-105">Эти функции должны вызываться только для структур, которые непосредственно возвращаются функцией одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="892c2-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="892c2-106">Не вызывайте другую функцию Фридата для высвобождения вложенных указателей, например, не вызывайте функцию Фридата для указателей в структуре [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="892c2-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="892c2-107">Пример освобождения данных</span><span class="sxs-lookup"><span data-stu-id="892c2-107">Example of Freeing Data</span></span>

<span data-ttu-id="892c2-108">В следующем фрагменте кода показано, как получить свойства, связанные с графом, а затем освободить возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="892c2-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



