---
title: Синтаксис функции Effect (Direct3D 11)
description: Функция Effect написана на HLSL и объявлена с синтаксисом, описанным в этом разделе.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791683"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="5fa71-103">Синтаксис функции Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="5fa71-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="5fa71-104">Функция Effect написана на HLSL и объявлена с синтаксисом, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5fa71-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa71-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fa71-105">Syntax</span></span>

<span data-ttu-id="5fa71-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="5fa71-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="5fa71-107">{</span><span class="sxs-lookup"><span data-stu-id="5fa71-107">{</span></span>

<dl> <span data-ttu-id="5fa71-108">\[ *Операторы* \]</span><span class="sxs-lookup"><span data-stu-id="5fa71-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="5fa71-109">};</span><span class="sxs-lookup"><span data-stu-id="5fa71-109">};</span></span>



| <span data-ttu-id="5fa71-110">Имя</span><span class="sxs-lookup"><span data-stu-id="5fa71-110">Name</span></span>         | <span data-ttu-id="5fa71-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5fa71-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa71-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="5fa71-112">ReturnType</span></span>   | <span data-ttu-id="5fa71-113">Любой [тип HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="5fa71-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="5fa71-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="5fa71-114">FunctionName</span></span> | <span data-ttu-id="5fa71-115">Строка ASCII, однозначно определяющая имя функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="5fa71-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="5fa71-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="5fa71-116">ArgumentList</span></span> | <span data-ttu-id="5fa71-117">Один или несколько аргументов, разделенных запятыми (см. раздел [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="5fa71-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="5fa71-118">Операторы</span><span class="sxs-lookup"><span data-stu-id="5fa71-118">Statements</span></span>   | <span data-ttu-id="5fa71-119">Одна или несколько инструкций (см. [инструкции (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)), которые составляют тело функции.</span><span class="sxs-lookup"><span data-stu-id="5fa71-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="5fa71-120">Если функция определена без тела, она считается прототипом; и должны быть переопределены с телом перед использованием.</span><span class="sxs-lookup"><span data-stu-id="5fa71-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="5fa71-121">Функция Effect может быть шейдером или может просто быть функцией, вызываемой шейдером.</span><span class="sxs-lookup"><span data-stu-id="5fa71-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="5fa71-122">Функция однозначно идентифицируется по ее имени, типам ее параметров и целевой платформе. Поэтому функции могут быть перегружены.</span><span class="sxs-lookup"><span data-stu-id="5fa71-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="5fa71-123">Любая допустимая функция HLSL должна соответствовать этому формату; более подробный список синтаксиса для функций HLSL см. в разделе [функции (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="5fa71-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="5fa71-124">Например, .</span><span class="sxs-lookup"><span data-stu-id="5fa71-124">Example</span></span>

<span data-ttu-id="5fa71-125">Ниже приведен пример функции шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="5fa71-125">The following is an example of a pixel shader function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5fa71-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5fa71-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fa71-127">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="5fa71-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 