---
title: Синтаксис методики влияния (Direct3D 11)
description: Метод влияния объявляется с помощью синтаксиса, описанного в этом разделе.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, Direct3D 11, результат
- успех, Direct3D 11
- Компилешадер, Direct3D 11, результат
- Сетстатеграуп, Direct3D 11, результат
- Сетблендстате, Direct3D 11, результат
- СетдепсстенЦилстате, Direct3D 11, результат
- Сетрастеризерстате, Direct3D 11, результат
- Сетвертексшадер, Direct3D 11, результат
- Сетжеометришадер, Direct3D 11, результат
- Сетпикселшадер, Direct3D 11, результат
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133342"
---
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="36428-113">Синтаксис методики влияния (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="36428-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="36428-114">Метод влияния объявляется с помощью синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="36428-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="36428-115">Заметки течникуеверсион *течникуенаме* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="36428-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="36428-116">{</span><span class="sxs-lookup"><span data-stu-id="36428-116">{</span></span>

<dl> <span data-ttu-id="36428-117">Передача  \[  < *заметок* пасснаме > \]</span><span class="sxs-lookup"><span data-stu-id="36428-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="36428-118">{</span><span class="sxs-lookup"><span data-stu-id="36428-118">{</span></span>
<dl> <span data-ttu-id="36428-119">\[*Сетстатеграуп*; \] \[ *Сетстатеграуп*;\]</span><span class="sxs-lookup"><span data-stu-id="36428-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="36428-120">...</span><span class="sxs-lookup"><span data-stu-id="36428-120">...</span></span>  
<span data-ttu-id="36428-121">\[*Сетстатеграуп*;\]</span><span class="sxs-lookup"><span data-stu-id="36428-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="36428-122">}</span><span class="sxs-lookup"><span data-stu-id="36428-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="36428-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="36428-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36428-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="36428-124">Item</span></span></th>
<th><span data-ttu-id="36428-125">Описание</span><span class="sxs-lookup"><span data-stu-id="36428-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36428-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>течникуеверсион</span><span class="sxs-lookup"><span data-stu-id="36428-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="36428-127">Либо technique10, либо technique11.</span><span class="sxs-lookup"><span data-stu-id="36428-127">Either technique10 or technique11.</span></span> <span data-ttu-id="36428-128">Методы, использующие новые функции Direct3D 11 (шейдеры 5_0, Биндинтерфацес и т. д.), должны использовать technique11.</span><span class="sxs-lookup"><span data-stu-id="36428-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36428-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>течникуенаме</em></span><span class="sxs-lookup"><span data-stu-id="36428-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="36428-130">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="36428-130">Optional.</span></span> <span data-ttu-id="36428-131">Строка ASCII, однозначно определяющая имя метода воздействия.</span><span class="sxs-lookup"><span data-stu-id="36428-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36428-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Примечания</em> ></span><span class="sxs-lookup"><span data-stu-id="36428-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="36428-133">[в] Необязательно.</span><span class="sxs-lookup"><span data-stu-id="36428-133">[in] Optional.</span></span> <span data-ttu-id="36428-134">Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="36428-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="36428-135">Синтаксис см. в разделе <a href="d3d11-effect-annotation-syntax.md">синтаксис аннотации (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="36428-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36428-136"><span id="pass"></span><span id="PASS"></span>проходит</span><span class="sxs-lookup"><span data-stu-id="36428-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="36428-137">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="36428-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36428-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>пасснаме</em></span><span class="sxs-lookup"><span data-stu-id="36428-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="36428-139">[в] Необязательно.</span><span class="sxs-lookup"><span data-stu-id="36428-139">[in] Optional.</span></span> <span data-ttu-id="36428-140">Строка ASCII, однозначно определяющая имя прохода.</span><span class="sxs-lookup"><span data-stu-id="36428-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36428-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>сетстатеграуп</em></span><span class="sxs-lookup"><span data-stu-id="36428-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="36428-142">окне Задайте одну или несколько групп состояний, например:</span><span class="sxs-lookup"><span data-stu-id="36428-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36428-143">StateGroup</span><span class="sxs-lookup"><span data-stu-id="36428-143">StateGroup</span></span></th>
<th><span data-ttu-id="36428-144">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36428-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36428-145">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="36428-145">Blend State</span></span></td>
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

<p><span data-ttu-id="36428-146">Список аргументов см. в разделе [<strong>ссылку ID3D11DeviceContext:: омсетблендстате</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-ID3D11DeviceContext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="36428-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36428-147">Состояние шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="36428-147">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="36428-148">Список аргументов см. в разделе <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ссылку ID3D11DeviceContext:: омсетдепсстенЦилстате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="36428-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36428-149">Состояние средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="36428-149">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="36428-150">Список аргументов см. в разделе [<strong>ссылку ID3D11DeviceContext:: рссетстате</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-ID3D11DeviceContext-rssetstate).</span><span class="sxs-lookup"><span data-stu-id="36428-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36428-151">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="36428-151">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="36428-152">Сетксксксшадер — это один из Сетвертексшадер, Сетдомаиншадер, Сесуллшадер, Сетжеометришадер, Сетпикселшадер или SetComputeShader (аналогично методам API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ссылку ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ссылку ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ссылку ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ссылку id3d11devicecontext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ссылку ID3D11DeviceContext::P ssetshader</strong></a> и <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ссылку ID3D11DeviceContext:: CSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="36428-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="36428-153">Шейдер — это переменная шейдера, которую можно получить множеством способов.</span><span class="sxs-lookup"><span data-stu-id="36428-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36428-154">Состояние целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="36428-154">Render Target State</span></span></td>
<td><span data-ttu-id="36428-155">Одно из двух значений:</span><span class="sxs-lookup"><span data-stu-id="36428-155">One of:</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="36428-156">Аналогично <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ссылку ID3D11DeviceContext:: омсетрендертаржетс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="36428-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="36428-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="36428-157">Examples</span></span>

<span data-ttu-id="36428-158">В этом примере задается состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="36428-158">This example sets blending state.</span></span>


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



<span data-ttu-id="36428-159">В этом примере выполняется настройка состояния средства прорисовки для отображения объекта в каркасе.</span><span class="sxs-lookup"><span data-stu-id="36428-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="36428-160">В этом примере задается состояние шейдера.</span><span class="sxs-lookup"><span data-stu-id="36428-160">This example sets shader state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="36428-161">См. также</span><span class="sxs-lookup"><span data-stu-id="36428-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36428-162">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="36428-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="36428-163">Синтаксис группы эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="36428-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="36428-164">Группы состояний эффектов</span><span class="sxs-lookup"><span data-stu-id="36428-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 





