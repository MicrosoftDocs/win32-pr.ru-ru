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
# <a name="effect-technique-syntax-direct3d-11"></a>Синтаксис методики влияния (Direct3D 11)

Метод влияния объявляется с помощью синтаксиса, описанного в этом разделе.

Заметки течникуеверсион *течникуенаме* \[  <  > \]

{

<dl> Передача  \[  < *заметок* пасснаме > \]  
{
<dl> \[*Сетстатеграуп*; \] \[ *Сетстатеграуп*;\]  
...  
\[*Сетстатеграуп*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Параметры



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>течникуеверсион<br/></td>
<td>Либо technique10, либо technique11. Методы, использующие новые функции Direct3D 11 (шейдеры 5_0, Биндинтерфацес и т. д.), должны использовать technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>течникуенаме</em><br/></td>
<td>Необязательный параметр. Строка ASCII, однозначно определяющая имя метода воздействия.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Примечания</em> ><br/></td>
<td>[в] Необязательно. Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов. Синтаксис см. в разделе <a href="d3d11-effect-annotation-syntax.md">синтаксис аннотации (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>проходит<br/></td>
<td>Обязательное ключевое слово.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>пасснаме</em><br/></td>
<td>[в] Необязательно. Строка ASCII, однозначно определяющая имя прохода.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>сетстатеграуп</em><br/></td>
<td>окне Задайте одну или несколько групп состояний, например: <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Синтаксис</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Состояние смешения</td>
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

<p>Список аргументов см. в разделе [<strong>ссылку ID3D11DeviceContext:: омсетблендстате</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-ID3D11DeviceContext-omsetblendstate).</p></td>
</tr>
<tr class="even">
<td>Состояние шаблона глубины</td>
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
<p>Список аргументов см. в разделе <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ссылку ID3D11DeviceContext:: омсетдепсстенЦилстате</strong></a> .</p></td>
</tr>
<tr class="odd">
<td>Состояние средства прорисовки</td>
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
<p>Список аргументов см. в разделе [<strong>ссылку ID3D11DeviceContext:: рссетстате</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-ID3D11DeviceContext-rssetstate).</p></td>
</tr>
<tr class="even">
<td>Состояние шейдера</td>
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
<p>Сетксксксшадер — это один из Сетвертексшадер, Сетдомаиншадер, Сесуллшадер, Сетжеометришадер, Сетпикселшадер или SetComputeShader (аналогично методам API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ссылку ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ссылку ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ссылку ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ссылку id3d11devicecontext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ссылку ID3D11DeviceContext::P ssetshader</strong></a> и <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ссылку ID3D11DeviceContext:: CSSetShader</strong></a>).</p>
<p>Шейдер — это переменная шейдера, которую можно получить множеством способов.</p>
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
<td>Состояние целевого объекта прорисовки</td>
<td>Одно из двух значений:
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
<p>Аналогично <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ссылку ID3D11DeviceContext:: омсетрендертаржетс</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Примеры

В этом примере задается состояние смешения.


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



В этом примере выполняется настройка состояния средства прорисовки для отображения объекта в каркасе.


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



В этом примере задается состояние шейдера.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат эффектов](d3d11-effect-format.md)
</dt> <dt>

[Синтаксис группы эффектов (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Группы состояний эффектов](d3d11-effect-states.md)
</dt> </dl>

 

 





