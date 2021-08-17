---
description: Метод влияния объявляется с помощью следующего синтаксиса.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Синтаксис методики влияния (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c0ff0c0f1b5e9c1fac4cdb12aac21e42d89771c0eae89d1cd9538d0281acee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914490"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Синтаксис методики влияния (Direct3D 10)

Метод влияния объявляется с помощью следующего синтаксиса.

заметки technique10 *течникуенаме* \[  <  > \]

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

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Обязательное ключевое слово.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*течникуенаме*
</dt> <dd>

Необязательный элемент. Строка ASCII, однозначно определяющая имя метода воздействия.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Примечания*
</dt> <dd>

\[\]необязательно. Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов. Синтаксис см. в разделе [синтаксис аннотации (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>проходит
</dt> <dd>

Обязательное ключевое слово.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*пасснаме*
</dt> <dd>

\[\]необязательно. Строка ASCII, однозначно определяющая имя прохода.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*сетстатеграуп*
</dt> <dd>

\[в \] установите одну или несколько групп состояний, например:



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

<p>Список аргументов см. в разделе [<strong>омсетблендстате</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate).</p></td>
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
<p>См. раздел <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>омсетдепсстенЦилстате</strong></a> для списка аргументов.</p></td>
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
<p>Список аргументов см. в разделе [<strong>рссетстате</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate).</p></td>
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
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>или</p>
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
<p>или</p>
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
<p>Сетксксксшадер — это один из <strong>сетвертексшадер</strong>, <strong>сетжеометришадер</strong>или <strong>сетпикселшадер</strong> (аналогично методам API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>вссетшадер</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>гссетшадер</strong></a>и <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Группы состояний эффектов отображаются в [состоянии влияния](d3d10-effect-states.md).

## <a name="examples"></a>Примеры

В этом примере (из [образца CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) задается состояние смешения.


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



В этом примере задается состояние шейдера (из [образца BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)). который использует вершину и шейдер пикселей.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Формат эффектов](d3d10-effect-format.md)
</dt> </dl>

 

 



