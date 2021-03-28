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
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983757"
---
# <a name="return-statement"></a><span data-ttu-id="ff75a-104">Оператор return</span><span class="sxs-lookup"><span data-stu-id="ff75a-104">return Statement</span></span>

<span data-ttu-id="ff75a-105">Оператор Return сообщает об окончании функции.</span><span class="sxs-lookup"><span data-stu-id="ff75a-105">A return statement signals the end of a function.</span></span>



|                   |
|-------------------|
| <span data-ttu-id="ff75a-106">возвращаемое \[ значение \] ;</span><span class="sxs-lookup"><span data-stu-id="ff75a-106">return \[value\];</span></span> |



 

<span data-ttu-id="ff75a-107">Простейший оператор return возвращает управление из функции в вызывающую программу; Он не возвращает значения.</span><span class="sxs-lookup"><span data-stu-id="ff75a-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="ff75a-108">Однако оператор return может возвращать одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="ff75a-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="ff75a-109">В этом примере возвращается литеральное значение:</span><span class="sxs-lookup"><span data-stu-id="ff75a-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="ff75a-110">Этот пример возвращает скалярный результат выражения.</span><span class="sxs-lookup"><span data-stu-id="ff75a-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="ff75a-111">Этот пример возвращает вектор из четырех компонентов, созданный из локальной переменной и литерала.</span><span class="sxs-lookup"><span data-stu-id="ff75a-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="ff75a-112">Этот пример возвращает вектор из четырех компонентов, созданный из результата, возвращаемого из встроенной функции, вместе с литеральными значениями.</span><span class="sxs-lookup"><span data-stu-id="ff75a-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="ff75a-113">В этом примере возвращается структура, содержащая один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="ff75a-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="ff75a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff75a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff75a-115">Функции (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff75a-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




