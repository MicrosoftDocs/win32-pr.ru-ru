---
title: Полотно и визуальные интерфейсы для модели XPS
description: В этом разделе описывается, как использовать интерфейсы, связанные с холстом, в API документов XPS в OM.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f7214a06779d997331f57a22ae29217e5cabdd635d0c3feac85bd8a3070065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469273"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Работа с холстом и визуальными интерфейсами в модели XPS

В этом разделе описывается, как использовать интерфейсы, связанные с холстом, в API документов XPS в OM.

| Имя интерфейса                                  | Логические дочерние интерфейсы                                                                                                                    | Описание                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Базовый класс интерфейсов, определяющих визуальные объекты, такие как текст и графика.<br/> Визуальные объекты можно собирать в интерфейсе [**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .<br/> |
| [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Коллекция визуальных объектов, которые можно рассматривать как один визуальный объект.<br/>                                                                                                                                |

[**Икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) является базовым интерфейсом; видимые объекты страницы наследуются от нее. [**Икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) наследует от [**икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) и позволяет группировать и обрабатывать многие другие визуальные элементы в виде одного визуального элемента. Например, можно использовать интерфейс [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) для создания баннера страницы, содержащего коллекцию текстовых и графических элементов. Такой баннер может содержать логотип, слоган компании и адрес компании. Все эти элементы можно поместить в [**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) интерфейса [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , а затем применить одно преобразование к объекту [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , чтобы изменить его размер на определенную страницу. Это гораздо проще, чем вычисления и применение преобразования к каждому отдельному визуальному компоненту в баннере.

Можно также использовать холст для изменения размера содержимого страницы в соответствии с текущим размером страницы. Для этого поместите все содержимое страницы в один холст, а затем примените соответствующее преобразование, чтобы вписать холст в текущий размер страницы. Это также гораздо проще, чем пытаться изменить размер каждого визуального элемента в коллекции визуальных элементов на странице.

## <a name="move-page-contents-to-a-canvas"></a>Перемещение содержимого страницы на холст

В следующем примере кода содержимое страницы перемещается на холст.

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

## <a name="related-topics"></a>Связанные темы

<dl> 
  
  <dt>[**Интерфейс икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt> интерфейса
  <dt>[**икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>интерфейса <dt>[**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
</dl>
