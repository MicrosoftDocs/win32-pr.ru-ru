---
title: Пример корневых подписей
description: В следующем разделе показано, какие корневые подписи имеют разный уровень сложности от Empty до полного заполнения.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104260"
---
# <a name="example-root-signatures"></a><span data-ttu-id="5342b-103">Пример корневых подписей</span><span class="sxs-lookup"><span data-stu-id="5342b-103">Example Root Signatures</span></span>

<span data-ttu-id="5342b-104">В следующем разделе показано, какие корневые подписи имеют разный уровень сложности от Empty до полного заполнения.</span><span class="sxs-lookup"><span data-stu-id="5342b-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="5342b-105">Пустая корневая подпись</span><span class="sxs-lookup"><span data-stu-id="5342b-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="5342b-106">Одна константа</span><span class="sxs-lookup"><span data-stu-id="5342b-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="5342b-107">Добавление представления буфера корневой константы</span><span class="sxs-lookup"><span data-stu-id="5342b-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="5342b-108">Таблицы дескрипторов привязки</span><span class="sxs-lookup"><span data-stu-id="5342b-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="5342b-109">Более сложная корневая подпись</span><span class="sxs-lookup"><span data-stu-id="5342b-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="5342b-110">Представления ресурсов потокового шейдера</span><span class="sxs-lookup"><span data-stu-id="5342b-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="5342b-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5342b-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="5342b-112">Пустая корневая подпись</span><span class="sxs-lookup"><span data-stu-id="5342b-112">An empty root signature</span></span>

![пустая корневая сигнатура не имеет привязок](images/root-tables-0.png)

<span data-ttu-id="5342b-114">Пустая корневая подпись вряд ли будет полезной, но ее можно использовать в тривиальных проходах с использованием только входного ассемблера, а также минимальных шейдеров вершин и пикселей, которые не обращаются ни к каким дескрипторам.</span><span class="sxs-lookup"><span data-stu-id="5342b-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="5342b-115">Кроме того, доступна стадия Blend, Целевая цель отрисовки и этапы глубины трафаретов, даже с пустой корневой сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="5342b-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="5342b-116">Одна константа</span><span class="sxs-lookup"><span data-stu-id="5342b-116">One constant</span></span>

![одна корневая константа](images/root-tables-constant.png)

<span data-ttu-id="5342b-118">Слот привязки API, в котором корневой аргумент для этого параметра будет привязан в списке команд время записи.</span><span class="sxs-lookup"><span data-stu-id="5342b-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="5342b-119">Число слотов привязки API является неявным в зависимости от порядка параметров в корневой сигнатуре (первый всегда равен нулю).</span><span class="sxs-lookup"><span data-stu-id="5342b-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="5342b-120">Слот привязки HLSL, где шейдер увидит параметр root, отображается.</span><span class="sxs-lookup"><span data-stu-id="5342b-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="5342b-121">Тип ("uint" в приведенном выше примере) неизвестен оборудованию, но является просто комментарием на изображении, оборудование просто увидит единственный DWORD в качестве содержимого.</span><span class="sxs-lookup"><span data-stu-id="5342b-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="5342b-122">Для привязки константы к времени записи списка команд используется следующая команда:</span><span class="sxs-lookup"><span data-stu-id="5342b-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="5342b-123">Добавление представления буфера корневой константы</span><span class="sxs-lookup"><span data-stu-id="5342b-123">Adding a root Constant Buffer View</span></span>

![Добавляет представление буфера константы в корневую подпись](images/root-tables-cbv.png)

<span data-ttu-id="5342b-125">В этом примере показаны две корневые константы и представление буфера корневых констант (CBV), которое наследует затраты на два слота DWORD.</span><span class="sxs-lookup"><span data-stu-id="5342b-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="5342b-126">Для привязки представления буфера констант используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="5342b-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="5342b-127">Обратите внимание, что первый параметр (2) — это слот, показанный на изображении.</span><span class="sxs-lookup"><span data-stu-id="5342b-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="5342b-128">Обычно массив констант настраивается, а затем становится доступным для шейдеров в B0 в виде CBV.</span><span class="sxs-lookup"><span data-stu-id="5342b-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="5342b-129">Таблицы дескрипторов привязки</span><span class="sxs-lookup"><span data-stu-id="5342b-129">Binding descriptor tables</span></span>

![Добавляет таблицы дескрипторов в корневую подпись](images/root-tables-2.png)

<span data-ttu-id="5342b-131">В этом примере показано использование двух таблиц дескрипторов. одно объявление таблицы из пяти дескрипторов, которое будет доступно во время выполнения в \_ КУЧЕ CBV SRV \_ UAV, и другое объявление таблицы из двух дескрипторов, которые будут отображаться во время выполнения в куче дескрипторов образцов.</span><span class="sxs-lookup"><span data-stu-id="5342b-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="5342b-132">Для привязки таблиц дескрипторов при записи списка команд.</span><span class="sxs-lookup"><span data-stu-id="5342b-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="5342b-133">Еще одна функция корневой сигнатуры — это корневая константа float4, которая имеет четыре DWORD в размере.</span><span class="sxs-lookup"><span data-stu-id="5342b-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="5342b-134">Следующая команда привязывает только средние два DWORD из четырех.</span><span class="sxs-lookup"><span data-stu-id="5342b-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="5342b-135">Более сложная корневая подпись</span><span class="sxs-lookup"><span data-stu-id="5342b-135">A more complex root signature</span></span>

![сложная корневая подпись с множеством элементов](images/root-tables-3.png)

<span data-ttu-id="5342b-137">В этом примере показана плотная корневая подпись с большинством типов записей.</span><span class="sxs-lookup"><span data-stu-id="5342b-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="5342b-138">Две таблицы дескрипторов (в слотах 3 и 6) включают массивы неограниченного размера.</span><span class="sxs-lookup"><span data-stu-id="5342b-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="5342b-139">Нагрузка здесь заключается в том, что приложение поддерживает только касание допустимых дескрипторов в куче.</span><span class="sxs-lookup"><span data-stu-id="5342b-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="5342b-140">Для неограниченных или очень больших массивов требуется аппаратный уровень 2 +, поддерживающий привязку ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5342b-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="5342b-141">Существует два статических пробных (связанных, не требующих корневых слотов подписи).</span><span class="sxs-lookup"><span data-stu-id="5342b-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="5342b-142">В слоте 9 UAV U4 и UAV U5 объявляются в одном и том же смещении таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="5342b-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="5342b-143">При использовании дескриптора псевдонима один дескриптор в памяти будет отображаться как U4 и U5 в шейдерах HLSL.</span><span class="sxs-lookup"><span data-stu-id="5342b-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="5342b-144">В этом случае шейдер должен быть скомпилирован с использованием \_ ресурсов шейдера D3D10 \_ , а также параметра \_ \_ или `/res_may_alias` в FXC.</span><span class="sxs-lookup"><span data-stu-id="5342b-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="5342b-145">Дескрипторы с псевдонимами позволяют привязывать один дескриптор к нескольким точкам привязки без внесения каких либо изменений в шейдер.</span><span class="sxs-lookup"><span data-stu-id="5342b-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="5342b-146">Представления ресурсов потокового шейдера</span><span class="sxs-lookup"><span data-stu-id="5342b-146">Streaming Shader Resource Views</span></span>

![представления ресурсов потокового шейдера в этой корневой подписи](images/root-tables-4.png)

<span data-ttu-id="5342b-148">Эта корневая подпись иллюстрирует ситуацию, когда все СРВС передаются в поток и из одного большого массива.</span><span class="sxs-lookup"><span data-stu-id="5342b-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="5342b-149">Во время выполнения таблица дескрипторов может быть задана один раз при установке корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="5342b-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="5342b-150">Затем все операции чтения текстур выполняются путем индексации в массив через константы, поступающие через первые несколько корневых аргументов.</span><span class="sxs-lookup"><span data-stu-id="5342b-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="5342b-151">Требуется только одна куча дескрипторов, и она обновляется только в том случае, если текстуры передаются в потоки или из свободных слотов дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="5342b-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="5342b-152">Смещения дескрипторов в большой куче определяются шейдерами с помощью констант в представлениях буфера констант.</span><span class="sxs-lookup"><span data-stu-id="5342b-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="5342b-153">Например, если для шейдера задан идентификатор материала, он может индексировать в один большой массив с помощью константы для доступа к требуемому дескриптору (который ссылается на требуемую текстуру).</span><span class="sxs-lookup"><span data-stu-id="5342b-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="5342b-154">Для этого сценария требуется оборудование с привязкой ресурсов партнеров +.</span><span class="sxs-lookup"><span data-stu-id="5342b-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5342b-155">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5342b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5342b-156">Уровни оборудования привязки ресурсов</span><span class="sxs-lookup"><span data-stu-id="5342b-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="5342b-157">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="5342b-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="5342b-158">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="5342b-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




