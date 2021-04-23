---
description: Распределитель памяти
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Распределитель памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909425"
---
# <a name="memory-allocator"></a><span data-ttu-id="33016-103">Распределитель памяти</span><span class="sxs-lookup"><span data-stu-id="33016-103">Memory Allocator</span></span>

<span data-ttu-id="33016-104">Объект распределителя памяти выделяет буферы для образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="33016-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="33016-105">Фильтры могут использовать этот объект для выделения буферов общей памяти; Однако фильтр с особыми требованиями также может реализовать собственный объект распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="33016-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="33016-106">Создайте этот объект, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="33016-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="33016-107">Метка</span><span class="sxs-lookup"><span data-stu-id="33016-107">Label</span></span> | <span data-ttu-id="33016-108">Значение</span><span class="sxs-lookup"><span data-stu-id="33016-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="33016-109">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="33016-109">Class Identifier</span></span> | <span data-ttu-id="33016-110">\_МЕМОРЯЛЛОКАТОР CLSID</span><span class="sxs-lookup"><span data-stu-id="33016-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="33016-111">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="33016-111">Interfaces</span></span>       | [<span data-ttu-id="33016-112">**имемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="33016-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="33016-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="33016-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33016-114">Объекты DirectShow</span><span class="sxs-lookup"><span data-stu-id="33016-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



