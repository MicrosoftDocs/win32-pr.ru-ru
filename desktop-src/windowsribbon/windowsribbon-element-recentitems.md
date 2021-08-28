---
title: Рецентитемс, элемент
description: Представляет элемент управления "Недавние элементы" в меню "приложение".
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- элемент рецентитемс Windows лента
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa1354caadc14cf15b34333c81bff1211e1fbc8c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631952"
---
# <a name="recentitems-element"></a>Рецентитемс, элемент

Представляет элемент управления " [недавние элементы](windowsribbon-controls-recentitems.md) " в [меню "приложение](windowsribbon-controls-applicationmenu.md)".

## <a name="usage"></a>Использование

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<tr class="even">
<td><strong>енаблепиннинг</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>Нет<br/></td>
<td>Число недавно отображаемых элементов.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: nonNegativeInteger)<br/> </dt> <dd> Целочисленное значение 0 или выше.<br/> Значение по умолчанию — <strong>10</strong>.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**Аппликатионмену. Рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен выполняться ровно один раз для каждого элемента [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) .

Элемент управления [недавние элементы](windowsribbon-controls-recentitems.md) отображает список недавно использовавшихся элементов приложения ленты.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента управления [недавние элементы](windowsribbon-controls-recentitems.md) .

В следующем примере показано объявление команды **рецентитемс** .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



В следующем примере показано связанное объявление элементов управления **рецентитемс** .


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Сведения об элементе

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да


## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления меню приложения](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Элемент управления "Недавние элементы"](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





