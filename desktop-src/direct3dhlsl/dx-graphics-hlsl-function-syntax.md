---
title: Синтаксис объявления функций
description: Функции HLSL объявляются с помощью следующего синтаксиса.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2781d173eb4a1c18a661495d9fb55a0cced81921
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998331"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="01fd1-103">Синтаксис объявления функций</span><span class="sxs-lookup"><span data-stu-id="01fd1-103">Function Declaration Syntax</span></span>

<span data-ttu-id="01fd1-104">Функции HLSL объявляются с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="01fd1-104">HLSL functions are declared with the following syntax.</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fd1-105">\[*Сторажекласс* \] \[клиппланес () \] \[ точное \] \_ *имя* возвращаемого значения ( \[ *ArgumentList* \] ) \[ : *семантика* \] { \[ *статементблокк* \] };</span><span class="sxs-lookup"><span data-stu-id="01fd1-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="01fd1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01fd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fd1-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*сторажекласс*</span><span class="sxs-lookup"><span data-stu-id="01fd1-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-108">Модификатор, который переопределяет объявление функции.</span><span class="sxs-lookup"><span data-stu-id="01fd1-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="01fd1-109">в настоящее время **подставляемое** значение является единственным значением модификатора.</span><span class="sxs-lookup"><span data-stu-id="01fd1-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="01fd1-110">Значение модификатора должно быть **встроенным** , поскольку оно также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01fd1-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="01fd1-111">Поэтому функция является встроенной, независимо от того, задано ли значение **inline**, и все функции в HLSL являются встроенными.</span><span class="sxs-lookup"><span data-stu-id="01fd1-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="01fd1-112">Встроенная функция создает копию тела функции (при компиляции) для каждого вызова функции.</span><span class="sxs-lookup"><span data-stu-id="01fd1-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="01fd1-113">Это делается для снижения издержек при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="01fd1-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="01fd1-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*клиппланес*</span><span class="sxs-lookup"><span data-stu-id="01fd1-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-115">Необязательный список плоскостей, который имеет до 6 заданных пользователем плоскостей.</span><span class="sxs-lookup"><span data-stu-id="01fd1-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="01fd1-116">Это альтернативный механизм для [SV \_ клипдистанце](dx-graphics-hlsl-semantics.md) , который работает на [уровне функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x и выше.</span><span class="sxs-lookup"><span data-stu-id="01fd1-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="01fd1-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="01fd1-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-118">Строка ASCII, однозначно определяющая имя функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="01fd1-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="01fd1-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="01fd1-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-120">Необязательный список аргументов, который представляет собой разделенный запятыми список [аргументов](dx-graphics-hlsl-function-parameters.md) , передаваемых в функцию.</span><span class="sxs-lookup"><span data-stu-id="01fd1-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="01fd1-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Семантическ*</span><span class="sxs-lookup"><span data-stu-id="01fd1-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-122">Необязательная строка, которая определяет предполагаемое использование возвращаемых данных (см. раздел [семантика (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="01fd1-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="01fd1-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*статементблокк*</span><span class="sxs-lookup"><span data-stu-id="01fd1-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="01fd1-124">Необязательные [инструкции](dx-graphics-hlsl-statement-blocks.md) , составляющие тело функции.</span><span class="sxs-lookup"><span data-stu-id="01fd1-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="01fd1-125">Функция, определенная без тела, называется прототипом функции; тело функции прототипа должно быть определено в любом расположении, прежде чем можно будет вызвать функцию.</span><span class="sxs-lookup"><span data-stu-id="01fd1-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fd1-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01fd1-126">Return Value</span></span>

<span data-ttu-id="01fd1-127">Тип возвращаемого значения может быть любым из следующих [типов HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="01fd1-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01fd1-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="01fd1-128">Remarks</span></span>

<span data-ttu-id="01fd1-129">Синтаксис на этой странице описывает почти все типы функций HLSL, включая шейдеры вершин, шейдеры пикселей и вспомогательные функции.</span><span class="sxs-lookup"><span data-stu-id="01fd1-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="01fd1-130">Хотя шейдер Geometry также реализован с помощью функции, его синтаксис немного сложнее, поэтому существует отдельная страница, определяющая объявление функции шейдера Geometry (см. раздел [объект Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="01fd1-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="01fd1-131">Функцию можно перегрузить при условии, что ей присваивается уникальное сочетание типов параметров и (или) порядка параметров.</span><span class="sxs-lookup"><span data-stu-id="01fd1-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="01fd1-132">HLSL также реализует ряд встроенных или [**встроенных функций**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="01fd1-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="01fd1-133">С помощью атрибута **клиппланес** можно указать определенные пользователем плоскости.</span><span class="sxs-lookup"><span data-stu-id="01fd1-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="01fd1-134">Windows применяет эти элементы обрезки ко всем рисуемым примитивам.</span><span class="sxs-lookup"><span data-stu-id="01fd1-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="01fd1-135">Атрибут **клиппланес** работает так же, как [SV \_ клипдистанце](dx-graphics-hlsl-semantics.md) , но работает на всех [уровнях компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) оборудования 9 \_ x и выше.</span><span class="sxs-lookup"><span data-stu-id="01fd1-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="01fd1-136">Дополнительные сведения см. [в статье пользовательские ролики на устройствах на уровне компонентов 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span><span class="sxs-lookup"><span data-stu-id="01fd1-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="01fd1-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="01fd1-137">Examples</span></span>

<span data-ttu-id="01fd1-138">Этот пример относится к BasicHLSL10. FX из [примера BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="01fd1-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="01fd1-139">В этом примере из Адванцедпартиклес. FX из [примера адванцедпартиклес](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)демонстрируется использование семантики для возвращаемого типа.</span><span class="sxs-lookup"><span data-stu-id="01fd1-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="01fd1-140">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01fd1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01fd1-141">Функции (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01fd1-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
