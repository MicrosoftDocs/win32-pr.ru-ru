---
description: Соединение строк — это общая область, сформированная двумя строками, конец которых соответствует или перекрывается.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Соединение строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066978"
---
# <a name="joining-lines"></a>Соединение строк

Соединение строк — это общая область, сформированная двумя строками, конец которых соответствует или перекрывается. Windows GDI+ предоставляет четыре стиля соединения линий: срез, скос, круглый и срез обрезаны. Тип подключения линии является свойством класса [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . При указании стиля соединения линий для пера и последующем использовании этого пера для рисования контура заданный стиль соединения применяется ко всем подключенным линиям в пути.

Стиль объединения линий можно указать с помощью метода [**Pen:: сетлинежоин**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) класса [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . В следующем примере показано соединение багетной линии между горизонтальной линией и вертикальной линией:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



На следующем рисунке показано соединение с рельефной линией.

![Иллюстрация, показывающая две строки в правом углом с рельефным соединением](images/pens5.png)

В предыдущем примере значение (**линежоинбевел**), передаваемое методу [**Pen:: сетлинежоин**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) , является элементом перечисления [**линежоин**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .

 

 



