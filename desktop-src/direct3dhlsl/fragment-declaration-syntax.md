---
title: Синтаксис объявления фрагмента (Direct3D 9 HLSL)
description: Каждая функция языка шейдера высокого уровня (HLSL) может быть преобразована в фрагмент шейдера с добавлением объявления фрагмента.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998311"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="a46a1-103">Синтаксис объявления фрагмента (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="a46a1-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="a46a1-104">Каждая функция языка шейдера высокого уровня (HLSL) может быть преобразована в фрагмент шейдера с добавлением объявления фрагмента.</span><span class="sxs-lookup"><span data-stu-id="a46a1-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a46a1-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="a46a1-106">где:</span><span class="sxs-lookup"><span data-stu-id="a46a1-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46a1-107">фрагменткэйворд</span><span class="sxs-lookup"><span data-stu-id="a46a1-107">fragmentKeyword</span></span>   | <span data-ttu-id="a46a1-108">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="a46a1-108">Required keyword.</span></span> <span data-ttu-id="a46a1-109">Либо пикселфрагмент, либо вертексфрагмент.</span><span class="sxs-lookup"><span data-stu-id="a46a1-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a46a1-110">фрагментнаме</span><span class="sxs-lookup"><span data-stu-id="a46a1-110">FragmentName</span></span>      | <span data-ttu-id="a46a1-111">Текстовая строка ASCII, указывающая имя скомпилированного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="a46a1-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="a46a1-112">компилировать \_ фрагмент</span><span class="sxs-lookup"><span data-stu-id="a46a1-112">compile\_fragment</span></span> | <span data-ttu-id="a46a1-113">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="a46a1-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="a46a1-114">шадерпрофиле</span><span class="sxs-lookup"><span data-stu-id="a46a1-114">shaderProfile</span></span>     | <span data-ttu-id="a46a1-115">Модель шейдера для компиляции.</span><span class="sxs-lookup"><span data-stu-id="a46a1-115">The shader model to compile against.</span></span> <span data-ttu-id="a46a1-116">Любой допустимый профиль шейдера вершин (см. [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) или профиль шейдера пикселей (см. [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="a46a1-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="a46a1-117">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="a46a1-117">FunctionName()</span></span>    | <span data-ttu-id="a46a1-118">Имя функции шейдера, а затем круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="a46a1-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="a46a1-119">Параметры общего фрагмента помечаются путем добавления \_ префикса "r" к их семантике.</span><span class="sxs-lookup"><span data-stu-id="a46a1-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="a46a1-120">В этом примере \_ семантика r посворлд и r \_ нормалворлд определяют, что эти два параметра являются общими параметрами между другими фрагментами.</span><span class="sxs-lookup"><span data-stu-id="a46a1-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="a46a1-121">Компоновщик фрагментов был технологией Microsoft Direct3D 9 в D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="a46a1-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="a46a1-122">Компоновщик фрагментов был средством (Flink.exe), API D3DX 9 и усовершенствованием HLSL.</span><span class="sxs-lookup"><span data-stu-id="a46a1-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="a46a1-123">Компоновщик фрагментов был удален в выпуске пакета SDK DirectX за Август 2009.</span><span class="sxs-lookup"><span data-stu-id="a46a1-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="a46a1-124">Компоновщик фрагментов никогда не применяется к Microsoft Direct3D 10, Microsoft Direct3D 10,1 или Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a46a1-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a46a1-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a46a1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a46a1-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a46a1-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
