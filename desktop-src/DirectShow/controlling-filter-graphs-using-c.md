---
description: Управление графами фильтра с помощью языка C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Управление графами фильтра с помощью языка C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073758"
---
# <a name="controlling-filter-graphs-using-c"></a>Управление графами фильтра с помощью языка C

при написании DirectShow приложения в C (а не C++) для вызова методов необходимо использовать указатель vtable. В следующем примере показано, как вызвать метод **IUnknown:: QueryInterface** из приложения, написанного на языке C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Ниже показан эквивалентный вызов в C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



В C интерфейсы COM определяются как структуры. Элемент **лпвтбл** является указателем на таблицу методов интерфейса (vtable). Все методы принимают дополнительный параметр, который является указателем на интерфейс.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Приложения](appendixes.md)
</dt> </dl>

 

 



