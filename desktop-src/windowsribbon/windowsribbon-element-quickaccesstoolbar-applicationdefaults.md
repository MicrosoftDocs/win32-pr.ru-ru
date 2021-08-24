---
title: Куиккакцесстулбар. Аппликатиондефаултс, свойство
description: Представляет контейнер для команд по умолчанию на панели инструментов быстрого доступа (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- куиккакцесстулбар. аппликатиондефаултс, свойство Windows лента
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473750"
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




| Элемент | Описание | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Кнопка</strong></a><br /> | Должна повториться хотя бы один раз.<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>Установка</strong></a><br /> | Должна повториться хотя бы один раз.<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br /> | Должна повториться хотя бы один раз.<br /><blockquote>[!Note]<br />Windows 8 и более поздних версий.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>дропдовнгаллери</strong></a><br /> | Должна повториться хотя бы один раз.<br /><blockquote>[!Note]<br />Windows 8 и более поздних версий.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>инриббонгаллери</strong></a><br /> | Должна повториться хотя бы один раз.<br /><blockquote>[!Note]<br />Windows 8 и более поздних версий.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>сплитбуттонгаллери</strong></a><br /> | Должна повториться хотя бы один раз.<br /><blockquote>[!Note]<br />Windows 8 и более поздних версий.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | Должна повториться хотя бы один раз.<br /><br /> | 




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
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





