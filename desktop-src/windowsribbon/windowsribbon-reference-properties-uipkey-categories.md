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
# <a name="ui_pkey_categories"></a><span data-ttu-id="c210e-103">\_Категории PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="c210e-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="c210e-104">Определяет свойство "категории" пользовательского интерфейса \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c210e-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="c210e-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c210e-105">Remarks</span></span>

<span data-ttu-id="c210e-106">\_Категории PKEY пользовательского интерфейса \_ используются приложением для запроса категорий, используемых для группирования связанных элементов в элементе управления галереи.</span><span class="sxs-lookup"><span data-stu-id="c210e-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="c210e-107">Значение свойства — это объект [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , в котором каждый элемент в коллекции представляет категорию.</span><span class="sxs-lookup"><span data-stu-id="c210e-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="c210e-108">Каждый элемент в этом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) должен реализовывать [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , чтобы предоставить доступ к свойствам только для чтения, связанным с элементом, таким как метка или изображение.</span><span class="sxs-lookup"><span data-stu-id="c210e-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="c210e-109">Чтобы добавлять или удалять элементы в элементе управления "Коллекция" во время выполнения, используйте различные методы [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="c210e-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="c210e-110">На следующем снимке экрана показано использование двух категорий, **фигур выделения** и **параметров выбора** в меню [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="c210e-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![снимок экрана, на котором показаны две категории: фигуры выделения и параметры выбора в элементе управления сплитбуттонгаллери.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="c210e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c210e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c210e-113">Свойства коллекции</span><span class="sxs-lookup"><span data-stu-id="c210e-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="c210e-114">КодТипа пользовательского интерфейса \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="c210e-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 