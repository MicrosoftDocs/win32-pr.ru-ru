---
title: Вспомогательные методы HLSL
description: Чтобы помочь авторам повлиять на написание построителей шейдеров пикселей, d2d1effecthelpers. hlsli определяет набор расширений языка HLSL в виде вспомогательных методов и макросов.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986242"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="fd154-103">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="fd154-103">HLSL Helpers</span></span>

<span data-ttu-id="fd154-104">Чтобы помочь авторам повлиять на написание построителей шейдеров пикселей, d2d1effecthelpers. hlsli определяет набор расширений языка HLSL в виде вспомогательных методов и макросов.</span><span class="sxs-lookup"><span data-stu-id="fd154-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="fd154-105">Чтобы добавить d2d1effecthelpers. hlsli в проект, добавьте \# инструкцию include в файл HLSL.</span><span class="sxs-lookup"><span data-stu-id="fd154-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="fd154-106">d2d1effecthelpers. hlsli находится в том же расположении, что и другие заголовки Direct2D, такие как D2D1. h; для ссылки на него можно использовать страницу свойств файла HLSL, добавив макрос $ (Виндовссдк \_ IncludePath) в свойство Дополнительные каталоги включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="fd154-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="fd154-107">Обратите внимание, что \# оператор include должен следовать после всех директив препроцессора, таких как \_ число входов D2D \_ .</span><span class="sxs-lookup"><span data-stu-id="fd154-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="fd154-108">Direct2D не поддерживает связывание вычислений или шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="fd154-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="fd154-109">Однако если в результате используется и шейдер вершин, и шейдер пикселей, выходные данные шейдера пикселей по-прежнему могут быть связаны.</span><span class="sxs-lookup"><span data-stu-id="fd154-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="fd154-110">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="fd154-110">Preprocessor Directives</span></span>

<span data-ttu-id="fd154-111">Для передачи сведений об этом действии требуются директивы препроцессора.</span><span class="sxs-lookup"><span data-stu-id="fd154-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="fd154-112">Сюда входит число входов и тип выборки для каждого входного значения.</span><span class="sxs-lookup"><span data-stu-id="fd154-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="fd154-113">Следующие значения должны быть определены в коде шейдера эффектов над соответствующей точкой входа шейдера, когда это применимо.</span><span class="sxs-lookup"><span data-stu-id="fd154-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="fd154-114">`D2D_INPUT_COUNT <N>` : Объявляет количество входных данных текстуры для результата.</span><span class="sxs-lookup"><span data-stu-id="fd154-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="fd154-115">Если результат имеет переменное число входов, это значение должно быть соответствующим образом ограничено каждой точкой входа шейдера.</span><span class="sxs-lookup"><span data-stu-id="fd154-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="fd154-116">Определение этого значения является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fd154-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="fd154-117">`D2D_INPUT<N>_SIMPLE` : Объявляет n входных данных для использования простой выборки.</span><span class="sxs-lookup"><span data-stu-id="fd154-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="fd154-118">Если не определено, по умолчанию используется значение n.</span><span class="sxs-lookup"><span data-stu-id="fd154-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="fd154-119">Определение этого значения является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd154-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="fd154-120">`D2D_INPUT<N>_COMPLEX` : Объявляет n входных данных для использования сложной выборки.</span><span class="sxs-lookup"><span data-stu-id="fd154-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="fd154-121">Если не определено, по умолчанию используется значение n.</span><span class="sxs-lookup"><span data-stu-id="fd154-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="fd154-122">Определение этого значения является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd154-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="fd154-123">`D2D_REQUIRES_SCENE_POSITION` : Указывает, что функция шейдера вызывает вспомогательные методы, использующие значение расположения сцены (а именно, вспомогательную функцию [D2DGetScenePosition](d2dgetsceneposition.md) ).</span><span class="sxs-lookup"><span data-stu-id="fd154-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="fd154-124">Этот параметр следует включать только при необходимости, так как только одна функция на связанный шейдер может использовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fd154-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="fd154-125">Определение этого значения является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd154-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="fd154-126">`D2D_CUSTOM_ENTRY` : Указывает, что функция шейдера пикселей использует выходные данные пользовательского шейдера вершин и, таким образом, объявляет свои входные параметры.</span><span class="sxs-lookup"><span data-stu-id="fd154-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="fd154-127">Все пользовательские входные шейдеры вершин используют сложную выборку и не могут использовать выходные данные другой функции шейдера (т. е. они доступны только после компоновки).</span><span class="sxs-lookup"><span data-stu-id="fd154-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="fd154-128">Определение этого значения является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd154-128">Defining this value is optional.</span></span>

<span data-ttu-id="fd154-129">Пример:</span><span class="sxs-lookup"><span data-stu-id="fd154-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="fd154-130">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="fd154-130">Helper Functions</span></span>

<span data-ttu-id="fd154-131">Вспомогательные функции используются в качестве замены для некоторых встроенных функций HLSL.</span><span class="sxs-lookup"><span data-stu-id="fd154-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="fd154-132">Во время компиляции эти вспомогательные функции переопределяются Direct2D в соответствующую версию в зависимости от типа целевого объекта компиляции (полного шейдера или функции экспорта).</span><span class="sxs-lookup"><span data-stu-id="fd154-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="fd154-133">Вспомогательные функции:</span><span class="sxs-lookup"><span data-stu-id="fd154-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="fd154-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="fd154-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="fd154-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="fd154-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="fd154-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="fd154-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="fd154-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="fd154-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="fd154-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="fd154-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="fd154-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="fd154-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="fd154-140">\_Запись D2D PS \_</span><span class="sxs-lookup"><span data-stu-id="fd154-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="fd154-141">См. также</span><span class="sxs-lookup"><span data-stu-id="fd154-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd154-142">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="fd154-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




