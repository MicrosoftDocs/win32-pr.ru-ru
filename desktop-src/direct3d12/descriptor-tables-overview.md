---
title: Общие сведения о таблицах дескрипторов
description: Каждая таблица дескрипторов хранит дескрипторы одного или нескольких типов — СРВС, уаве, КБВС и пробы. Таблица дескрипторов не является выделением памяти; Это просто смещение и длина в куче дескрипторов.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105020"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="d3113-104">Общие сведения о таблицах дескрипторов</span><span class="sxs-lookup"><span data-stu-id="d3113-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="d3113-105">Каждая таблица дескрипторов хранит дескрипторы одного или нескольких типов — СРВС, уаве, КБВС и пробы.</span><span class="sxs-lookup"><span data-stu-id="d3113-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="d3113-106">Таблица дескрипторов не является выделением памяти; Это просто смещение и длина в куче дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="d3113-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="d3113-107">Ссылки на таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="d3113-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="d3113-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d3113-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="d3113-109">Ссылки на таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="d3113-109">Referencing descriptor tables</span></span>

<span data-ttu-id="d3113-110">Графический конвейер, через корневую подпись, получает доступ к ресурсам, ссылаясь на таблицы дескрипторов по индексу.</span><span class="sxs-lookup"><span data-stu-id="d3113-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="d3113-111">Таблица дескрипторов фактически является только поддиапазоном кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="d3113-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="d3113-112">Кучи дескрипторов представляют базовое выделение памяти для коллекции дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="d3113-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="d3113-113">Так как выделение памяти является свойством создания кучи дескрипторов, определение таблицы дескриптора из одной из них гарантированно становится недешевой, чем определение региона в куче на оборудование.</span><span class="sxs-lookup"><span data-stu-id="d3113-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="d3113-114">Таблицы дескрипторов не нужно создавать или удалять на уровне API — они просто обнаруживаются драйверами как смещение и размер из кучи при каждой ссылке.</span><span class="sxs-lookup"><span data-stu-id="d3113-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="d3113-115">Вполне возможно, что приложение может определить очень крупные таблицы дескрипторов, когда ее шейдеры хотят выбрать из огромного набора доступных дескрипторов (часто ссылающихся на текстуры) на лету (возможно, на основе данных материала).</span><span class="sxs-lookup"><span data-stu-id="d3113-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="d3113-116">Корневая подпись ссылается на запись таблицы дескрипторов со ссылкой на кучу, начальным расположением таблицы (смещением от начала кучи) и длиной (в записях) таблицы.</span><span class="sxs-lookup"><span data-stu-id="d3113-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="d3113-117">На рисунке ниже показаны эти понятия: указатели таблицы дескрипторов из корневой сигнатуры и дескрипторы в куче дескрипторов, ссылающиеся на полную текстуру или данные буфера в куче передачи.</span><span class="sxs-lookup"><span data-stu-id="d3113-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![таблицы дескрипторов](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="d3113-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d3113-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3113-120">Таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="d3113-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




