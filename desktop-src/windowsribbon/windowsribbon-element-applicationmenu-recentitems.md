---
title: Аппликатионмену. Рецентитемс, свойство
description: Представляет контейнер для элемента управления "Недавние элементы" в меню "приложение".
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- аппликатионмену. рецентитемс, свойство Windows лента
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630379"
---
# <a name="applicationmenurecentitems-property"></a>Аппликатионмену. Рецентитемс, свойство

Представляет контейнер для элемента управления " [недавние элементы](windowsribbon-controls-recentitems.md) " в [меню "приложение](windowsribbon-controls-applicationmenu.md)".

## <a name="usage"></a>Использование

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
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
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Описание                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**рецентитемс**](windowsribbon-element-recentitems.md)<br/> | Должно выполняться только один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                     |
|-----------------------------------------------------------------------------|
| [**аппликатионмену**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**аппликатионмену**](windowsribbon-element-applicationmenu.md) .

Элемент управления [недавние элементы](windowsribbon-controls-recentitems.md) отображает список недавно использовавшихся элементов приложения ленты.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента управления [недавние элементы](windowsribbon-controls-recentitems.md) .

В следующем примере показано объявление команды [**рецентитемс**](windowsribbon-element-recentitems.md) .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



В следующем примере показаны связанные объявления элементов управления **аппликатионмену. рецентитемс** и [**рецентитемс**](windowsribbon-element-recentitems.md) .


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления меню приложения](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Элемент управления "Недавние элементы"](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





