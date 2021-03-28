---
title: Тип образца
description: Используйте следующий синтаксис, чтобы объявить состояние образца, а также состояние сравнения образцов.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Тип образца HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070030"
---
# <a name="sampler-type"></a>Тип образца

Используйте следующий синтаксис, чтобы объявить состояние образца, а также состояние сравнения образцов.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 10 и более поздними версиями:<br/> Ниже приведен синтаксис для образца в Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em>имя</em>образца  =  <em>самплертипе</em>{текстура = <<em>texture_variable</em> > ;   [<em>STATE_NAME = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Синтаксис образца для выборки в Direct3D 10 и более поздних версиях немного изменился для поддержки объектов текстуры и массивов выборки.</p>

<table>
<tbody>
<tr class="odd">
<td><em>Самплертипе имя [Индекс]</em>{[<em>STATE_NAME = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>образец
</dt> <dd>

Только Direct3D 9. Обязательное ключевое слово.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*
</dt> <dd>

Строка ASCII, однозначно определяющая имя переменной образца.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Номер\]*
</dt> <dd>

Только Direct3D 10 и более поздние версии. Необязательный размер массива; положительное целое число, которое больше или равно 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*самплертипе*
</dt> <dd>

\[в \] поле Тип образца выберите одно из следующих: выборка,  *sampler1D*, *sampler2D*, *sampler3D*, *самплеркубе*, *\_ состояние образца*, *самплерстате*.



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Различия между Direct3D 9 и Direct3D 10 и более поздними версиями:<br/> Direct3D 10 и более поздних версий поддерживает один дополнительный тип образца: *самплеркомпарисонстате*.<br/> |



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Текстура* = <ая *\_ переменная текстуры*>;
</dt> <dd>

Только Direct3D 9. Переменная текстуры. Ключевое слово *текстуры* является обязательным в левой части; имя переменной принадлежит правой части выражения в угловых скобках.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ Name = \_ значение State*
</dt> <dd>

\[При \] необязательном назначении состояний. Левая часть назначения — это имя состояния, правая часть — это значение состояния. Все назначения состояний должны находиться в блоке операторов (в фигурных скобках). Каждая инструкция отделяется точкой с запятой. В следующей таблице перечислены возможные имена состояний.


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



Правая часть каждого выражения — это значение, присваиваемое каждому состоянию. Возможные значения состояния для Direct3D 11 см. в разделе [**D3D11 \_ образец \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) в виде структуры. Между именами состояний и элементами структуры существует одна и одна связь. См. следующий пример.

</dd> </dl>

## <a name="remarks"></a>Примечания

При реализации воздействия состояние выборки — это один из нескольких типов состояний, которые может потребоваться настроить в конвейере для подготовки к просмотру. Список всех возможных состояний, которые можно установить в результате, см. в следующих статьях:

-   В Direct3D 10 используются [группы состояний](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 использует индивидуальные [состояния](/windows/desktop/direct3d9/effect-states).

## <a name="example"></a>Например, .



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 10:<br/> Ниже приведен частичный пример образца Direct3D 9 из <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">примера басичлсл</a>.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Ниже приведен частичный пример образца Direct3D 10 из <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">примера BasicHLSL10</a>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

Ниже приведен частичный пример объявления состояния сравнения образцов и вызова образца сравнения в Direct3D 10.


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Типы данных (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

