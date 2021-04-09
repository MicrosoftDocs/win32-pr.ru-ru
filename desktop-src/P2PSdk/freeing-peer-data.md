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
# <a name="freeing-peer-data"></a>Освобождение данных однорангового узла

Все указатели, возвращаемые функциями одноранговой инфраструктуры, должны быть освобождены с помощью [**пирграффридата**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) или [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Эти функции должны вызываться только для структур, которые непосредственно возвращаются функцией одноранговой инфраструктуры. Не вызывайте другую функцию Фридата для высвобождения вложенных указателей, например, не вызывайте функцию Фридата для указателей в структуре [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) .

## <a name="example-of-freeing-data"></a>Пример освобождения данных

В следующем фрагменте кода показано, как получить свойства, связанные с графом, а затем освободить возвращаемые данные.


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



 

 



