---
title: Аргументы функции
description: Функция принимает один или несколько входных аргументов. для объявления каждого аргумента используйте следующий синтаксис.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a2f2fdb656917ccf9dc57f06713fe01d77398d35776ac0c479b7d088281bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514767"
---
# <a name="function-arguments"></a>Аргументы функции

Функция принимает один или несколько входных аргументов. для объявления каждого аргумента используйте следующий синтаксис.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[\]Имя типа инпутмодифиер \[ : семантика \] \[ интерполатионмодифиер \] \[ = инициализаторы\]** |



 

\[\]Имя типа модификатора \[ : семантика \] \[ : модификатор интерполяции \] \[ = инициализаторы\]

Если имеется несколько аргументов функции, они разделяются запятыми.

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
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>инпутмодифиер</strong><br/></td>
<td>Необязательный термин, который определяет аргумент как вход, выход или и то, и другое.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Значение</td>
<td>Описание</td>
</tr>
<tr class="even">
<td><strong>В поле</strong></td>
<td>Только входные данные</td>
</tr>
<tr class="odd">
<td><strong>Inout</strong></td>
<td>Входные и выходные данные</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Только вывод</td>
</tr>
<tr class="odd">
<td><strong>Однородный элемент</strong></td>
<td>Входные только постоянные данные</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Параметры всегда передаются по значению. в указывает, что значение параметра должно быть скопировано из вызывающего приложения перед началом функции. out указывает, что последнее значение параметра должно быть скопировано и возвращено вызывающему приложению при возврате функции. параметр InOut является сокращением для указания обоих типов.</p>
<p>Универсальное значение берется из регистра констант; Каждый вызов шейдера вершин или шейдер пикселей имеет одинаковое начальное значение для универсальной переменной. Глобальные переменные обрабатываются так, как если бы они были объявлены единообразно. Для функций, не относящихся к верхнему уровню, универсальный код является синонимом <strong>в</strong>. Если использование параметра не указано, предполагается, что используется <strong>параметр.</strong></p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Тип</strong></p></td>
<td><p>Тип аргумента; может быть любым допустимым <a href="dx-graphics-hlsl-data-types.md">типом</a>HLSL.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Безымян</strong></p></td>
<td><p>Строка ASCII, однозначно определяющая имя функции шейдера.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Семантическ</strong></p></td>
<td><p>Необязательная строка, определяющая предполагаемое использование данных (см. раздел <a href="dx-graphics-hlsl-semantics.md">семантика (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>интерполатионмодифиер</strong></p></td>
<td><p>Необязательный <a href="dx-graphics-hlsl-struct.md">Модификатор интерполяции</a> , позволяющий шейдеру определить метод интерполяции. Модификатор интерполяции для аргумента функции применяется только к аргументу, используемому в качестве входных данных для функции шейдера пикселей.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Инициализаторы</strong></p></td>
<td><p>Необязательные значения для инициализации; для инициализации типов данных с несколькими компонентами требуется несколько значений.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

Аргументы функции перечислены в объявлении функции в списке аргументов с разделителями-запятыми. Как и в функциях C, у каждого аргумента должно быть объявлено имя параметра и тип. аргумент функции HLSL может включать семантическое, начальное значение, а входные шейдеры пикселей могут включать тип интерполяции.

*Типом* аргумента функции может быть структура, которая может включать модификатор интерполяции для каждого члена. Если аргумент функции также имеет модификатор интерполяции, модификатор аргумента функции переопределяет модификаторы интерполяции, объявленные в типе.

## <a name="examples"></a>Примеры

В этом примере (из [образца BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) показаны однородные и неоднородные входные данные функции шейдера вершин.


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



В этом примере (из [примера контентстреаминг](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) используется входная структура для передачи аргументов в функцию шейдера пикселей.


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





