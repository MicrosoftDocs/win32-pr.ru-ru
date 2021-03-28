---
title: Шейдерный язык HLSL
description: HLSL — это язык шейдера высокого уровня, который можно использовать с программируемыми шейдерами в DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986181"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="178fa-103">Шейдерный язык HLSL</span><span class="sxs-lookup"><span data-stu-id="178fa-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="178fa-104">HLSL — это язык шейдера высокого уровня, который можно использовать с программируемыми шейдерами в DirectX.</span><span class="sxs-lookup"><span data-stu-id="178fa-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="178fa-105">Например, можно использовать HLSL для создания [шейдера вершин](../direct3d11/vertex-shader-stage.md)или [шейдера пикселей](../direct3d11/pixel-shader-stage.md)и использовать эти шейдеры в реализации модуля подготовки отчетов в приложении [Direct3D](../direct3d12/directx-12-programming-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="178fa-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="178fa-106">Или можно использовать HLSL для создания шейдера вычислений, возможно, для реализации модели физикы.</span><span class="sxs-lookup"><span data-stu-id="178fa-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="178fa-107">Однако если, например, вы заметите собственный оператор свертки (для обработки изображений) как HLSL в вычислительном шейдере, вы получите лучшую производительность в этом сценарии, если вместо этого используется [Direct машинное обучение (директмл)](../direct3d12/dml.md) .</span><span class="sxs-lookup"><span data-stu-id="178fa-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="178fa-108">HLSL был создан (начиная с версии DirectX 9), чтобы настроить программируемый трехмерный [конвейер](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="178fa-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="178fa-109">Вы можете программировать весь конвейер с помощью инструкций HLSL.</span><span class="sxs-lookup"><span data-stu-id="178fa-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="178fa-110">Далее</span><span class="sxs-lookup"><span data-stu-id="178fa-110">Where to go next</span></span>

* [<span data-ttu-id="178fa-111">Инструкции по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="178fa-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="178fa-112">Справочник по HLSL</span><span class="sxs-lookup"><span data-stu-id="178fa-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="178fa-113">Инструкции по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="178fa-113">Programming guide for HLSL</span></span>

<span data-ttu-id="178fa-114">Основные сведения о HLSL см. в разделе " [инструкции по программированию для HLSL](./dx-graphics-hlsl-pguide.md)".</span><span class="sxs-lookup"><span data-stu-id="178fa-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="178fa-115">Руководство по программированию описывает различные виды этапов шейдера, а также создание, компиляцию, оптимизацию, привязку и связывание шейдеров.</span><span class="sxs-lookup"><span data-stu-id="178fa-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="178fa-116">Кроме того, вы найдете обзоры и заметки о выпуске, посвященные последующим поколениям версии модели шейдеров, которые были выпущены, и вернемся к модели шейдера HLSL 5.</span><span class="sxs-lookup"><span data-stu-id="178fa-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="178fa-117">Справочник по HLSL</span><span class="sxs-lookup"><span data-stu-id="178fa-117">Reference for HLSL</span></span>

<span data-ttu-id="178fa-118">Справочную документацию по HLSL см. в [справочнике по HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="178fa-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="178fa-119">В разделе Reference содержится полный список синтаксиса языка и встроенных функций, встроенных в HLSL для упрощения требований к написанию кода.</span><span class="sxs-lookup"><span data-stu-id="178fa-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="178fa-120">Кроме того, здесь можно найти обсуждение моделей шейдеров и профилей, а также справочное содержимое модели шейдера, которое будет возвращаться к модели шейдера HLSL 1.</span><span class="sxs-lookup"><span data-stu-id="178fa-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="178fa-121">Есть также содержимое, охватывающее инструкции по сборке, средство D3DCompiler и сведения об ошибках и предупреждениях, которые может возвращать шейдер.</span><span class="sxs-lookup"><span data-stu-id="178fa-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>