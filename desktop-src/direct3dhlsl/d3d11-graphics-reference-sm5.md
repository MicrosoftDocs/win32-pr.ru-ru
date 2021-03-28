---
title: Модель шейдера 5
description: Этот раздел содержит справочные страницы для HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413158"
---
# <a name="shader-model-5"></a><span data-ttu-id="9a66a-103">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9a66a-103">Shader Model 5</span></span>

<span data-ttu-id="9a66a-104">Этот раздел содержит справочные страницы для HLSL Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="9a66a-105">Shader Model 5 является надмножеством возможности в [модели шейдера 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="9a66a-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="9a66a-106">Она была разработана с использованием ядра общего шейдера, предоставляющего общий набор функций для всех программируемых шейдеров, которые можно программировать только с помощью HLSL.</span><span class="sxs-lookup"><span data-stu-id="9a66a-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="9a66a-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="9a66a-107">Feature</span></span>                   | <span data-ttu-id="9a66a-108">Возможностями.</span><span class="sxs-lookup"><span data-stu-id="9a66a-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a66a-109">Набор инструкций</span><span class="sxs-lookup"><span data-stu-id="9a66a-109">Instruction Set</span></span>           | [<span data-ttu-id="9a66a-110">**Встроенные функции HLSL**</span><span class="sxs-lookup"><span data-stu-id="9a66a-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="9a66a-111">Максимум вершинного шейдера</span><span class="sxs-lookup"><span data-stu-id="9a66a-111">Vertex Shader Max</span></span>         | <span data-ttu-id="9a66a-112">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="9a66a-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="9a66a-113">Максимальный размер шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="9a66a-113">Pixel Shader Max</span></span>          | <span data-ttu-id="9a66a-114">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="9a66a-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="9a66a-115">Добавлены новые профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="9a66a-115">New Shader Profiles Added</span></span> | <span data-ttu-id="9a66a-116">CS \_ 4 \_ 0, GS \_ 4 \_ 0, \* PS \_ 4 \_ 0 \* , VS \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , VS \_ 4 \_ 1 \* , CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 0, HS 5 0, \_ \_ \_ PS \_ 5 \_ 0, VS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a66a-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="9a66a-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS 4 0 \_ \_ , PS \_ 4 1 \_ , VS \_ 4 \_ 0 и vs \_ 4 \_ 1 были введены в модель шейдеров 4,0, однако в DirectX 11 добавлена поддержка [структурированных буферов](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) и буферов байтовых адресов для модели шейдеров 4, работающей на оборудовании DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="9a66a-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="9a66a-118">В модели шейдеров 5 появился [вычислительный шейдер](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) , который обеспечивает высокоскоростные вычисления общего назначения.</span><span class="sxs-lookup"><span data-stu-id="9a66a-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="9a66a-119">Более полный список функций шейдера 5 включен в список [функций Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).</span><span class="sxs-lookup"><span data-stu-id="9a66a-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="9a66a-120">В разделе [Assembly модель шейдеров 5](shader-model-5-assembly--directx-hlsl-.md) описаны инструкции ассемблера, поддерживаемые моделью шейдеров 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9a66a-121">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="9a66a-121">In This Section</span></span>



| <span data-ttu-id="9a66a-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a66a-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="9a66a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9a66a-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9a66a-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="9a66a-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="9a66a-125">Справочные страницы для атрибутов Shader модели 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="9a66a-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Встроенные функции модели шейдеров 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="9a66a-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="9a66a-127">Справочные страницы для встроенных функций модели шейдеров 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="9a66a-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="9a66a-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="9a66a-129">Справочные страницы для объектов и методов модели шейдеров 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="9a66a-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Системные значения модели шейдеров 5](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="9a66a-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="9a66a-131">Справочные страницы для системных значений модели шейдеров 5.</span><span class="sxs-lookup"><span data-stu-id="9a66a-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="9a66a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="9a66a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a66a-133">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="9a66a-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

