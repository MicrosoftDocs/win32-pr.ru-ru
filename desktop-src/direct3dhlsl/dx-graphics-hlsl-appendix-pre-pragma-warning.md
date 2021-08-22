---
title: Warning pragma, директива
description: Директива pragma, которая изменяет поведение предупреждающих сообщений компилятора.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- предупреждение директивы pragma HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56d741f0d91784f578377e5ee117cf0c3b4aabe5cb1177c7942fc6e8ab8f81d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120358"
---
# <a name="warning-pragma-directive"></a>Warning pragma, директива

Директива pragma, которая изменяет поведение предупреждающих сообщений компилятора.



| \#pragma warning ( *warning-спецификатор* : *warning-number-list* \[ ; *warning — описатель* : *warning-number-list*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

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
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>описатель "предупреждение"</em><br/></td>
<td>Поведение, заданное для указанных предупреждений. Этот параметр может принимать одно из значений, перечисленных в следующей таблице. <br/> 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>Отображение сообщения предупреждений с указанными числами только один раз.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Сброс поведения предупреждений с указанными значениями по умолчанию. Это также влияет на отключение предупреждения по умолчанию. Предупреждение будет создано на уровне по умолчанию.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Применить указанный уровень к предупреждениям с указанными числами. Это также влияет на отключение предупреждения по умолчанию.</td>
</tr>
<tr class="even">
<td>disable</td>
<td>Не выдавать предупреждения с указанными числами.</td>
</tr>
<tr class="odd">
<td>error</td>
<td>Сообщать о предупреждениях с указанными числами как об ошибках.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>Список "warning-number-list"</em></p></td>
<td><p>Разделенный пробелами список номеров предупреждений для изменения поведения.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

Можно указать любое количество уникальных изменений поведения предупреждений в пределах одной и той же директивы pragma warning, разделяя изменения точкой с запятой.

Компилятор добавит 4000 к любому номеру предупреждения, который находится в диапазоне от 0 до 999. Для номеров предупреждений больше 4699 (связанных с созданием кода) прагма-директива warning действует только при размещении внешних определений функций. Директива pragma пропускается, если она указывает число больше 4699 и используется внутри функции.

Прагма-директива HLSL warning не поддерживает функцию **Push** и **POP** предупреждения pragma, входящей в компилятор C++.

## <a name="examples"></a>Примеры

В следующем примере отключаются предупреждения 4507 и 4034, отображается предупреждение 4385 и выводится предупреждение 4164 в качестве ошибки.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



Предыдущий пример функционально эквивалентен следующему:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Директивы препроцессора (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Директива pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





