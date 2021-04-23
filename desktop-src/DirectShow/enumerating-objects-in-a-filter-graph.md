---
description: Перечисление объектов в графе фильтра
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Перечисление объектов в графе фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139923"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="e7de4-103">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="e7de4-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="e7de4-104">Приложению может потребоваться выбрать определенный фильтр в графе фильтра или даже определенный ПИН-код для фильтра.</span><span class="sxs-lookup"><span data-stu-id="e7de4-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="e7de4-105">Например, он может использовать интерфейс, предоставляемый определенным фильтром.</span><span class="sxs-lookup"><span data-stu-id="e7de4-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="e7de4-106">Кроме того, он может создать специализированный граф фильтра и для подключения фильтров необходимо вызвать методы на отдельных контактах.</span><span class="sxs-lookup"><span data-stu-id="e7de4-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="e7de4-107">Для этой цели DirectShow предоставляет несколько методов перечисления объектов в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="e7de4-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="e7de4-108">Перечислители, обсуждаемые в этом разделе, следуют стандартной форме, используемой интерфейсами перечисления COM.</span><span class="sxs-lookup"><span data-stu-id="e7de4-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="e7de4-109">Дополнительные сведения см. в разделе "Иенумкскскскс" в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="e7de4-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="e7de4-110">Сведения о перечислении фильтров, зарегистрированных на компьютере пользователя, но еще не находящимся на графе фильтра, см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e7de4-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="e7de4-111">Эта статья содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="e7de4-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="e7de4-112">Перечисление фильтров</span><span class="sxs-lookup"><span data-stu-id="e7de4-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="e7de4-113">Перечисление ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="e7de4-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="e7de4-114">Перечисление типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e7de4-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="e7de4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e7de4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7de4-116">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7de4-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



