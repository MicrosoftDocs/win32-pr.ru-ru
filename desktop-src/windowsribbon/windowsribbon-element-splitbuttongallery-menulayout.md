---
title: Сплитбуттонгаллери. Менулайаут, свойство
description: Представляет контейнер для макетов раскрывающегося меню коллекции разделенных кнопок.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- сплитбуттонгаллери. менулайаут, свойство Windows лента
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40cf184d6122fc40041cfb77953bba2b7950d9d1a957d99aae659633ee5c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706902"
---
# <a name="splitbuttongallerymenulayout-property"></a>Сплитбуттонгаллери. Менулайаут, свойство

Представляет контейнер для макетов раскрывающегося меню [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md) .

## <a name="usage"></a>Использование

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Описание                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)<br/>         | Должно выполняться только один раз<br/> <br/> |
| [**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md)<br/> | Должно выполняться только один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

> [!Note]  
> Допускается не более одного дочернего элемента ([**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md).

В этом разделе кода показано объявление элемента управления **сплитбуттонгаллери. менулайаут** .


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> </dl>

 

 





