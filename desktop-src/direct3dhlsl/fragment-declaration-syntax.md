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
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825731"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="47088-103">Синтаксис объявления фрагмента (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="47088-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="47088-104">Каждая функция языка шейдера высокого уровня (HLSL) может быть преобразована в фрагмент шейдера с добавлением объявления фрагмента.</span><span class="sxs-lookup"><span data-stu-id="47088-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="47088-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47088-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="47088-106">где:</span><span class="sxs-lookup"><span data-stu-id="47088-106">where:</span></span>



| <span data-ttu-id="47088-107">Значение</span><span class="sxs-lookup"><span data-stu-id="47088-107">Value</span></span>                  | <span data-ttu-id="47088-108">Описание</span><span class="sxs-lookup"><span data-stu-id="47088-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47088-109">фрагменткэйворд</span><span class="sxs-lookup"><span data-stu-id="47088-109">fragmentKeyword</span></span>   | <span data-ttu-id="47088-110">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="47088-110">Required keyword.</span></span> <span data-ttu-id="47088-111">Либо пикселфрагмент, либо вертексфрагмент.</span><span class="sxs-lookup"><span data-stu-id="47088-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="47088-112">фрагментнаме</span><span class="sxs-lookup"><span data-stu-id="47088-112">FragmentName</span></span>      | <span data-ttu-id="47088-113">Текстовая строка ASCII, указывающая имя скомпилированного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="47088-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="47088-114">компилировать \_ фрагмент</span><span class="sxs-lookup"><span data-stu-id="47088-114">compile\_fragment</span></span> | <span data-ttu-id="47088-115">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="47088-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="47088-116">шадерпрофиле</span><span class="sxs-lookup"><span data-stu-id="47088-116">shaderProfile</span></span>     | <span data-ttu-id="47088-117">Модель шейдера для компиляции.</span><span class="sxs-lookup"><span data-stu-id="47088-117">The shader model to compile against.</span></span> <span data-ttu-id="47088-118">Любой допустимый профиль шейдера вершин (см. [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) или профиль шейдера пикселей (см. [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="47088-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="47088-119">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="47088-119">FunctionName()</span></span>    | <span data-ttu-id="47088-120">Имя функции шейдера, а затем круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="47088-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="47088-121">Параметры общего фрагмента помечаются путем добавления \_ префикса "r" к их семантике.</span><span class="sxs-lookup"><span data-stu-id="47088-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="47088-122">В этом примере \_ семантика r посворлд и r \_ нормалворлд определяют, что эти два параметра являются общими параметрами между другими фрагментами.</span><span class="sxs-lookup"><span data-stu-id="47088-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="47088-123">Компоновщик фрагментов был технологией Microsoft Direct3D 9 в D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="47088-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="47088-124">Компоновщик фрагментов был средством (Flink.exe), API D3DX 9 и усовершенствованием HLSL.</span><span class="sxs-lookup"><span data-stu-id="47088-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="47088-125">Компоновщик фрагментов был удален в выпуске пакета SDK DirectX за Август 2009.</span><span class="sxs-lookup"><span data-stu-id="47088-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="47088-126">Компоновщик фрагментов никогда не применяется к Microsoft Direct3D 10, Microsoft Direct3D 10,1 или Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="47088-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="47088-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="47088-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47088-128">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47088-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
