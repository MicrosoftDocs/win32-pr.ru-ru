---
title: Оператор return
description: Оператор Return сообщает об окончании функции.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Оператор Return HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119589"
---
# <a name="return-statement"></a><span data-ttu-id="3f49c-104">Оператор return</span><span class="sxs-lookup"><span data-stu-id="3f49c-104">return Statement</span></span>

<span data-ttu-id="3f49c-105">Оператор Return сообщает об окончании функции.</span><span class="sxs-lookup"><span data-stu-id="3f49c-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="3f49c-106">возвращаемое \[ значение \] ;</span><span class="sxs-lookup"><span data-stu-id="3f49c-106">return \[value\];</span></span>



 

<span data-ttu-id="3f49c-107">Простейший оператор return возвращает управление из функции в вызывающую программу; Он не возвращает значения.</span><span class="sxs-lookup"><span data-stu-id="3f49c-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="3f49c-108">Однако оператор return может возвращать одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="3f49c-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="3f49c-109">В этом примере возвращается литеральное значение:</span><span class="sxs-lookup"><span data-stu-id="3f49c-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="3f49c-110">Этот пример возвращает скалярный результат выражения.</span><span class="sxs-lookup"><span data-stu-id="3f49c-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="3f49c-111">Этот пример возвращает вектор из четырех компонентов, созданный из локальной переменной и литерала.</span><span class="sxs-lookup"><span data-stu-id="3f49c-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="3f49c-112">Этот пример возвращает вектор из четырех компонентов, созданный из результата, возвращаемого из встроенной функции, вместе с литеральными значениями.</span><span class="sxs-lookup"><span data-stu-id="3f49c-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="3f49c-113">В этом примере возвращается структура, содержащая один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="3f49c-113">This example returns a structure that contains one or more members.</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a><span data-ttu-id="3f49c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3f49c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f49c-115">Функции (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f49c-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




