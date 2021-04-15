---
description: Управление графами фильтра с помощью языка C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Управление графами фильтра с помощью языка C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422989"
---
# <a name="controlling-filter-graphs-using-c"></a>Управление графами фильтра с помощью языка C

При написании приложения DirectShow на языке C (а не C++) для вызова методов необходимо использовать указатель vtable. В следующем примере показано, как вызвать метод **IUnknown:: QueryInterface** из приложения, написанного на языке C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Ниже показан эквивалентный вызов в C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



В C интерфейсы COM определяются как структуры. Элемент **лпвтбл** является указателем на таблицу методов интерфейса (vtable). Все методы принимают дополнительный параметр, который является указателем на интерфейс.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Приложения](appendixes.md)
</dt> </dl>

 

 



