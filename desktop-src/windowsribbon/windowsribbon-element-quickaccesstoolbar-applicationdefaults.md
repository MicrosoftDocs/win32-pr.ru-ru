---
title: Куиккакцесстулбар. Аппликатиондефаултс, свойство
description: Представляет контейнер для команд по умолчанию на панели инструментов быстрого доступа (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Лента Windows для свойства Куиккакцесстулбар. Аппликатиондефаултс
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701028"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Куиккакцесстулбар. Аппликатиондефаултс, свойство

Представляет контейнер для команд по умолчанию на [панели инструментов быстрого доступа (QAT)](windowsribbon-controls-quickaccesstoolbar.md).

## <a name="usage"></a>Использование

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



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
<td><a href="windowsribbon-element-button.md"><strong>Кнопка</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>Установка</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/>
<blockquote>
[!Note]<br />
Windows 8 и более поздние версии.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>дропдовнгаллери</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/>
<blockquote>
[!Note]<br />
Windows 8 и более поздние версии.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>инриббонгаллери</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/>
<blockquote>
[!Note]<br />
Windows 8 и более поздние версии.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>сплитбуттонгаллери</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/>
<blockquote>
[!Note]<br />
Windows 8 и более поздние версии.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>Должна повториться хотя бы один раз.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md).

Необходимо указать минимум один дочерний элемент.

Можно указать не более 20 дочерних элементов.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [**куиккакцесстулбар**](windowsribbon-element-quickaccesstoolbar.md).

В этом разделе кода показано объявление элемента управления **куиккакцесстулбар. аппликатиондефаултс** .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





