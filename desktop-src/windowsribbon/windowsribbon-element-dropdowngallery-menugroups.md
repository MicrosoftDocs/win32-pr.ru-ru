---
title: Дропдовнгаллери. Менуграупс, свойство
description: Представляет контейнер для набора элементов раскрывающегося меню в элементе управления коллекции Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Лента Windows для свойства Дропдовнгаллери. Менуграупс
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719208"
---
# <a name="dropdowngallerymenugroups-property"></a>Дропдовнгаллери. Менуграупс, свойство

Представляет контейнер для набора пунктов раскрывающегося меню в [раскрывающемся](windowsribbon-controls-dropdowngallery.md) элементе управления "Коллекция".

## <a name="usage"></a>Использование

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
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
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Комментарии

Обязательный.

Должен выполняться ровно один раз для каждого элемента [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **дропдовнгаллери. менуграупс** .

В этом разделе кода показано объявление элемента управления **дропдовнгаллери. менуграупс** в [раскрывающейся](windowsribbon-controls-dropdowngallery.md) области команд коллекции.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент управления "раскрывающийся список"**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> </dl>

 

 





