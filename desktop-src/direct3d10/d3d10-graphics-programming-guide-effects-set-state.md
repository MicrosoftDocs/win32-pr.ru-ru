---
description: Некоторые константы эффектов необходимо инициализировать.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Установка состояния действия (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f14d4cdfb23c56f9534d1b4029482ce4e494b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990460"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="d6a73-103">Установка состояния действия (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d6a73-103">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="d6a73-104">Некоторые константы эффектов необходимо инициализировать.</span><span class="sxs-lookup"><span data-stu-id="d6a73-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="d6a73-105">После инициализации состояние воздействия устанавливается на устройство для всего цикла подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="d6a73-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="d6a73-106">Другие переменные необходимо обновлять каждый раз при вызове цикла визуализации.</span><span class="sxs-lookup"><span data-stu-id="d6a73-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="d6a73-107">Базовый код для установки переменных эффектов показан ниже для каждого типа переменных.</span><span class="sxs-lookup"><span data-stu-id="d6a73-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="d6a73-108">Действие инкапсулирует все состояние отрисовки, необходимое для выполнения этапа отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d6a73-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="d6a73-109">В терминах API существует три типа состояния, инкапсулированные в результате.</span><span class="sxs-lookup"><span data-stu-id="d6a73-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="d6a73-110">Состояние константы</span><span class="sxs-lookup"><span data-stu-id="d6a73-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="d6a73-111">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="d6a73-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="d6a73-112">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="d6a73-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="d6a73-113">Состояние константы</span><span class="sxs-lookup"><span data-stu-id="d6a73-113">Constant State</span></span>

<span data-ttu-id="d6a73-114">Сначала объявите переменные в силе с помощью типов данных HLSL.</span><span class="sxs-lookup"><span data-stu-id="d6a73-114">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="d6a73-115">Во вторых, объявите в приложении переменные, которые могут быть заданы приложением, а затем обновите переменные эффектов.</span><span class="sxs-lookup"><span data-stu-id="d6a73-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="d6a73-116">В третьих, используйте методы Update, чтобы задать значения переменных в приложении в переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="d6a73-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D10FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="d6a73-117">Два способа получения состояния в переменной Effect</span><span class="sxs-lookup"><span data-stu-id="d6a73-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="d6a73-118">Существует два способа получить состояние, содержащееся в переменной Effect.</span><span class="sxs-lookup"><span data-stu-id="d6a73-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="d6a73-119">С учетом влияния, которое было загружено в память.</span><span class="sxs-lookup"><span data-stu-id="d6a73-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="d6a73-120">Один из способов — получить состояние образца из [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) , который был приведен как интерфейс образца.</span><span class="sxs-lookup"><span data-stu-id="d6a73-120">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="d6a73-121">Другой способ — получить состояние образца из [**интерфейса ID3D10SamplerState**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span><span class="sxs-lookup"><span data-stu-id="d6a73-121">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="d6a73-122">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="d6a73-122">Shader State</span></span>

<span data-ttu-id="d6a73-123">Состояние шейдера объявляется и назначается в методике действия в рамках прохода.</span><span class="sxs-lookup"><span data-stu-id="d6a73-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="d6a73-124">Это работает так же, как если бы вы не использовали никаких эффектов.</span><span class="sxs-lookup"><span data-stu-id="d6a73-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="d6a73-125">Существует три вызова, по одному для каждого типа шейдера (вершина, геометрия и пиксель).</span><span class="sxs-lookup"><span data-stu-id="d6a73-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="d6a73-126">Первый из них, Сетвертексшадер, вызывает [**ID3D10Device:: вссетшадер**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="d6a73-126">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="d6a73-127">Компилешадер — это специальная функция, которая принимает профиль шейдера (VS \_ 4 \_ 0) и имя функции шейдера вершин (рендервс).</span><span class="sxs-lookup"><span data-stu-id="d6a73-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="d6a73-128">Иными словами, каждый из этих вызовов Сетксксксшадер компилирует свою связанную функцию шейдера и возвращает указатель на скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="d6a73-128">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="d6a73-129">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="d6a73-129">Texture State</span></span>

<span data-ttu-id="d6a73-130">Состояние текстуры немного сложнее, чем задание переменной, поскольку данные текстуры не просто считываются как переменная, она выдается из текстуры.</span><span class="sxs-lookup"><span data-stu-id="d6a73-130">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="d6a73-131">Поэтому необходимо определить переменную текстуры (как и обычную переменную, за исключением того, что она использует тип текстуры), и необходимо определить условия выборки.</span><span class="sxs-lookup"><span data-stu-id="d6a73-131">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="d6a73-132">Ниже приведен пример объявления переменной текстуры и соответствующего объявления состояния выборки.</span><span class="sxs-lookup"><span data-stu-id="d6a73-132">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="d6a73-133">Ниже приведен пример настройки текстуры из приложения.</span><span class="sxs-lookup"><span data-stu-id="d6a73-133">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="d6a73-134">В этом примере текстура хранится в данных сетки, которая была загружена при создании результата.</span><span class="sxs-lookup"><span data-stu-id="d6a73-134">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="d6a73-135">Первый шаг — получение указателя на текстуру из результата (из сетки).</span><span class="sxs-lookup"><span data-stu-id="d6a73-135">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="d6a73-136">На втором шаге указывается представление для доступа к текстуре.</span><span class="sxs-lookup"><span data-stu-id="d6a73-136">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="d6a73-137">Представление определяет общий способ доступа к данным из ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="d6a73-137">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



<span data-ttu-id="d6a73-138">Дополнительные сведения о просмотре ресурсов см. в разделе [представления текстуры (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="d6a73-138">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6a73-139">См. также</span><span class="sxs-lookup"><span data-stu-id="d6a73-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6a73-140">Отрисовка влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d6a73-140">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



