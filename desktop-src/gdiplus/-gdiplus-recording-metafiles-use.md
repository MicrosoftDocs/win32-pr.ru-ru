---
description: Класс Metafile, который наследует от класса Image, позволяет записывать последовательность команд рисования.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Запись метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984440"
---
# <a name="recording-metafiles"></a>Запись метафайлов

Класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , который наследует от класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , позволяет записывать последовательность команд рисования. Записанные команды могут храниться в памяти, сохраняться в файле или сохраняться в потоке. Метафайлы могут содержать векторную графику, растровые изображения и текст.

В следующем примере создается объект [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Код использует объект **Metafile** для записи последовательности графических команд, а затем сохраняет записанные команды в файл с именем самплеметафиле. EMF. Обратите внимание, что конструктор **Metafile** получает маркер контекста устройства, а [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктор получает адрес объекта **Metafile** . Запись останавливается (и записанные команды сохраняются в файл), когда объект **Graphics** выходит из области действия. Последние две строки кода отображают метафайл путем создания нового **графического** объекта и передачи адреса объекта **метафайла** методу **DrawImage** этого **графического** объекта. Обратите внимание, что код использует тот же объект **Metafile** для записи и вывода (воспроизведения) метафайла.


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Чтобы записать метафайл, необходимо создать [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе объекта [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Запись метафайла заканчивается, когда объект **Graphics** удаляется или выходит за пределы области.

 

Метафайл содержит собственное состояние графики, которое определяется [**графическим**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объектом, используемым для записи метафайла. Все свойства **графического** объекта (область обрезки, универсальное преобразование, режим сглаживания и т. д.), заданные при записи метафайла, будут храниться в метафайле. При отображении метафайла рисование выполняется в соответствии с сохраненными свойствами.

В следующем примере предполагается, что для режима сглаживания было задано значение Смусингмоденормал во время записи метафайла. Несмотря на то, что режим сглаживания объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , используемый для воспроизведения, имеет значение смусингмодехигхкуалити, метафайл будет воспроизводиться в соответствии с параметром смусингмоденормал. Это режим сглаживания, заданный во время записи, а не в режиме сглаживания, установленном перед воспроизведением.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



