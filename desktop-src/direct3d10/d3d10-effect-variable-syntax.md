---
description: Переменная Effect объявляется с помощью следующего синтаксиса.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Синтаксис переменной Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423369"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="8675e-103">Синтаксис переменной Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8675e-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="8675e-104">Переменная Effect объявляется с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="8675e-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="8675e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8675e-105">Syntax</span></span>

<span data-ttu-id="8675e-106">*DataType* *variablename* \[ : *семантикнаме* \]  <  *Annotations* >;</span><span class="sxs-lookup"><span data-stu-id="8675e-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="8675e-107">Имя</span><span class="sxs-lookup"><span data-stu-id="8675e-107">Name</span></span>         | <span data-ttu-id="8675e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8675e-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8675e-109">DataType</span><span class="sxs-lookup"><span data-stu-id="8675e-109">DataType</span></span>     | <span data-ttu-id="8675e-110">Любой тип [базовой](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) или [текстуры](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8675e-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="8675e-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="8675e-111">VariableName</span></span> | <span data-ttu-id="8675e-112">Строка ASCII, однозначно определяющая имя переменной Effect.</span><span class="sxs-lookup"><span data-stu-id="8675e-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="8675e-113">семантикнаме</span><span class="sxs-lookup"><span data-stu-id="8675e-113">SemanticName</span></span> | <span data-ttu-id="8675e-114">Строка ASCII, указывающая дополнительные сведения о том, как должна использоваться переменная.</span><span class="sxs-lookup"><span data-stu-id="8675e-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="8675e-115">Семантика — это строка ASCII, которая может быть стандартной системой или пользовательской строкой.</span><span class="sxs-lookup"><span data-stu-id="8675e-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="8675e-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="8675e-116">Annotations</span></span>  | <span data-ttu-id="8675e-117">Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="8675e-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="8675e-118">Синтаксис см. в разделе [синтаксис аннотации (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8675e-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="8675e-119">Переменная Effect, объявленная вне всех функций, считается глобальной в области видимости. переменные, объявленные внутри функции, являются локальными для этой функции.</span><span class="sxs-lookup"><span data-stu-id="8675e-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="8675e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="8675e-120">Example</span></span>

<span data-ttu-id="8675e-121">В [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) используются глобальные переменные без семантики для цветов материала, свойств освещения и матриц преобразования.</span><span class="sxs-lookup"><span data-stu-id="8675e-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="8675e-122">В этом примере показаны переменные глобальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="8675e-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="8675e-123">В этом примере показаны переменные, являющиеся локальными для функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="8675e-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="8675e-124">В этом примере показаны параметры функции, имеющие семантику.</span><span class="sxs-lookup"><span data-stu-id="8675e-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="8675e-125">В этом примере показано объявление переменной текстуры.</span><span class="sxs-lookup"><span data-stu-id="8675e-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="8675e-126">Выборка текстуры осуществляется с помощью образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="8675e-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="8675e-127">Чтобы настроить образец в результате, см. [тип образца](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="8675e-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8675e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8675e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8675e-129">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="8675e-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
