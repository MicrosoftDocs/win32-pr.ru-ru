---
title: Модель шейдера HLSL 5
description: Модель шейдера HLSL 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890780"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="b87c5-103">Модель шейдера HLSL 5</span><span class="sxs-lookup"><span data-stu-id="b87c5-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="b87c5-104">В этом разделе содержится обзорный материал для языка High-Level шейдера, в частности новые функции в модели шейдеров 5, появившиеся в Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b87c5-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b87c5-105">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="b87c5-105">In This Section</span></span>



| <span data-ttu-id="b87c5-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="b87c5-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b87c5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b87c5-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87c5-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Динамическая компоновка](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="b87c5-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="b87c5-109">Динамическое связывание позволяет среде выполнения принимать решение во время рисования (а не во время компиляции) о том, какой путь кода следует запустить.</span><span class="sxs-lookup"><span data-stu-id="b87c5-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="b87c5-110">Это сокращает проблему распространения шейдера, вызванную появлением шейдеров практически идентичными входными сигнатурами.</span><span class="sxs-lookup"><span data-stu-id="b87c5-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="b87c5-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Функции шейдера Geometry](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="b87c5-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="b87c5-112">Новые функции шейдера Geometry, в том числе: создание экземпляров, которое обеспечивает повышение производительности, когда порядок примитивов в потоке не имеет значения, и несколько потоков вывода, поэтому шейдер может выводить вершины в нескольких потоках.</span><span class="sxs-lookup"><span data-stu-id="b87c5-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="b87c5-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Тесселяции](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="b87c5-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="b87c5-114">Среда выполнения Direct3D 11 поддерживает три новых этапа, реализующих тесселяцию, которая преобразует поверхности подразделений с низким уровнем детализации в примитивы более высокого уровня для GPU.</span><span class="sxs-lookup"><span data-stu-id="b87c5-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="b87c5-115">Тесселяции разбивает на плитки поверхности старшего порядка на структуры, подходящие для прорисовки.</span><span class="sxs-lookup"><span data-stu-id="b87c5-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="b87c5-116">Три этапа тесселяции: поверхности-шейдер, тесселяция и поэтапный шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="b87c5-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="b87c5-117">Кроме того, в разделе Reference рассматриваются многие новые элементы API для Shader Model 5, включая [атрибуты](d3d11-graphics-reference-sm5-attributes.md), [встроенные функции](d3d11-graphics-reference-sm5-intrinsics.md), [объекты и методы модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md), а также [системные значения](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="b87c5-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b87c5-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b87c5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b87c5-119">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="b87c5-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

