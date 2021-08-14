---
title: UI_PKEY_ItemsSource
description: Определяет \_ свойство ItemsSource PKEY пользовательского интерфейса \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201578"
---
# <a name="ui_pkey_itemssource"></a>ItemsSource пользовательского интерфейса \_ PKEY \_

Определяет \_ свойство ItemsSource PKEY пользовательского интерфейса \_ .

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Remarks

Элемент пользовательского интерфейса \_ PKEY \_ класса используется приложением для запроса коллекции элементов в элементе управления галереи, например панели быстрого доступа (QAT).

Значение свойства является объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Каждый элемент в этом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) должен реализовывать [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , чтобы предоставить доступ к свойствам только для чтения, связанным с элементом, таким как метка или изображение.

Чтобы добавлять или удалять элементы в элементе управления "Коллекция" во время выполнения, используйте методы [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

На следующем снимке экрана показана коллекция элементов в меню [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .

![снимок экрана: Отображение категорий в коллекции лент.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства коллекции](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 