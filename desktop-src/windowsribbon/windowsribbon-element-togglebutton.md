---
title: ToggleButton, элемент
description: Представляет элемент управления "выключатель".
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- элемент ToggleButton Windows лента
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c92a5985b560738d7119a6c5de354ad703f58894
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626970"
---
# <a name="togglebutton-element"></a>ToggleButton, элемент

Представляет элемент управления ["выключатель"](windowsribbon-controls-togglebutton.md) .

## <a name="usage"></a>Использование

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>Аппликатиондефаултс. Check</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Этот атрибут допустим, только если элемент <strong>ToggleButton</strong> является дочерним для <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>. <br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
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



| Элемент                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Группа**](windowsribbon-element-group.md)<br/>                                                                   |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**Куиккакцесстулбар. Аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton. Буттонитем**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Remarks

Необязательный или обязательный в зависимости от родительского элемента.

Может встречаться не более одного раза для каждого элемента [**SplitButton. буттонитем**](windowsribbon-element-splitbutton-buttonitem.md) .

Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **ToggleButton** .

В этом разделе кода показано объявление элемента **ToggleButton** в элементе [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Да       |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления "выключатель"](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





