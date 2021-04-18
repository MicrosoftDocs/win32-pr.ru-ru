---
description: Распределитель памяти
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Распределитель памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537805"
---
# <a name="memory-allocator"></a><span data-ttu-id="5b7b6-103">Распределитель памяти</span><span class="sxs-lookup"><span data-stu-id="5b7b6-103">Memory Allocator</span></span>

<span data-ttu-id="5b7b6-104">Объект распределителя памяти выделяет буферы для образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5b7b6-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="5b7b6-105">Фильтры могут использовать этот объект для выделения буферов общей памяти; Однако фильтр с особыми требованиями также может реализовать собственный объект распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="5b7b6-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="5b7b6-106">Создайте этот объект, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5b7b6-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="5b7b6-107">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="5b7b6-107">Class Identifier</span></span> | <span data-ttu-id="5b7b6-108">\_МЕМОРЯЛЛОКАТОР CLSID</span><span class="sxs-lookup"><span data-stu-id="5b7b6-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="5b7b6-109">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="5b7b6-109">Interfaces</span></span>       | [<span data-ttu-id="5b7b6-110">**имемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="5b7b6-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="5b7b6-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5b7b6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b7b6-112">Объекты DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b7b6-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



