---
title: Хелпбуттон, элемент
description: Представляет элемент управления кнопки справки.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Лента Windows для элемента Хелпбуттон
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442845"
---
# <a name="helpbutton-element"></a>Хелпбуттон, элемент

Представляет элемент управления [кнопки справки](windowsribbon-controls-helpbutton.md) .

## <a name="usage"></a>Использование

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                         |
|---------------------------------------------------------------------------------|
| [**Лента. Хелпбуттон**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждой [**ленты. хелпбуттон**](windowsribbon-element-ribbon-helpbutton.md).

Открывает диалоговое окно Справка по приложению при щелчке.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка, необходимая для реализации элемента управления [кнопки справки](windowsribbon-controls-helpbutton.md) на ленте.

В этом разделе кода показано объявление команды **хелпбуттон** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



В этом разделе кода показано объявление элемента управления **хелпбуттон** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Сведения об элементе

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления кнопки "Справка"](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





