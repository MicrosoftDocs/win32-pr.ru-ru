---
title: Установка состояния действия (Direct3D 11)
description: Некоторые константы эффектов необходимо инициализировать. См. базовый код для установки переменных эффектов в Direct3D 12.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c64f9e642e867e9398722d4590a4c2ce9193b4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407667"
---
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="ba3b6-104">Установка состояния действия (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ba3b6-104">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="ba3b6-105">Некоторые константы эффектов необходимо инициализировать.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="ba3b6-106">После инициализации состояние воздействия устанавливается на устройство для всего цикла подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="ba3b6-107">Другие переменные необходимо обновлять каждый раз при вызове цикла визуализации.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="ba3b6-108">Базовый код для установки переменных эффектов показан ниже для каждого типа переменных.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="ba3b6-109">Действие инкапсулирует все состояние отрисовки, необходимое для выполнения этапа отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="ba3b6-110">В терминах API существует три типа состояния, инкапсулированные в результате.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="ba3b6-111">Состояние константы</span><span class="sxs-lookup"><span data-stu-id="ba3b6-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="ba3b6-112">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="ba3b6-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="ba3b6-113">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="ba3b6-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="ba3b6-114">Состояние константы</span><span class="sxs-lookup"><span data-stu-id="ba3b6-114">Constant State</span></span>

<span data-ttu-id="ba3b6-115">Сначала объявите переменные в силе с помощью типов данных HLSL.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-115">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="ba3b6-116">Во вторых, объявите в приложении переменные, которые могут быть заданы приложением, а затем обновите переменные эффектов.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="ba3b6-117">В третьих, используйте методы Update, чтобы задать значения переменных в приложении в переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D11FrameRender()
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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="ba3b6-118">Два способа получения состояния в переменной Effect</span><span class="sxs-lookup"><span data-stu-id="ba3b6-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="ba3b6-119">Существует два способа получить состояние, содержащееся в переменной Effect.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="ba3b6-120">С учетом влияния, которое было загружено в память.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="ba3b6-121">Один из способов — получить состояние образца из [**ID3DX11EffectVariable**](id3dx11effectvariable.md) , которое было приведено в качестве интерфейса выборки.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-121">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="ba3b6-122">Другой способ — получить состояние образца из [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-122">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="ba3b6-123">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="ba3b6-123">Shader State</span></span>

<span data-ttu-id="ba3b6-124">Состояние шейдера объявляется и назначается в методике действия в рамках прохода.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="ba3b6-125">Это работает так же, как если бы вы не использовали никаких эффектов.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="ba3b6-126">Существует три вызова, по одному для каждого типа шейдера (вершина, геометрия и пиксель).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="ba3b6-127">Первый из них, Сетвертексшадер, вызывает [**ссылку ID3D11DeviceContext:: вссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-127">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="ba3b6-128">Компилешадер — это специальная функция, которая принимает профиль шейдера (VS \_ 4 \_ 0) и имя функции шейдера вершин (рендервс).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="ba3b6-129">Иными словами, каждый из этих вызовов Компилешадер компилирует свою связанную функцию шейдера и возвращает указатель на скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-129">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="ba3b6-130">Обратите внимание, что должно быть задано не все состояние шейдера.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-130">Note that not all shader state must be set.</span></span> <span data-ttu-id="ba3b6-131">Этот проход не включает вызовы Сесуллшадер или Сетдомаиншадер, что означает, что привязанные в данный момент поверхности и шейдеры доменов будут неизменными.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-131">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="ba3b6-132">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="ba3b6-132">Texture State</span></span>

<span data-ttu-id="ba3b6-133">Состояние текстуры немного сложнее, чем задание переменной, поскольку данные текстуры не просто считываются как переменная, она выдается из текстуры.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-133">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="ba3b6-134">Поэтому необходимо определить переменную текстуры (как и обычную переменную, за исключением того, что она использует тип текстуры), и необходимо определить условия выборки.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-134">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="ba3b6-135">Ниже приведен пример объявления переменной текстуры и соответствующего объявления состояния выборки.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-135">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="ba3b6-136">Ниже приведен пример настройки текстуры из приложения.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-136">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="ba3b6-137">В этом примере текстура хранится в данных сетки, которая была загружена при создании результата.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-137">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="ba3b6-138">Первый шаг — получение указателя на текстуру из результата (из сетки).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-138">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="ba3b6-139">На втором шаге указывается представление для доступа к текстуре.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-139">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="ba3b6-140">Представление определяет общий способ доступа к данным из ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-140">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



<span data-ttu-id="ba3b6-141">С точки зрения приложения неупорядоченные представления доступа обрабатываются аналогично представлениям ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-141">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="ba3b6-142">Однако в построителейх шейдеров и функций шейдера неупорядоченные данные представления доступа считываются и записываются напрямую.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-142">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="ba3b6-143">Невозможно выполнить выборку из представления неупорядоченного доступа.</span><span class="sxs-lookup"><span data-stu-id="ba3b6-143">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="ba3b6-144">Дополнительные сведения о просмотре ресурсов см. в разделе [ресурсы](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ba3b6-144">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba3b6-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ba3b6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba3b6-146">Отрисовка результата (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ba3b6-146">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




