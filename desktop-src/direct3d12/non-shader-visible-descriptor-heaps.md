---
title: Недоступные шейдеру кучи дескрипторов
description: Шейдеры не могут ссылаться на некоторые кучи дескрипторов через таблицы дескрипторов, но существуют либо для помощи приложению в промежуточной среде перед записью списка команд, либо из-за отсутствия в ней видимой кучи.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343459"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="3e573-103">Недоступные шейдеру кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="3e573-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="3e573-104">Шейдеры не могут ссылаться на некоторые кучи дескрипторов через таблицы дескрипторов, но существуют либо для помощи приложению в промежуточной среде перед записью списка команд, либо из-за отсутствия в ней видимой кучи.</span><span class="sxs-lookup"><span data-stu-id="3e573-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="3e573-105">Невидимые представления</span><span class="sxs-lookup"><span data-stu-id="3e573-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="3e573-106">Сводка</span><span class="sxs-lookup"><span data-stu-id="3e573-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="3e573-107">См. также</span><span class="sxs-lookup"><span data-stu-id="3e573-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="3e573-108">Невидимые представления</span><span class="sxs-lookup"><span data-stu-id="3e573-108">Non-visible views</span></span>

<span data-ttu-id="3e573-109">Все кучи дескрипторов, включая созданные ранее кучи дескрипторов шейдеров, могут управляться ЦП и/или списками команд в зависимости от пула памяти и свойств доступа к ЦП, которые приложение выбирает для кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="3e573-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="3e573-110">Очевидной причиной запрета доступа шейдера к этим кучам дескриптора для [видимых куч дескрипторов шейдером](shader-visible-descriptor-heaps.md)является промежуточная причина.</span><span class="sxs-lookup"><span data-stu-id="3e573-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="3e573-111">Затем эти кучи становятся видимыми для шейдера и доступны через таблицы дескрипторов при выполнении списка команд.</span><span class="sxs-lookup"><span data-stu-id="3e573-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="3e573-112">Тем не менее, нет необходимости в промежуточных кучах, которые можно заполнить напрямую.</span><span class="sxs-lookup"><span data-stu-id="3e573-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="3e573-113">Другие дескрипторы привязываются к конвейеру путем записи их содержимого непосредственно в список команд.</span><span class="sxs-lookup"><span data-stu-id="3e573-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="3e573-114">Эти дескрипторы служат только для преобразования параметров представления в список команд время записи.</span><span class="sxs-lookup"><span data-stu-id="3e573-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="3e573-115">Эти кучи всегда отображаются без шейдера и содержат следующие данные.</span><span class="sxs-lookup"><span data-stu-id="3e573-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="3e573-116">Представления целевого объекта прорисовки (RTVs)</span><span class="sxs-lookup"><span data-stu-id="3e573-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="3e573-117">Представления трафарета глубины (DSV)</span><span class="sxs-lookup"><span data-stu-id="3e573-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="3e573-118">Представления буферов индексов (Ибвс), представления буфера вершин (Вбвс) и представления потокового вывода (СОВС) передаются непосредственно методам API, не имеют конкретных типов кучи.</span><span class="sxs-lookup"><span data-stu-id="3e573-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="3e573-119">После записи в список команд (например, с помощью вызова, например [**омсетрендертаржетс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)) память, используемая для хранения дескрипторов этого вызова, немедленно становится доступной для повторного использования после вызова.</span><span class="sxs-lookup"><span data-stu-id="3e573-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="3e573-120">Даже таблицы дескрипторов имеют параметры, где приложение может позволить реализации выбрать запись содержимого таблицы при записи списка команд (вместо разыменования указателя на таблицу во время выполнения).</span><span class="sxs-lookup"><span data-stu-id="3e573-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="3e573-121">Итоги</span><span class="sxs-lookup"><span data-stu-id="3e573-121">Summary</span></span>



|                   | <span data-ttu-id="3e573-122">Видимый шейдер, только запись ЦП</span><span class="sxs-lookup"><span data-stu-id="3e573-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="3e573-123">Видимый без шейдера, чтение и запись ЦП</span><span class="sxs-lookup"><span data-stu-id="3e573-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="3e573-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="3e573-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="3e573-125">да</span><span class="sxs-lookup"><span data-stu-id="3e573-125">yes</span></span>                                | <span data-ttu-id="3e573-126">да</span><span class="sxs-lookup"><span data-stu-id="3e573-126">yes</span></span>                                    |
| <span data-ttu-id="3e573-127">**ОБРАЗЕЦ**</span><span class="sxs-lookup"><span data-stu-id="3e573-127">**SAMPLER**</span></span>       | <span data-ttu-id="3e573-128">да</span><span class="sxs-lookup"><span data-stu-id="3e573-128">yes</span></span>                                | <span data-ttu-id="3e573-129">да</span><span class="sxs-lookup"><span data-stu-id="3e573-129">yes</span></span>                                    |
| <span data-ttu-id="3e573-130">**Возврат поставщику**</span><span class="sxs-lookup"><span data-stu-id="3e573-130">**RTV**</span></span>           | <span data-ttu-id="3e573-131">нет</span><span class="sxs-lookup"><span data-stu-id="3e573-131">no</span></span>                                 | <span data-ttu-id="3e573-132">да</span><span class="sxs-lookup"><span data-stu-id="3e573-132">yes</span></span>                                    |
| <span data-ttu-id="3e573-133">**ПРЕДСТАВЛЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="3e573-133">**DSV**</span></span>           | <span data-ttu-id="3e573-134">нет</span><span class="sxs-lookup"><span data-stu-id="3e573-134">no</span></span>                                 | <span data-ttu-id="3e573-135">да</span><span class="sxs-lookup"><span data-stu-id="3e573-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3e573-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3e573-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e573-137">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="3e573-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




