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
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="fdf4a-103">Управление графами фильтра с помощью языка C</span><span class="sxs-lookup"><span data-stu-id="fdf4a-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="fdf4a-104">При написании приложения DirectShow на языке C (а не C++) для вызова методов необходимо использовать указатель vtable.</span><span class="sxs-lookup"><span data-stu-id="fdf4a-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="fdf4a-105">В следующем примере показано, как вызвать метод **IUnknown:: QueryInterface** из приложения, написанного на языке C:</span><span class="sxs-lookup"><span data-stu-id="fdf4a-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="fdf4a-106">Ниже показан эквивалентный вызов в C++:</span><span class="sxs-lookup"><span data-stu-id="fdf4a-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="fdf4a-107">В C интерфейсы COM определяются как структуры.</span><span class="sxs-lookup"><span data-stu-id="fdf4a-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="fdf4a-108">Элемент **лпвтбл** является указателем на таблицу методов интерфейса (vtable).</span><span class="sxs-lookup"><span data-stu-id="fdf4a-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="fdf4a-109">Все методы принимают дополнительный параметр, который является указателем на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fdf4a-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdf4a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="fdf4a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf4a-111">Приложения</span><span class="sxs-lookup"><span data-stu-id="fdf4a-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



