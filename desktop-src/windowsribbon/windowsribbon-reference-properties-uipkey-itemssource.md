---
title: UI_PKEY_ItemsSource
description: Определяет \_ свойство ItemsSource PKEY пользовательского интерфейса \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793254"
---
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="d94c1-103">ItemsSource пользовательского интерфейса \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d94c1-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="d94c1-104">Определяет \_ свойство ItemsSource PKEY пользовательского интерфейса \_ .</span><span class="sxs-lookup"><span data-stu-id="d94c1-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="d94c1-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d94c1-105">Remarks</span></span>

<span data-ttu-id="d94c1-106">Элемент пользовательского интерфейса \_ PKEY \_ класса используется приложением для запроса коллекции элементов в элементе управления галереи, например панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="d94c1-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="d94c1-107">Значение свойства является объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="d94c1-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="d94c1-108">Каждый элемент в этом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) должен реализовывать [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , чтобы предоставить доступ к свойствам только для чтения, связанным с элементом, таким как метка или изображение.</span><span class="sxs-lookup"><span data-stu-id="d94c1-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="d94c1-109">Чтобы добавлять или удалять элементы в элементе управления "Коллекция" во время выполнения, используйте методы [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="d94c1-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="d94c1-110">На следующем снимке экрана показана коллекция элементов в меню [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="d94c1-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![снимок экрана: Отображение категорий в коллекции лент.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="d94c1-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d94c1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d94c1-113">Свойства коллекции</span><span class="sxs-lookup"><span data-stu-id="d94c1-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 