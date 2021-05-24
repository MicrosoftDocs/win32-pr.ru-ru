---
title: Сводка по настройке куч дескрипторов
description: В следующей таблице представлены сведения о поддержке шейдера и видимой кучи без шейдера.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335576"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="30a0a-103">Сводка по настройке куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="30a0a-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="30a0a-104">В следующей таблице представлены сведения о поддержке шейдера и видимой кучи без шейдера.</span><span class="sxs-lookup"><span data-stu-id="30a0a-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="30a0a-105">Видимая куча дескрипторов шейдеров</span><span class="sxs-lookup"><span data-stu-id="30a0a-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="30a0a-106">Видимая куча дескрипторов без шейдеров</span><span class="sxs-lookup"><span data-stu-id="30a0a-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a0a-107">**Поддерживаемые типы кучи**</span><span class="sxs-lookup"><span data-stu-id="30a0a-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="30a0a-108">CBV \_ SRV \_ UAV, образец</span><span class="sxs-lookup"><span data-stu-id="30a0a-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="30a0a-109">Все</span><span class="sxs-lookup"><span data-stu-id="30a0a-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="30a0a-110">**Поддерживаемые свойства страницы ЦП**</span><span class="sxs-lookup"><span data-stu-id="30a0a-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="30a0a-111">\_недоступно, запись \_ объединения</span><span class="sxs-lookup"><span data-stu-id="30a0a-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="30a0a-112">\_обратная запись</span><span class="sxs-lookup"><span data-stu-id="30a0a-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="30a0a-113">**Управление местонахождение по приложениям**</span><span class="sxs-lookup"><span data-stu-id="30a0a-113">**Residency Management By App**</span></span>   | <span data-ttu-id="30a0a-114">Да, ответственное за приложение</span><span class="sxs-lookup"><span data-stu-id="30a0a-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="30a0a-115">Неприменимо (не отображается GPU).</span><span class="sxs-lookup"><span data-stu-id="30a0a-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="30a0a-116">**Поддержка редактирования дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="30a0a-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="30a0a-117">Копировать только назначение, через обновление списка команд и (или) копирование ЦП, если отображается ЦП.</span><span class="sxs-lookup"><span data-stu-id="30a0a-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="30a0a-118">Только чтение и запись ЦП.</span><span class="sxs-lookup"><span data-stu-id="30a0a-118">CPU read and write only.</span></span> <span data-ttu-id="30a0a-119">Прямой доступ к GPU отсутствует.</span><span class="sxs-lookup"><span data-stu-id="30a0a-119">No direct GPU access.</span></span> <span data-ttu-id="30a0a-120">Может использоваться для немедленного копирования ЦП (в качестве источника и назначения).</span><span class="sxs-lookup"><span data-stu-id="30a0a-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="30a0a-121">Можно использовать в качестве источника обновления в списке команд — это приведет к копированию дескрипторов в хранилище списка команд во время записи списка команд.</span><span class="sxs-lookup"><span data-stu-id="30a0a-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="30a0a-122">При выполнении хранимая копия будет скопирована в место назначения, что должно быть видимой кучей шейдера.</span><span class="sxs-lookup"><span data-stu-id="30a0a-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="30a0a-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="30a0a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a0a-124">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="30a0a-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




