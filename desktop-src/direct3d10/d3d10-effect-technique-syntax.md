---
description: Метод влияния объявляется с помощью следующего синтаксиса.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Синтаксис методики влияния (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141359"
---
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="15981-103">Синтаксис методики влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="15981-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="15981-104">Метод влияния объявляется с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="15981-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="15981-105">заметки technique10 *течникуенаме* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="15981-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="15981-106">{</span><span class="sxs-lookup"><span data-stu-id="15981-106">{</span></span>

<dl> <span data-ttu-id="15981-107">Передача  \[  < *заметок* пасснаме > \]</span><span class="sxs-lookup"><span data-stu-id="15981-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="15981-108">{</span><span class="sxs-lookup"><span data-stu-id="15981-108">{</span></span>
<dl> <span data-ttu-id="15981-109">\[*Сетстатеграуп*; \] \[ *Сетстатеграуп*;\]</span><span class="sxs-lookup"><span data-stu-id="15981-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="15981-110">...</span><span class="sxs-lookup"><span data-stu-id="15981-110">...</span></span>  
<span data-ttu-id="15981-111">\[*Сетстатеграуп*;\]</span><span class="sxs-lookup"><span data-stu-id="15981-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="15981-112">}</span><span class="sxs-lookup"><span data-stu-id="15981-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="15981-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="15981-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15981-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="15981-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="15981-115">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="15981-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="15981-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*течникуенаме*</span><span class="sxs-lookup"><span data-stu-id="15981-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="15981-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="15981-117">Optional.</span></span> <span data-ttu-id="15981-118">Строка ASCII, однозначно определяющая имя метода воздействия.</span><span class="sxs-lookup"><span data-stu-id="15981-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="15981-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Примечания*</span><span class="sxs-lookup"><span data-stu-id="15981-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="15981-120">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="15981-120">\[in\] Optional.</span></span> <span data-ttu-id="15981-121">Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="15981-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="15981-122">Синтаксис см. в разделе [синтаксис аннотации (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="15981-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="15981-123"><span id="pass"></span><span id="PASS"></span>проходит</span><span class="sxs-lookup"><span data-stu-id="15981-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="15981-124">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="15981-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="15981-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*пасснаме*</span><span class="sxs-lookup"><span data-stu-id="15981-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="15981-126">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="15981-126">\[in\] Optional.</span></span> <span data-ttu-id="15981-127">Строка ASCII, однозначно определяющая имя прохода.</span><span class="sxs-lookup"><span data-stu-id="15981-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="15981-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*сетстатеграуп*</span><span class="sxs-lookup"><span data-stu-id="15981-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="15981-129">\[в \] установите одну или несколько групп состояний, например:</span><span class="sxs-lookup"><span data-stu-id="15981-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15981-130">StateGroup</span><span class="sxs-lookup"><span data-stu-id="15981-130">StateGroup</span></span></th>
<th><span data-ttu-id="15981-131">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15981-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15981-132">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="15981-132">Blend State</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="15981-133">Список аргументов см. в разделе [<strong>омсетблендстате</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="15981-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15981-134">Состояние шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="15981-134">Depth-stencil State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="15981-135">См. раздел <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>омсетдепсстенЦилстате</strong></a> для списка аргументов.</span><span class="sxs-lookup"><span data-stu-id="15981-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15981-136">Состояние средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="15981-136">Rasterizer State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="15981-137">Список аргументов см. в разделе [<strong>рссетстате</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate).</span><span class="sxs-lookup"><span data-stu-id="15981-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15981-138">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="15981-138">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="15981-139">или</span><span class="sxs-lookup"><span data-stu-id="15981-139">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="15981-140">или</span><span class="sxs-lookup"><span data-stu-id="15981-140">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="15981-141">Сетксксксшадер — это один из <strong>сетвертексшадер</strong>, <strong>сетжеометришадер</strong>или <strong>сетпикселшадер</strong> (аналогично методам API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>вссетшадер</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>гссетшадер</strong></a>и <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="15981-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="15981-142">Группы состояний эффектов отображаются в [состоянии влияния](d3d10-effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="15981-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="15981-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="15981-143">Examples</span></span>

<span data-ttu-id="15981-144">В этом примере (из [образца CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) задается состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="15981-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



<span data-ttu-id="15981-145">В этом примере выполняется настройка состояния средства прорисовки для отображения объекта в каркасе.</span><span class="sxs-lookup"><span data-stu-id="15981-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



<span data-ttu-id="15981-146">В этом примере задается состояние шейдера (из [образца BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)). который использует вершину и шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="15981-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="15981-147">См. также</span><span class="sxs-lookup"><span data-stu-id="15981-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15981-148">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="15981-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 



