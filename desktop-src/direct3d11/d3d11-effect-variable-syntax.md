---
title: Синтаксис переменной Effect (Direct3D 11)
description: Переменная Effect объявляется с помощью синтаксиса, описанного в этом разделе.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487753"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="c8201-103">Синтаксис переменной Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c8201-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="c8201-104">Переменная Effect объявляется с помощью синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c8201-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8201-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8201-105">Syntax</span></span>

<span data-ttu-id="c8201-106">Базовый синтаксис:</span><span class="sxs-lookup"><span data-stu-id="c8201-106">Basic syntax:</span></span>

<span data-ttu-id="c8201-107">*DataType* *variablename* \[ *: семантикнаме* \]  <  *Annotations*  >  \[ = инитиалвалуе \] ;</span><span class="sxs-lookup"><span data-stu-id="c8201-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="c8201-108">Полный синтаксис см. в разделе [синтаксис переменных (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .</span><span class="sxs-lookup"><span data-stu-id="c8201-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="c8201-109">Имя</span><span class="sxs-lookup"><span data-stu-id="c8201-109">Name</span></span>         | <span data-ttu-id="c8201-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c8201-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8201-111">DataType</span><span class="sxs-lookup"><span data-stu-id="c8201-111">DataType</span></span>     | <span data-ttu-id="c8201-112">Любое [базовое](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [текстурное](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), неупорядоченное представление доступа, шейдер или тип блока состояния.</span><span class="sxs-lookup"><span data-stu-id="c8201-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="c8201-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="c8201-113">VariableName</span></span> | <span data-ttu-id="c8201-114">Строка ASCII, однозначно определяющая имя переменной Effect.</span><span class="sxs-lookup"><span data-stu-id="c8201-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="c8201-115">семантикнаме</span><span class="sxs-lookup"><span data-stu-id="c8201-115">SemanticName</span></span> | <span data-ttu-id="c8201-116">Строка ASCII, указывающая дополнительные сведения о том, как должна использоваться переменная.</span><span class="sxs-lookup"><span data-stu-id="c8201-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="c8201-117">Семантика — это строка ASCII, которая может быть стандартной системой или пользовательской строкой.</span><span class="sxs-lookup"><span data-stu-id="c8201-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="c8201-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="c8201-118">Annotations</span></span>  | <span data-ttu-id="c8201-119">Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="c8201-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="c8201-120">Синтаксис см. в разделе [синтаксис аннотации (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c8201-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="c8201-121">инитиалвалуе</span><span class="sxs-lookup"><span data-stu-id="c8201-121">InitialValue</span></span> | <span data-ttu-id="c8201-122">Значение переменной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8201-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="c8201-123">Переменная Effect, объявленная вне всех функций, считается глобальной в области видимости. переменные, объявленные внутри функции, являются локальными для этой функции.</span><span class="sxs-lookup"><span data-stu-id="c8201-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="c8201-124">Например, .</span><span class="sxs-lookup"><span data-stu-id="c8201-124">Example</span></span>

<span data-ttu-id="c8201-125">В этом примере показаны числовые переменные глобальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="c8201-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="c8201-126">В этом примере показаны переменные, являющиеся локальными для функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="c8201-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="c8201-127">В этом примере показаны параметры функции, имеющие семантику.</span><span class="sxs-lookup"><span data-stu-id="c8201-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="c8201-128">В этом примере показано объявление глобальной переменной текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8201-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="c8201-129">Выборка текстуры осуществляется с помощью образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8201-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="c8201-130">Чтобы настроить образец в результате, см. [тип образца](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="c8201-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="c8201-131">В этом примере показано объявление глобальных переменных представления неупорядоченного доступа.</span><span class="sxs-lookup"><span data-stu-id="c8201-131">This example illustrates declaring global unordered access view variables.</span></span>


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a><span data-ttu-id="c8201-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c8201-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8201-133">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="c8201-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 