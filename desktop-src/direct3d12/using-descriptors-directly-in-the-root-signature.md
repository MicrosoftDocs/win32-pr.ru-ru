---
title: Использование дескрипторов непосредственно в корневой подписи
description: Приложения могут добавлять дескрипторы непосредственно в корневую подпись, чтобы избежать необходимости проходить через кучу дескрипторов.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "104549030"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="b4ddd-103">Использование дескрипторов непосредственно в корневой подписи</span><span class="sxs-lookup"><span data-stu-id="b4ddd-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="b4ddd-104">Приложения могут добавлять дескрипторы непосредственно в корневую подпись, чтобы избежать необходимости проходить через кучу дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="b4ddd-105">Эти дескрипторы занимают много пространства в корневой подписи (см. раздел ограничения корневых подписей), поэтому приложения должны использовать их с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="b4ddd-106">В качестве примера использования можно поместить представления постоянного буфера (CBV), которые изменяются на рисование в корневом макете таким образом, чтобы пространство кучи дескриптора не выделилось приложением на Draw (и сохранить указатель на таблицу дескрипторов в новом месте в куче дескрипторов).</span><span class="sxs-lookup"><span data-stu-id="b4ddd-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="b4ddd-107">Поместив что-либо в корневую подпись, приложение просто переводит ответственность за управление версиями в драйвер, но это инфраструктура, которая у них уже есть.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="b4ddd-108">Для отрисовки, использующей очень незначительное число ресурсов, использование таблицы или кучи дескрипторов может быть ненужным, если все необходимые дескрипторы можно поместить непосредственно в корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="b4ddd-109">В корневой сигнатуре поддерживаются только следующие типы дескрипторов:</span><span class="sxs-lookup"><span data-stu-id="b4ddd-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="b4ddd-110">КБВС.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-110">CBVs.</span></span>
- <span data-ttu-id="b4ddd-111">Представления ресурсов шейдера (СРВС)/Унордеред Access Views (Уавс) буферных ресурсов, в которых формат SRV/UAV содержит только 32-разрядные компоненты FLOAT/UINT/Синт (преобразование формата отсутствует).</span><span class="sxs-lookup"><span data-stu-id="b4ddd-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="b4ddd-112">СРВС структуры ускорения райтраЦинг в локальных и глобальных корневых сигнатурах.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="b4ddd-113">Уавс в корне не может иметь связанные с ними счетчики.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="b4ddd-114">Дескрипторы в корневой подписи отображаются каждый как отдельные отдельные дескрипторы, &mdash; которые они не могут динамически индексировать.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="b4ddd-115">В приведенном выше примере `mySceneData` не может быть объявлен как массив, как в `cbuffer mySceneData[2]` случае, если он будет сопоставлен с дескриптором в корневой сигнатуре, так как индексирование в псевдонимах не поддерживается в корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="b4ddd-116">Приложение может определить отдельные отдельные буферы констант и определить их каждый как отдельную запись в корневой подписи при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="b4ddd-117">Обратите внимание, что в `mySceneData` приведенном выше примере имеется массив `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="b4ddd-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="b4ddd-118">Динамическое индексирование в буфере константы является допустимым. дескриптор в корневой подписи ведет себя так же, как и тот же дескриптор, при доступе через кучу дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="b4ddd-119">Это отличается от констант встраивания непосредственно в корневой сигнатуре, которая также выглядит как буфер констант, за исключением того, что динамическое индексирование внутри встроенных констант не разрешено `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="b4ddd-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="b4ddd-120">Следующие интерфейсы API (из интерфейса [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) предназначены для установки дескрипторов непосредственно в корневой подписи:</span><span class="sxs-lookup"><span data-stu-id="b4ddd-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="b4ddd-121">**сеткомпутерутконстантбуффервиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="b4ddd-122">**сетграфиксрутконстантбуффервиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="b4ddd-123">**сеткомпутерутшадерресаурцевиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="b4ddd-124">**сетграфиксрутшадерресаурцевиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="b4ddd-125">**сеткомпутерутунордередакцессвиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="b4ddd-126">**сетграфиксрутунордередакцессвиев**</span><span class="sxs-lookup"><span data-stu-id="b4ddd-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="b4ddd-127">В Direct3D 12 нет концепции "корневого массива дескрипторов".</span><span class="sxs-lookup"><span data-stu-id="b4ddd-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="b4ddd-128">Массивы дескрипторов поддерживаются только в кучах дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4ddd-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b4ddd-129">Related topics</span></span>

[<span data-ttu-id="b4ddd-130">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="b4ddd-130">Root Signatures</span></span>](root-signatures.md)
