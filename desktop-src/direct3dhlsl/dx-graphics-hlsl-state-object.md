---
title: Объекты состояния
description: Используйте HLSL для определения объектов State.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998010"
---
# <a name="state-objects"></a><span data-ttu-id="5571c-103">Объекты состояния</span><span class="sxs-lookup"><span data-stu-id="5571c-103">State Objects</span></span>

<span data-ttu-id="5571c-104">С помощью моделей шейдеров 6,3 и более поздних версий приложения имеют удобную и гибкую возможность определения объектов состояния ДКСР непосредственно в коде шейдера HLSL в дополнение к использованию API-интерфейсов Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="5571c-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="5571c-105">В HLSL объекты состояния объявляются с помощью этого синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="5571c-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="5571c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-106">Item</span></span>                                                                                         | <span data-ttu-id="5571c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="5571c-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="5571c-109">Определяет тип подобъекта.</span><span class="sxs-lookup"><span data-stu-id="5571c-109">Identifies the type of subobject.</span></span> <span data-ttu-id="5571c-110">Должен быть одним из поддерживаемых типов подобъектов HLSL.</span><span class="sxs-lookup"><span data-stu-id="5571c-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="5571c-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-112">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Поле [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="5571c-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="5571c-114">Поля подобъекта.</span><span class="sxs-lookup"><span data-stu-id="5571c-114">Fields of the subobject.</span></span> <span data-ttu-id="5571c-115">Ниже описаны конкретные поля для каждого типа подобъекта.</span><span class="sxs-lookup"><span data-stu-id="5571c-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="5571c-116">Список типов подобъектов:</span><span class="sxs-lookup"><span data-stu-id="5571c-116">List of subobject types:</span></span>
-   [<span data-ttu-id="5571c-117">статеобжектконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="5571c-118">глобалрутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="5571c-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="5571c-119">локалрутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="5571c-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="5571c-120">субобжекттоекспортсассокатион</span><span class="sxs-lookup"><span data-stu-id="5571c-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="5571c-121">райтраЦингшадерконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="5571c-122">райтраЦингпипелинеконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="5571c-123">трианглехитграуп</span><span class="sxs-lookup"><span data-stu-id="5571c-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="5571c-124">процедуралпримитивехитграуп</span><span class="sxs-lookup"><span data-stu-id="5571c-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="5571c-125">статеобжектконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-125">StateObjectConfig</span></span>

<span data-ttu-id="5571c-126">Тип подобъекта Статеобжектконфиг соответствует структуре [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .</span><span class="sxs-lookup"><span data-stu-id="5571c-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="5571c-127">У него есть одно поле, побитовый флаг, который является одним или обоими</span><span class="sxs-lookup"><span data-stu-id="5571c-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="5571c-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="5571c-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="5571c-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="5571c-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="5571c-130">или ноль ни для одного из них.</span><span class="sxs-lookup"><span data-stu-id="5571c-130">or, zero for neither of them.</span></span>

<span data-ttu-id="5571c-131">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="5571c-132">глобалрутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="5571c-132">GlobalRootSignature</span></span>
<span data-ttu-id="5571c-133">Глобалрутсигнатуре соответствует структуре [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="5571c-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="5571c-134">Поля состоят из нескольких строк, описывающих части корневой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="5571c-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="5571c-135">Справочные сведения об этом см. [в разделе Указание корневых подписей в HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="5571c-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="5571c-136">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="5571c-137">локалрутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="5571c-137">LocalRootSignature</span></span>
<span data-ttu-id="5571c-138">Локалрутсигнатуре соответствует структуре [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="5571c-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="5571c-139">Как и в случае с глобальным корневым объектом подписи, поля состоят из нескольких строк, описывающих части корневой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="5571c-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="5571c-140">Справочные сведения об этом см. [в разделе Указание корневых подписей в HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="5571c-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="5571c-141">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="5571c-142">субобжекттоекспортсассокатион</span><span class="sxs-lookup"><span data-stu-id="5571c-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="5571c-143">По умолчанию подобъект, только объявленный в той же библиотеке, что и экспорт, может применяться к этому экспорту.</span><span class="sxs-lookup"><span data-stu-id="5571c-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="5571c-144">Однако приложения имеют возможность переопределить это и получить конкретные сведения о том, какой из них выполняет экспорт.</span><span class="sxs-lookup"><span data-stu-id="5571c-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="5571c-145">В HLSL это "явная ассоциация" выполняется с помощью Субобжекттоекспортсассокатион.</span><span class="sxs-lookup"><span data-stu-id="5571c-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="5571c-146">Субобжекттоекспортсассокатион соответствует структуре [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .</span><span class="sxs-lookup"><span data-stu-id="5571c-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="5571c-147">Этот подобъект объявляется с помощью синтаксиса</span><span class="sxs-lookup"><span data-stu-id="5571c-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="5571c-148">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-148">Item</span></span>                                                                                         | <span data-ttu-id="5571c-149">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-151">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**субобжектнаме**</span><span class="sxs-lookup"><span data-stu-id="5571c-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="5571c-153">Строка, определяющая экспортированный подобъект.</span><span class="sxs-lookup"><span data-stu-id="5571c-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="5571c-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="5571c-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="5571c-155">Строка, содержащая разделенный точками с запятой список экспортов.</span><span class="sxs-lookup"><span data-stu-id="5571c-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="5571c-156">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="5571c-157">Обратите внимание, что в обоих полях используются *экспортированные* имена.</span><span class="sxs-lookup"><span data-stu-id="5571c-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="5571c-158">Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.</span><span class="sxs-lookup"><span data-stu-id="5571c-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="5571c-159">райтраЦингшадерконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="5571c-160">РайтраЦингшадерконфиг соответствует структуре [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .</span><span class="sxs-lookup"><span data-stu-id="5571c-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="5571c-161">Этот подобъект объявляется с помощью синтаксиса</span><span class="sxs-lookup"><span data-stu-id="5571c-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="5571c-162">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-162">Item</span></span>                                                                                         | <span data-ttu-id="5571c-163">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-165">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**макспайлоадсизе**</span><span class="sxs-lookup"><span data-stu-id="5571c-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="5571c-167">Числовое значение для максимального хранилища для скаляров (подсчитывается как 4 байта каждый) в полезных данных лучей для связанных шейдеров райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="5571c-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="5571c-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**максаттрибутесизе**</span><span class="sxs-lookup"><span data-stu-id="5571c-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="5571c-169">Числовое значение для максимального числа скаляров (подсчитывается как 4 байта), которое может использоваться для атрибутов в связанных шейдерах райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="5571c-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="5571c-170">Значение не может превышать [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span><span class="sxs-lookup"><span data-stu-id="5571c-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="5571c-171">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="5571c-172">райтраЦингпипелинеконфиг</span><span class="sxs-lookup"><span data-stu-id="5571c-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="5571c-173">РайтраЦингпипелинеконфиг соответствует структуре [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .</span><span class="sxs-lookup"><span data-stu-id="5571c-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="5571c-174">Этот подобъект объявляется с помощью синтаксиса</span><span class="sxs-lookup"><span data-stu-id="5571c-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="5571c-175">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-175">Item</span></span>                                                                                         | <span data-ttu-id="5571c-176">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-178">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**макстрацерекурсиондепс**</span><span class="sxs-lookup"><span data-stu-id="5571c-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="5571c-180">Числовой предел, используемый для рекурсии лучей в конвейере райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="5571c-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="5571c-181">Это число от 0 до 31 включительно.</span><span class="sxs-lookup"><span data-stu-id="5571c-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="5571c-182">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="5571c-183">Так как для рекурсии райтраЦинг существуют затраты на производительность, приложения должны использовать минимальную глубину рекурсии, необходимую для нужных результатов.</span><span class="sxs-lookup"><span data-stu-id="5571c-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="5571c-184">Если вызовы шейдера еще не достигли максимальной глубины рекурсии, они могут вызывать [трацерай](../direct3d12/traceray-function.md) любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="5571c-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="5571c-185">Но если они достигли или превышают максимальную глубину рекурсии, вызов Трацерай переводит устройство в состояние «удалено».</span><span class="sxs-lookup"><span data-stu-id="5571c-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="5571c-186">Таким образом, шейдеры райтраЦинг должны отказаться от вызова Трацерай, если они удовлетворены или превысили максимальную глубину рекурсии.</span><span class="sxs-lookup"><span data-stu-id="5571c-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="5571c-187">трианглехитграуп</span><span class="sxs-lookup"><span data-stu-id="5571c-187">TriangleHitGroup</span></span>

<span data-ttu-id="5571c-188">Трианглехитграуп соответствует структуре [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) , для которой в поле Type задано значение [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="5571c-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="5571c-189">Этот подобъект объявляется с помощью синтаксиса</span><span class="sxs-lookup"><span data-stu-id="5571c-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="5571c-190">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-190">Item</span></span>                                                                                         | <span data-ttu-id="5571c-191">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-193">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**анихитшадер**</span><span class="sxs-lookup"><span data-stu-id="5571c-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="5571c-195">Строковое имя шейдера анихит для группы попаданий или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5571c-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="5571c-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**клосесситшадер**</span><span class="sxs-lookup"><span data-stu-id="5571c-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="5571c-197">Строковое имя ближайшего шейдера нажатия для группы попаданий или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5571c-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="5571c-198">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="5571c-199">Обратите внимание, что в обоих полях используются *экспортированные* имена.</span><span class="sxs-lookup"><span data-stu-id="5571c-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="5571c-200">Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.</span><span class="sxs-lookup"><span data-stu-id="5571c-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="5571c-201">процедуралпримитивехитграуп</span><span class="sxs-lookup"><span data-stu-id="5571c-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="5571c-202">Процедуралпримитивехитграуп соответствует структуре [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) , для которой в поле Type задано значение [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="5571c-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="5571c-203">Этот подобъект объявляется с помощью синтаксиса</span><span class="sxs-lookup"><span data-stu-id="5571c-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="5571c-204">Элемент</span><span class="sxs-lookup"><span data-stu-id="5571c-204">Item</span></span>                                                                                         | <span data-ttu-id="5571c-205">Описание</span><span class="sxs-lookup"><span data-stu-id="5571c-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5571c-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5571c-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="5571c-207">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5571c-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="5571c-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**анихитшадер**</span><span class="sxs-lookup"><span data-stu-id="5571c-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="5571c-209">Строковое имя шейдера анихит для группы попаданий или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5571c-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="5571c-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**клосесситшадер**</span><span class="sxs-lookup"><span data-stu-id="5571c-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="5571c-211">Строковое имя ближайшего шейдера нажатия для группы попаданий или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5571c-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="5571c-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**интерсектионшадер**</span><span class="sxs-lookup"><span data-stu-id="5571c-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="5571c-213">Строковое имя шейдера пересечения для группы попаданий или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5571c-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="5571c-214">Пример</span><span class="sxs-lookup"><span data-stu-id="5571c-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="5571c-215">Обратите внимание, что в трех полях используются *экспортированные* имена.</span><span class="sxs-lookup"><span data-stu-id="5571c-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="5571c-216">Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.</span><span class="sxs-lookup"><span data-stu-id="5571c-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="5571c-217">Примечания</span><span class="sxs-lookup"><span data-stu-id="5571c-217">Remarks</span></span>

<span data-ttu-id="5571c-218">Подобъекты имеют понятие "Ассоциация" или "какой подобъект проходит с помощью экспорта".</span><span class="sxs-lookup"><span data-stu-id="5571c-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="5571c-219">При указании подобъектов с помощью кода шейдера выбирается параметр «какой подобъект проходит с экспортом» согласно правилам, описанным в [спецификации дкср](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="5571c-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="5571c-220">В частности, предположим, что в приложении есть экспорт.</span><span class="sxs-lookup"><span data-stu-id="5571c-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="5571c-221">Если приложение связывается с экспортом с корневой подписью A с помощью шейдера и корневой сигнатуры B с помощью кода приложения, то используется именно объект B.</span><span class="sxs-lookup"><span data-stu-id="5571c-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="5571c-222">Проектирование «использование B» вместо «создание ошибки» дает приложениям возможность удобно переопределять ассоциации ДКСИЛ с помощью кода приложения, а не принудительно перекомпилировать шейдеры для устранения несоответствий.</span><span class="sxs-lookup"><span data-stu-id="5571c-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5571c-223">См. также</span><span class="sxs-lookup"><span data-stu-id="5571c-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5571c-224">Запись блога разработчиков DirectX: "Новая возможность в D3D12 — DirectX РайтраЦинг (ДКСР) теперь поддерживает подобъекты библиотеки"</span><span class="sxs-lookup"><span data-stu-id="5571c-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="5571c-225">Функциональная спецификация DirectX РайтраЦинг (ДКСР)</span><span class="sxs-lookup"><span data-stu-id="5571c-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="5571c-226">Пример: D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="5571c-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>