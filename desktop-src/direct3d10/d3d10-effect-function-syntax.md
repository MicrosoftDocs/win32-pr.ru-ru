---
description: Функция Effect написана на HLSL и объявлена с помощью следующего синтаксиса.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Синтаксис функции Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496152"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="98190-103">Синтаксис функции Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="98190-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="98190-104">Функция Effect написана на HLSL и объявлена с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="98190-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="98190-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98190-105">Syntax</span></span>

<span data-ttu-id="98190-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="98190-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="98190-107">{</span><span class="sxs-lookup"><span data-stu-id="98190-107">{</span></span>

<dl> <span data-ttu-id="98190-108">\[ *Инструкции* \]</span><span class="sxs-lookup"><span data-stu-id="98190-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="98190-109">};</span><span class="sxs-lookup"><span data-stu-id="98190-109">};</span></span>



| <span data-ttu-id="98190-110">Имя</span><span class="sxs-lookup"><span data-stu-id="98190-110">Name</span></span>         | <span data-ttu-id="98190-111">Описание</span><span class="sxs-lookup"><span data-stu-id="98190-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98190-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="98190-112">ReturnType</span></span>   | <span data-ttu-id="98190-113">Любой [тип HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="98190-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="98190-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="98190-114">FunctionName</span></span> | <span data-ttu-id="98190-115">Строка ASCII, однозначно определяющая имя функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="98190-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="98190-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="98190-116">ArgumentList</span></span> | <span data-ttu-id="98190-117">Один или несколько аргументов, разделенных запятыми (см. раздел [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="98190-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="98190-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="98190-118">Statements</span></span>   | <span data-ttu-id="98190-119">Одна или несколько инструкций (см. [инструкции (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)), которые составляют тело функции.</span><span class="sxs-lookup"><span data-stu-id="98190-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="98190-120">Если функция определена без тела, она считается прототипом; и должны быть переопределены с телом перед использованием.</span><span class="sxs-lookup"><span data-stu-id="98190-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="98190-121">Функция Effect может быть шейдером или может просто быть функцией, вызываемой шейдером.</span><span class="sxs-lookup"><span data-stu-id="98190-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="98190-122">Функция однозначно идентифицируется по ее имени, типам ее параметров и целевой платформе. Поэтому функции могут быть перегружены.</span><span class="sxs-lookup"><span data-stu-id="98190-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="98190-123">Любая допустимая функция HLSL должна соответствовать этому формату; более подробный список синтаксиса для функций HLSL см. в разделе [функции (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="98190-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="98190-124">Пример</span><span class="sxs-lookup"><span data-stu-id="98190-124">Example</span></span>

<span data-ttu-id="98190-125">В [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) используется шейдер пикселей и шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="98190-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="98190-126">Функция шейдера пикселей называется Рендерсценепс и показана ниже.</span><span class="sxs-lookup"><span data-stu-id="98190-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="98190-127">См. также</span><span class="sxs-lookup"><span data-stu-id="98190-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98190-128">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="98190-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
