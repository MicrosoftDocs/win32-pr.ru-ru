---
description: Чтобы заполнить форму сплошным цветом, создайте объект SolidBrush, а затем передайте адрес этого объекта SolidBrush в качестве аргумента в один из методов Fill класса Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Заполнение фигуры сплошным цветом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036722"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Заполнение фигуры сплошным цветом

Чтобы заполнить форму сплошным цветом, создайте объект [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , а затем передайте адрес этого объекта **SolidBrush** в качестве аргумента в один из методов Fill класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . В следующем примере показано, как заполнить эллипс красным цветом:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



В предыдущем примере конструктор [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) принимает ссылку на объект [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) в качестве единственного аргумента. Значения, используемые конструктором **Color** , представляют альфа-, красный, зеленый и синий компоненты цвета. Каждое из этих значений должно находиться в диапазоне от 0 до 255. Первая 255 указывает, что цвет является полностью непрозрачным, а второй 255 указывает, что красный компонент имеет полную интенсивность. Два нуля указывают, что зеленый и синий компоненты имеют интенсивность 0.

Четыре числа (0, 0, 100, 60), передаваемые методу [**Graphics:: филлеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) , определяют расположение и размер ограничивающего прямоугольника для эллипса. Прямоугольник содержит левый верхний угол (0, 0), ширину 100 и высоту 60.

 

 
