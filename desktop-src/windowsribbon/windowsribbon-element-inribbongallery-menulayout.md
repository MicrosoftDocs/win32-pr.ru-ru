---
title: Инриббонгаллери. Менулайаут, свойство
description: Представляет контейнер для макетов раскрывающихся меню коллекции In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Лента Windows для свойства Инриббонгаллери. Менулайаут
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071208"
---
# <a name="inribbongallerymenulayout-property"></a>Инриббонгаллери. Менулайаут, свойство

Представляет контейнер для макетов раскрывающихся меню [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .

## <a name="usage"></a>Использование

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Описание                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)<br/>         | Должно выполняться только один раз<br/> <br/> |
| [**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md)<br/> | Должно выполняться только один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                     |
|-----------------------------------------------------------------------------|
| [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .

> [!Note]  
> Допускается не более одного дочернего элемента ([**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [коллекции на ленте](windowsribbon-controls-inribbongallery.md).

В этом разделе кода показано объявление элемента управления **инриббонгаллери. менулайаут** .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления "Коллекция ленты"](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> </dl>

 

 





