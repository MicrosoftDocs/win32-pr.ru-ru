---
title: Инриббонгаллери. Менуграупс, свойство
description: Представляет контейнер для набора пунктов раскрывающегося меню элемента управления коллекции In-Ribbon.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Лента Windows для свойства Инриббонгаллери. Менуграупс
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071684"
---
# <a name="inribbongallerymenugroups-property"></a>Инриббонгаллери. Менуграупс, свойство

Представляет контейнер для набора пунктов раскрывающегося меню элемента управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .

## <a name="usage"></a>Использование

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                         | Описание                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                     |
|-----------------------------------------------------------------------------|
| [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .

В этом разделе кода показано объявление элемента управления **инриббонгаллери. менуграупс** .


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
</dt> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> </dl>

 

 





