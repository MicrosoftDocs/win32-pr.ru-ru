---
title: Элемент счетчика
description: Представляет элемент управления "Счетчик".
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Лента Windows для элемента счетчика
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1f9727dc7fbad8be24c15f0b1f551b021294dd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104069505"
---
# <a name="spinner-element"></a>Элемент счетчика

Представляет элемент управления " [Счетчик](windowsribbon-controls-spinner.md) ".

## <a name="usage"></a>Использование

``` syntax
<Spinner
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



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>             |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Группа**](windowsribbon-element-group.md)<br/>                           |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                   |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может происходить один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md) или [**Group**](windowsribbon-element-group.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [счетчика](windowsribbon-controls-spinner.md).

В этом разделе кода показаны объявления команд **счетчика** с элементом [**группы**](windowsribbon-element-group.md) , который выступает в качестве родительского контейнера для элемента **счетчика** .


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



В этом разделе кода показаны объявления элемента управления " **Счетчик** ".


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Да       |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления "Счетчик"](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





