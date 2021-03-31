---
title: Сплитбуттонгаллери. Менуграупс, свойство
description: Представляет контейнер для набора элементов раскрывающегося меню в элементе управления Сплитбуттонгаллери.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Лента Windows для свойства Сплитбуттонгаллери. Менуграупс
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135874"
---
# <a name="splitbuttongallerymenugroups-property"></a>Сплитбуттонгаллери. Менуграупс, свойство

Представляет контейнер для набора элементов раскрывающегося меню в элементе управления [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

## <a name="usage"></a>Использование

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                         | Описание                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                           |
|-----------------------------------------------------------------------------------|
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Комментарии

Обязательный.

Должен выполняться ровно один раз для каждого элемента [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **сплитбуттонгаллери. менуграупс** .

В этом разделе кода показано объявление элемента управления **сплитбуттонгаллери. менуграупс** .


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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> </dl>

 

 





