---
title: UI_PKEY_Categories
description: Определяет свойство "категории" пользовательского интерфейса \_ \_ .
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700889"
---
# <a name="ui_pkey_categories"></a>\_Категории PKEY пользовательского интерфейса \_

Определяет свойство "категории" пользовательского интерфейса \_ \_ .

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Комментарии

\_Категории PKEY пользовательского интерфейса \_ используются приложением для запроса категорий, используемых для группирования связанных элементов в элементе управления галереи.

Значение свойства — это объект [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , в котором каждый элемент в коллекции представляет категорию.

Каждый элемент в этом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) должен реализовывать [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , чтобы предоставить доступ к свойствам только для чтения, связанным с элементом, таким как метка или изображение.

Чтобы добавлять или удалять элементы в элементе управления "Коллекция" во время выполнения, используйте различные методы [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

На следующем снимке экрана показано использование двух категорий, **фигур выделения** и **параметров выбора** в меню [**SplitButton**](windowsribbon-element-splitbutton.md) .

![снимок экрана, на котором показаны две категории: фигуры выделения и параметры выбора в элементе управления сплитбуттонгаллери.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства коллекции](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[КодТипа пользовательского интерфейса \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 