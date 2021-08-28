---
title: Куиккакцесстулбар, элемент
description: Представляет панель быстрого доступа (QAT), маленькую панель инструментов, которая отображает ярлыки для команд ленты.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- элемент куиккакцесстулбар Windows лента
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa9d097823d049d145c25d1027bdb5a67d688692
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624170"
---
# <a name="quickaccesstoolbar-element"></a>Куиккакцесстулбар, элемент

Представляет [панель быстрого доступа (QAT)](windowsribbon-controls-quickaccesstoolbar.md), маленькую панель инструментов, которая отображает ярлыки для команд ленты.

## <a name="usage"></a>Использование

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
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
<td><strong>кустомизекомманднаме</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Вставляет дополнительный элемент команды в меню QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                   | Описание                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Куиккакцесстулбар. Аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Лента. Куиккакцесстулбар**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен выполняться ровно один раз для каждой [**ленты. куиккакцесстулбар**](windowsribbon-element-ribbon-quickaccesstoolbar.md).

Элементы в QAT могут быть добавлены или удалены во время выполнения.

Для обеспечения согласованности между приложениями ленты рекомендуется запустить диалоговое окно настройки QAT с помощью обработчика команд *кустомизекомманднаме* .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для **куиккакцесстулбар**.

В этом разделе кода показано объявление команды **куиккакцесстулбар** .


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



В этом разделе кода показано объявление элемента управления **куиккакцесстулбар** .


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

* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





