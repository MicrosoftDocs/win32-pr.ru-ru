---
description: Замкнутую фигуру можно заполнить текстурой с помощью класса Image и класса TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Заполнение фигуры текстурой изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156187"
---
# <a name="filling-a-shape-with-an-image-texture"></a>Заполнение фигуры текстурой изображения

Замкнутую фигуру можно заполнить текстурой с помощью класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и класса [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .

В следующем примере заливка эллипса осуществляется с помощью изображения. Код конструирует объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , а затем передает адрес этого объекта **Image** в качестве аргумента в конструктор [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) . Третья инструкция Code масштабирует изображение, а четвертый оператор заполняет эллипс повторяющимися копиями масштабированного изображения:


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



В предыдущем примере кода метод [**TextureBrush:: сеттрансформ**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) задает преобразование, которое применяется к изображению перед его прорисовкой. Предположим, что исходное изображение имеет ширину 640 пикселей и высоту 480 пикселей. Преобразование сжимает изображение до 75 × 75, устанавливая горизонтальные и вертикальные значения масштабирования.

> [!Note]  
> В предыдущем примере размер изображения составляет 75 × 75, а размер эллипса — 150 × 250. Поскольку изображение меньше, чем заливка, эллипс заполняется изображением. Мозаичное заполнение означает, что изображение повторяется горизонтально и вертикально до тех пор, пока не будет достигнута граница фигуры. Дополнительные сведения о мозаичном заполнении см. в разделе [Мозаичное заполнение фигуры изображением](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



