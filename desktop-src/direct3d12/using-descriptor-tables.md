---
title: Использование таблиц дескрипторов
description: Таблицы дескрипторов, каждый из которых идентифицирует диапазон в куче дескрипторов, привязываются к слотам, определенным текущей корневой подписью в списке команд.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104336"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="9d79f-103">Использование таблиц дескрипторов</span><span class="sxs-lookup"><span data-stu-id="9d79f-103">Using Descriptor Tables</span></span>

<span data-ttu-id="9d79f-104">Таблицы дескрипторов, каждый из которых идентифицирует диапазон в куче дескрипторов, привязываются к слотам, определенным текущей корневой подписью в списке команд.</span><span class="sxs-lookup"><span data-stu-id="9d79f-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="9d79f-105">Таблицы дескрипторов индексации</span><span class="sxs-lookup"><span data-stu-id="9d79f-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="9d79f-106">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9d79f-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="9d79f-107">Шейдеры могут искать ресурсы, на которые ссылаются дескрипторы, составляющие таблицу индексов.</span><span class="sxs-lookup"><span data-stu-id="9d79f-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="9d79f-108">Другие привязки ресурсов — буферы индексов, буфер вершин, буферы вывода потока, целевые объекты отрисовки и трафарет глубины выполняются непосредственно в списке команд, а не с помощью дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="9d79f-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="9d79f-109">Подведение итогов.</span><span class="sxs-lookup"><span data-stu-id="9d79f-109">To summarize:</span></span>

<span data-ttu-id="9d79f-110">Следующие ссылки на ресурсы могут совместно использовать одну и ту же таблицу дескрипторов и кучу:</span><span class="sxs-lookup"><span data-stu-id="9d79f-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="9d79f-111">Представления ресурсов шейдера</span><span class="sxs-lookup"><span data-stu-id="9d79f-111">Shader resource views</span></span>
-   <span data-ttu-id="9d79f-112">Представления неупорядоченного доступа</span><span class="sxs-lookup"><span data-stu-id="9d79f-112">Unordered access views</span></span>
-   <span data-ttu-id="9d79f-113">Представления буфера констант</span><span class="sxs-lookup"><span data-stu-id="9d79f-113">Constant buffer views</span></span>

<span data-ttu-id="9d79f-114">Следующие ссылки на ресурсы должны находиться в собственной куче дескрипторов:</span><span class="sxs-lookup"><span data-stu-id="9d79f-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="9d79f-115">Образцы.</span><span class="sxs-lookup"><span data-stu-id="9d79f-115">Samplers</span></span>

<span data-ttu-id="9d79f-116">Следующие ресурсы не помещаются в таблицы дескрипторов или кучи, но привязываются напрямую с помощью списков команд:</span><span class="sxs-lookup"><span data-stu-id="9d79f-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="9d79f-117">Буферы индексов</span><span class="sxs-lookup"><span data-stu-id="9d79f-117">Index buffers</span></span>
-   <span data-ttu-id="9d79f-118">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="9d79f-118">Vertex buffers</span></span>
-   <span data-ttu-id="9d79f-119">Потоковые буферы вывода</span><span class="sxs-lookup"><span data-stu-id="9d79f-119">Stream output buffers</span></span>
-   <span data-ttu-id="9d79f-120">Целевые объекты рендеринга</span><span class="sxs-lookup"><span data-stu-id="9d79f-120">Render targets</span></span>
-   <span data-ttu-id="9d79f-121">Представления трафарета глубины</span><span class="sxs-lookup"><span data-stu-id="9d79f-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="9d79f-122">Таблицы дескрипторов индексации</span><span class="sxs-lookup"><span data-stu-id="9d79f-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="9d79f-123">Шейдеры не могут динамически индексироваться между границами таблиц дескрипторов с данного узла вызова в шейдере.</span><span class="sxs-lookup"><span data-stu-id="9d79f-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="9d79f-124">Однако выбор дескриптора в таблице дескрипторов может динамически индексироваться в коде шейдера в пределах диапазонов одного и того же типа дескриптора (например, индексирование по смежной области СРВС).</span><span class="sxs-lookup"><span data-stu-id="9d79f-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d79f-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9d79f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d79f-126">Таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="9d79f-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




