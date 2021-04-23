---
title: Использование этапа Input-Assembler без буферов
description: Создание и привязка буферов не требуется, если шейдеры не требуют буферов. В этом разделе содержится пример простых шейдеров вершин и пикселей, которые рисуют один треугольник.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3aa4c63176d184e1e67349149bd1f4044159e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983637"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a><span data-ttu-id="22a33-104">Использование этапа Input-Assembler без буферов</span><span class="sxs-lookup"><span data-stu-id="22a33-104">Using the Input-Assembler Stage without Buffers</span></span>

<span data-ttu-id="22a33-105">Создание и привязка буферов не требуется, если шейдеры не требуют буферов.</span><span class="sxs-lookup"><span data-stu-id="22a33-105">Creating and binding buffers is not necessary if your shaders don't require buffers.</span></span> <span data-ttu-id="22a33-106">В этом разделе содержится пример простых шейдеров вершин и пикселей, которые рисуют один треугольник.</span><span class="sxs-lookup"><span data-stu-id="22a33-106">This section contains an example of simple vertex and pixel shaders that draw a single triangle.</span></span>

-   [<span data-ttu-id="22a33-107">Шейдер вершин</span><span class="sxs-lookup"><span data-stu-id="22a33-107">Vertex Shader</span></span>](#vertex-shader)
-   [<span data-ttu-id="22a33-108">Шейдер пикселей</span><span class="sxs-lookup"><span data-stu-id="22a33-108">Pixel Shader</span></span>](#pixel-shader)
-   [<span data-ttu-id="22a33-109">Метод</span><span class="sxs-lookup"><span data-stu-id="22a33-109">Technique</span></span>](#technique)
-   [<span data-ttu-id="22a33-110">Код приложения</span><span class="sxs-lookup"><span data-stu-id="22a33-110">Application Code</span></span>](#application-code)
-   [<span data-ttu-id="22a33-111">См. также</span><span class="sxs-lookup"><span data-stu-id="22a33-111">Related topics</span></span>](#related-topics)

## <a name="vertex-shader"></a><span data-ttu-id="22a33-112">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="22a33-112">Vertex Shader</span></span>

<span data-ttu-id="22a33-113">Например, можно объявить шейдер вершин, который создает собственные вершины.</span><span class="sxs-lookup"><span data-stu-id="22a33-113">For example, you could declare a vertex shader that creates its own vertices.</span></span>


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a><span data-ttu-id="22a33-114">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="22a33-114">Pixel Shader</span></span>


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a><span data-ttu-id="22a33-115">Метод</span><span class="sxs-lookup"><span data-stu-id="22a33-115">Technique</span></span>

<span data-ttu-id="22a33-116">Метод — это набор этапов отрисовки (должен быть хотя бы один проход).</span><span class="sxs-lookup"><span data-stu-id="22a33-116">A technique is a collection of rendering passes (there must be at least one pass).</span></span>


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a><span data-ttu-id="22a33-117">Код приложения</span><span class="sxs-lookup"><span data-stu-id="22a33-117">Application Code</span></span>


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a><span data-ttu-id="22a33-118">См. также</span><span class="sxs-lookup"><span data-stu-id="22a33-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22a33-119">Начало работы с этапом Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="22a33-119">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




