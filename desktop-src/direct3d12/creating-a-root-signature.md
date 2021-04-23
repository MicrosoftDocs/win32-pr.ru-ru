---
title: Создание корневой подписи
description: Корневые подписи являются сложной структурой данных, содержащей вложенные структуры.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548946"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="4e3b1-103">Создание корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-103">Creating a Root Signature</span></span>

<span data-ttu-id="4e3b1-104">Корневые подписи являются сложной структурой данных, содержащей вложенные структуры.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="4e3b1-105">Их можно определить программно с помощью приведенного ниже определения структуры данных (в том числе методы для помощи в инициализации членов).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="4e3b1-106">Кроме того, они могут быть созданы на языке высокого уровня заливки (HLSL), что дает возможность компилятору проверять, что макет совместим с шейдером.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="4e3b1-107">API для создания корневой подписи принимает сериализованную (автономную) версию описания макета, описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="4e3b1-108">Метод предназначен для создания этой сериализованной версии из структуры данных C++, но другим способом получения сериализованного определения корневой подписи является получение его из шейдера, скомпилированного с помощью корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="4e3b1-109">Если вы хотите воспользоваться преимуществами оптимизации драйверов для дескрипторов корневых подписей и данных, обратитесь к [корневой сигнатуре версии 1,1](root-signature-version-1-1.md) .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="4e3b1-110">Типы привязки таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="4e3b1-111">Диапазон дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="4e3b1-112">Макет таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="4e3b1-113">Корневые константы</span><span class="sxs-lookup"><span data-stu-id="4e3b1-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="4e3b1-114">Дескриптор корня</span><span class="sxs-lookup"><span data-stu-id="4e3b1-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="4e3b1-115">Видимость шейдера</span><span class="sxs-lookup"><span data-stu-id="4e3b1-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="4e3b1-116">Определение корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="4e3b1-117">Сериализация и десериализация структуры данных корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="4e3b1-118">API создания корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="4e3b1-119">Корневая подпись в объектах состояния конвейера</span><span class="sxs-lookup"><span data-stu-id="4e3b1-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="4e3b1-120">Код для определения корневой сигнатуры версии 1,1</span><span class="sxs-lookup"><span data-stu-id="4e3b1-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="4e3b1-121">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4e3b1-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="4e3b1-122">Типы привязки таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="4e3b1-123">[**\_ \_ \_ Тип диапазона дескрипторов перечисления D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) определяет типы передескрипторов, на которые может ссылаться как часть определения макета таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="4e3b1-124">Это диапазон, так что, например, если часть таблицы дескрипторов имеет 100 СРВС, этот диапазон можно объявить в одной записи, а не в 100.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="4e3b1-125">Поэтому определение таблицы дескрипторов — это коллекция диапазонов.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="4e3b1-126">Диапазон дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-126">Descriptor Range</span></span>

<span data-ttu-id="4e3b1-127">Структура [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) определяет набор дескрипторов заданного типа (например, СРВС) в таблице дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="4e3b1-128">Этот `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` макрос обычно можно использовать для `OffsetInDescriptorsFromTableStart` параметра [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="4e3b1-129">Это означает, что добавляется диапазон дескрипторов, определенный после предыдущего в таблице дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="4e3b1-130">Если приложению требуется создать псевдонимы для дескрипторов или по какой-либо причине нужно пропускать слоты, для него можно задать `OffsetInDescriptorsFromTableStart` любое смещение.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="4e3b1-131">Определение перекрывающихся диапазонов различных типов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="4e3b1-132">Набор регистров шейдеров, заданный сочетанием `RangeType` ,, и, `NumDescriptors` `BaseShaderRegister` `RegisterSpace` не может конфликтовать или перекрывать любые объявления в корневой сигнатуре, которые имеют общую [**\_ \_ видимость шейдера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (см. раздел видимость шейдера ниже).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="4e3b1-133">Макет таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="4e3b1-133">Descriptor Table Layout</span></span>

<span data-ttu-id="4e3b1-134">Структура [**\_ \_ \_ таблицы дескрипторов root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) объявляет макет таблицы дескрипторов в виде коллекции диапазонов дескрипторов, которые появляются в куче дескрипторов один за другим.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="4e3b1-135">Пробы не разрешены в той же таблице дескрипторов, что и CBV/UAV/СРВС.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="4e3b1-136">Эта структура используется, если для корневого слота подписи задано значение `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="4e3b1-137">Чтобы задать таблицу дескрипторов графики (CBV, SRV, UAV, образец), используйте [**ID3D12GraphicsCommandList:: сетграфиксрутдескриптортабле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="4e3b1-138">Чтобы задать таблицу дескрипторов вычислений, используйте [**ID3D12GraphicsCommandList:: сеткомпутерутдескриптортабле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="4e3b1-139">Корневые константы</span><span class="sxs-lookup"><span data-stu-id="4e3b1-139">Root Constants</span></span>

<span data-ttu-id="4e3b1-140">Структура [**\_ \_ констант D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) объявляет константы встроенной в корневой сигнатуре, которая отображается в шейдере как один буфер константы.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="4e3b1-141">Эта структура используется, если для корневого слота подписи задано значение `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="4e3b1-142">Дескриптор корня</span><span class="sxs-lookup"><span data-stu-id="4e3b1-142">Root Descriptor</span></span>

<span data-ttu-id="4e3b1-143">Структура [**\_ корневого \_ дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) в качестве встроенной сигнатуры объявляет дескрипторы (которые отображаются в шейдере).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="4e3b1-144">Эта структура используется, если тип слота корневой подписи имеет значение `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` или `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="4e3b1-145">Видимость шейдера</span><span class="sxs-lookup"><span data-stu-id="4e3b1-145">Shader Visibility</span></span>

<span data-ttu-id="4e3b1-146">Член набора перечисления [**\_ \_ видимости шейдеров D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) , заданный в параметре видимости шейдера [**\_ \_ параметра root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) , определяет, какие шейдеры видят содержимое заданного корневого слота подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="4e3b1-147">Функция COMPUTE всегда использует \_ ALL (так как имеется только один активный этап).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="4e3b1-148">График может выбрать, но если в ней используются \_ все, то все этапы построителя текстур видят все, что привязано к корневому слоту подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="4e3b1-149">Один из способов использования видимости шейдеров — помочь с шейдерами, созданными в ожидании различных привязок на каждый этап шейдера с помощью перекрывающихся пространств имен.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="4e3b1-150">Например, шейдер вершин может объявлять:</span><span class="sxs-lookup"><span data-stu-id="4e3b1-150">For example, a vertex shader may declare:</span></span>

 

<span data-ttu-id="4e3b1-151">Texture2D foo: Register (T0); "</span><span class="sxs-lookup"><span data-stu-id="4e3b1-151">Texture2D foo : register(t0);"</span></span>

 

<span data-ttu-id="4e3b1-152">Кроме того, шейдер пикселей может также объявлять:</span><span class="sxs-lookup"><span data-stu-id="4e3b1-152">and the pixel shader may also declare:</span></span>

 

<span data-ttu-id="4e3b1-153">Texture2D линейчатая: Register (T0);</span><span class="sxs-lookup"><span data-stu-id="4e3b1-153">Texture2D bar : register(t0);</span></span>

<span data-ttu-id="4e3b1-154">Если приложение делает привязку корневой подписи для T0 видимости \_ все, обе шейдеры видят одну и ту же текстуру.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-154">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="4e3b1-155">Если шейдер определяет, что каждый шейдер должен видеть различные текстуры, он может определить два корневых слота подписи с \_ вершиной видимости и \_ пикселями.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-155">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="4e3b1-156">Независимо от того, какая область видимости находится в корневом слоте подписи, она всегда имеет такие же затраты (только в зависимости от того, что Слоттипе) в сторону одного фиксированного максимального размера корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-156">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="4e3b1-157">На низком D3D11 оборудовании видимость ШЕЙДЕРа также учитывается \_ при проверке размеров таблиц дескрипторов в корневом макете, так как некоторые D3D11 оборудование могут поддерживать только максимальное количество привязок на каждый этап.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-157">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="4e3b1-158">Эти ограничения накладываются только при работе на оборудовании низкого уровня и не ограничивают более современное оборудование.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-158">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="4e3b1-159">Если в корневой сигнатуре определено несколько таблиц дескрипторов, которые перекрывают друг друга в пространстве имен (привязки регистров к шейдеру), а любой из них указывает \_ все для видимости, то макет является недопустимым (создание завершится ошибкой).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-159">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="4e3b1-160">Определение корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-160">Root Signature Definition</span></span>

<span data-ttu-id="4e3b1-161">[**Корневая структура \_ \_ подписи \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) может содержать таблицы дескрипторов и встроенные константы, каждый тип слота, определенный структурой [**\_ \_ параметра D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) , и [**\_ \_ \_ тип корневого параметра enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-161">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="4e3b1-162">Чтобы инициировать корневой слот подписи, см. методы **сеткомпутерут \* \* \*** и **сетграфиксрут \* \* \*** в [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-162">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="4e3b1-163">Статические пробы описаны в корневой подписи с использованием [**структуры \_ статического \_ образца D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-163">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="4e3b1-164">Некоторые флаги ограничивают доступ определенных шейдеров к корневой подписи, см. [**\_ \_ \_ Флаги корневой сигнатуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-164">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="4e3b1-165">Сериализация и десериализация структуры данных корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-165">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="4e3b1-166">Методы, описанные в этом разделе, экспортируются с помощью D3D12Core.dll и предоставляют методы для сериализации и десериализации корневой структуры данных сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-166">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="4e3b1-167">Сериализованная форма передается в API при создании корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-167">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="4e3b1-168">Если шейдер был создан с помощью корневой подписи (при добавлении этой возможности), скомпилированный шейдер уже будет содержать сериализованную корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-168">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="4e3b1-169">Если приложение последовательно создает структуру данных [**D3D12 \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , она должна сделать сериализованную форму с помощью [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-169">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="4e3b1-170">Выходные данные, которые можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-170">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="4e3b1-171">Если у приложения уже есть сериализованная корневая подпись или скомпилированный шейдер, содержащий корневую подпись и желающий программно обнаружить Определение макета (называемое "отражением"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) можно вызвать.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-171">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="4e3b1-172">При этом создается интерфейс [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , который содержит метод, возвращающий десериализованную структуру данных [**\_ DESC корневой \_ сигнатуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-172">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="4e3b1-173">Интерфейс владеет жизненным циклом десериализованной структуры данных.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-173">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="4e3b1-174">API создания корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-174">Root Signature Creation API</span></span>

<span data-ttu-id="4e3b1-175">API [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) принимает сериализованную версию корневой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-175">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="4e3b1-176">Корневая подпись в объектах состояния конвейера</span><span class="sxs-lookup"><span data-stu-id="4e3b1-176">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="4e3b1-177">Методы для создания состояния конвейера ([**ID3D12Device:: креатеграфикспипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) и [**ID3D12Device:: креатекомпутепипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) принимают необязательный интерфейс [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) в качестве входного параметра (который хранится в структуре описания [**\_ \_ \_ состояния \_ графического конвейера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-177">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="4e3b1-178">Все корневые подписи, уже имеющиеся в шейдере, переопределяются.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-178">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="4e3b1-179">Если корневая подпись передается в один из методов создания состояния конвейера, эта корневая подпись проверяется по всем шейдерам в PSO на совместимость и передается драйверу для использования со всеми шейдерами.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-179">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="4e3b1-180">Если какой-либо из шейдеров имеет другую корневую подпись, он заменяется корневой подписью, передаваемой в API.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-180">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="4e3b1-181">Если корневая подпись не передается, все передаваемые шейдеры должны иметь корневую подпись и должны совпадать — это будет предоставлено драйверу.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-181">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="4e3b1-182">Установка PSO для списка команд или набора не приводит к изменению корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-182">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="4e3b1-183">Это достигается с помощью методов [**сетграфиксрутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) и [**сеткомпутерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="4e3b1-183">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="4e3b1-184">При вызове времени (Graphics)/диспатч (вычисление) приложение должно гарантировать, что текущая PSO соответствует текущей корневой сигнатуре. в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-184">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="4e3b1-185">Код для определения корневой сигнатуры версии 1,1</span><span class="sxs-lookup"><span data-stu-id="4e3b1-185">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="4e3b1-186">В приведенном ниже примере показано, как создать корневую подпись в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="4e3b1-186">The example below shows how to create a root signature with the following format:</span></span>



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="4e3b1-187">**рутпараметериндекс**</span><span class="sxs-lookup"><span data-stu-id="4e3b1-187">**RootParameterIndex**</span></span> | <span data-ttu-id="4e3b1-188">**Contents**</span><span class="sxs-lookup"><span data-stu-id="4e3b1-188">**Contents**</span></span>                                   |                                              |
| <span data-ttu-id="4e3b1-189">\[0\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-189">\[0\]</span></span>                  | <span data-ttu-id="4e3b1-190">Корневые константы: {B2}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-190">Root constants: { b2 }</span></span>                         | <span data-ttu-id="4e3b1-191">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-191">(1 CBV)</span></span>                                      |
| <span data-ttu-id="4e3b1-192">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-192">\[1\]</span></span>                  | <span data-ttu-id="4e3b1-193">Таблица дескрипторов: {T2-T7, U0-U3}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-193">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="4e3b1-194">(6 СРВС + 4 Уавс)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-194">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="4e3b1-195">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-195">\[2\]</span></span>                  | <span data-ttu-id="4e3b1-196">Корневой CBV: {B0}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-196">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="4e3b1-197">(1 CBV, статические данные)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-197">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="4e3b1-198">\[3\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-198">\[3\]</span></span>                  | <span data-ttu-id="4e3b1-199">Таблица дескрипторов: {S0-S1}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-199">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="4e3b1-200">(2 проба)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-200">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="4e3b1-201">\[4\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-201">\[4\]</span></span>                  | <span data-ttu-id="4e3b1-202">Таблица дескрипторов: {T8-unbound}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-202">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="4e3b1-203">(без ограничений \# СРВС, переменных дескрипторов)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-203">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="4e3b1-204">\[5\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-204">\[5\]</span></span>                  | <span data-ttu-id="4e3b1-205">Таблица дескрипторов: {(T0, space1) — без ограничений}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-205">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="4e3b1-206">(без ограничений \# СРВС, переменных дескрипторов)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-206">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="4e3b1-207">\[6\]</span><span class="sxs-lookup"><span data-stu-id="4e3b1-207">\[6\]</span></span>                  | <span data-ttu-id="4e3b1-208">Таблица дескрипторов: {B1}</span><span class="sxs-lookup"><span data-stu-id="4e3b1-208">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="4e3b1-209">(1 CBV, статические данные)</span><span class="sxs-lookup"><span data-stu-id="4e3b1-209">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="4e3b1-210">Если большинство частей корневой подписи используются в большинстве случаев, это может быть лучше, чем необходимость слишком частого переключения корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-210">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="4e3b1-211">Приложения должны сортировать записи в корневой сигнатуре от наиболее часто изменяющихся по меньшей мере.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-211">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="4e3b1-212">Когда приложение изменяет привязки на любую часть корневой сигнатуры, драйверу может потребоваться создать копию некоторых или всех состояний корневой подписи, что может стать нетривиальной стоимостью при умножении нескольких изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-212">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="4e3b1-213">Кроме того, в корневой подписи будет определена статическая выборка, которая выполняет анизотропную фильтрацию текстур при регистрации шейдера в регистре S3.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-213">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="4e3b1-214">После привязки этой корневой сигнатуры таблицы дескрипторов, корневые CBV и константы могут быть назначены в \[ пространстве параметров 0.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-214">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="4e3b1-215">Например, таблицы дескрипторов (диапазоны в куче дескрипторов) можно привязать к каждому из корневых параметров \[ 1 \] и \[ 3.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="4e3b1-215">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="4e3b1-216">В следующем коде показано, как указанная выше подпись может использоваться в списке команд графики.</span><span class="sxs-lookup"><span data-stu-id="4e3b1-216">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="4e3b1-217">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4e3b1-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e3b1-218">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-218">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="4e3b1-219">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="4e3b1-219">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="4e3b1-220">Использование корневой подписи</span><span class="sxs-lookup"><span data-stu-id="4e3b1-220">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
