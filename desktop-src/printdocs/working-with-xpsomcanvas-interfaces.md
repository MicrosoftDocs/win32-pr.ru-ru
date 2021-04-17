---
title: Полотно и визуальные интерфейсы для модели XPS
description: В этом разделе описывается, как использовать интерфейсы, связанные с холстом, в API документов XPS в OM.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8bd15333c2786801900b09b32eb6cd59121af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693177"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="b70d4-103">Работа с холстом и визуальными интерфейсами в модели XPS</span><span class="sxs-lookup"><span data-stu-id="b70d4-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="b70d4-104">В этом разделе описывается, как использовать интерфейсы, связанные с холстом, в API документов XPS в OM.</span><span class="sxs-lookup"><span data-stu-id="b70d4-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="b70d4-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="b70d4-105">Interface name</span></span>                                  | <span data-ttu-id="b70d4-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="b70d4-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="b70d4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b70d4-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b70d4-108">**икспсомвисуал**</span><span class="sxs-lookup"><span data-stu-id="b70d4-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="b70d4-109">**икспсомканвас**</span><span class="sxs-lookup"><span data-stu-id="b70d4-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="b70d4-110">**икспсомглифс**</span><span class="sxs-lookup"><span data-stu-id="b70d4-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="b70d4-111">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="b70d4-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="b70d4-112">Базовый класс интерфейсов, определяющих визуальные объекты, такие как текст и графика.</span><span class="sxs-lookup"><span data-stu-id="b70d4-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="b70d4-113">Визуальные объекты можно собирать в интерфейсе [**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .</span><span class="sxs-lookup"><span data-stu-id="b70d4-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="b70d4-114">**икспсомканвас**</span><span class="sxs-lookup"><span data-stu-id="b70d4-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="b70d4-115">**икспсомканвас**</span><span class="sxs-lookup"><span data-stu-id="b70d4-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="b70d4-116">**икспсомглифс**</span><span class="sxs-lookup"><span data-stu-id="b70d4-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="b70d4-117">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="b70d4-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="b70d4-118">Коллекция визуальных объектов, которые можно рассматривать как один визуальный объект.</span><span class="sxs-lookup"><span data-stu-id="b70d4-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |
<span data-ttu-id="b70d4-119">[**Икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) является базовым интерфейсом; видимые объекты страницы наследуются от нее.</span><span class="sxs-lookup"><span data-stu-id="b70d4-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="b70d4-120">[**Икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) наследует от [**икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) и позволяет группировать и обрабатывать многие другие визуальные элементы в виде одного визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="b70d4-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="b70d4-121">Например, можно использовать интерфейс [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) для создания баннера страницы, содержащего коллекцию текстовых и графических элементов.</span><span class="sxs-lookup"><span data-stu-id="b70d4-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="b70d4-122">Такой баннер может содержать логотип, слоган компании и адрес компании.</span><span class="sxs-lookup"><span data-stu-id="b70d4-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="b70d4-123">Все эти элементы можно поместить в [**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) интерфейса [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , а затем применить одно преобразование к объекту [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , чтобы изменить его размер на определенную страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="b70d4-124">Это гораздо проще, чем вычисления и применение преобразования к каждому отдельному визуальному компоненту в баннере.</span><span class="sxs-lookup"><span data-stu-id="b70d4-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="b70d4-125">Можно также использовать холст для изменения размера содержимого страницы в соответствии с текущим размером страницы.</span><span class="sxs-lookup"><span data-stu-id="b70d4-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="b70d4-126">Для этого поместите все содержимое страницы в один холст, а затем примените соответствующее преобразование, чтобы вписать холст в текущий размер страницы.</span><span class="sxs-lookup"><span data-stu-id="b70d4-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="b70d4-127">Это также гораздо проще, чем пытаться изменить размер каждого визуального элемента в коллекции визуальных элементов на странице.</span><span class="sxs-lookup"><span data-stu-id="b70d4-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="b70d4-128">Перемещение содержимого страницы на холст</span><span class="sxs-lookup"><span data-stu-id="b70d4-128">Move page contents to a canvas</span></span>

<span data-ttu-id="b70d4-129">В следующем примере кода содержимое страницы перемещается на холст.</span><span class="sxs-lookup"><span data-stu-id="b70d4-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="b70d4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b70d4-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="b70d4-131">
  <dt>[\*\*Интерфейс икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt> интерфейса
  <dt>[\*\*икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>интерфейса <dt>[\*\*икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
</span><span class="sxs-lookup"><span data-stu-id="b70d4-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
