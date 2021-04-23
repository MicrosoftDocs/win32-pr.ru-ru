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
# <a name="recording-metafiles"></a><span data-ttu-id="bf984-103">Запись метафайлов</span><span class="sxs-lookup"><span data-stu-id="bf984-103">Recording Metafiles</span></span>

<span data-ttu-id="bf984-104">Класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , который наследует от класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , позволяет записывать последовательность команд рисования.</span><span class="sxs-lookup"><span data-stu-id="bf984-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="bf984-105">Записанные команды могут храниться в памяти, сохраняться в файле или сохраняться в потоке.</span><span class="sxs-lookup"><span data-stu-id="bf984-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="bf984-106">Метафайлы могут содержать векторную графику, растровые изображения и текст.</span><span class="sxs-lookup"><span data-stu-id="bf984-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="bf984-107">В следующем примере создается объект [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="bf984-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="bf984-108">Код использует объект **Metafile** для записи последовательности графических команд, а затем сохраняет записанные команды в файл с именем самплеметафиле. EMF.</span><span class="sxs-lookup"><span data-stu-id="bf984-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="bf984-109">Обратите внимание, что конструктор **Metafile** получает маркер контекста устройства, а [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктор получает адрес объекта **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="bf984-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="bf984-110">Запись останавливается (и записанные команды сохраняются в файл), когда объект **Graphics** выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="bf984-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="bf984-111">Последние две строки кода отображают метафайл путем создания нового **графического** объекта и передачи адреса объекта **метафайла** методу **DrawImage** этого **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="bf984-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="bf984-112">Обратите внимание, что код использует тот же объект **Metafile** для записи и вывода (воспроизведения) метафайла.</span><span class="sxs-lookup"><span data-stu-id="bf984-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


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
> <span data-ttu-id="bf984-113">Чтобы записать метафайл, необходимо создать [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе объекта [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="bf984-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="bf984-114">Запись метафайла заканчивается, когда объект **Graphics** удаляется или выходит за пределы области.</span><span class="sxs-lookup"><span data-stu-id="bf984-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="bf984-115">Метафайл содержит собственное состояние графики, которое определяется [**графическим**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объектом, используемым для записи метафайла.</span><span class="sxs-lookup"><span data-stu-id="bf984-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="bf984-116">Все свойства **графического** объекта (область обрезки, универсальное преобразование, режим сглаживания и т. д.), заданные при записи метафайла, будут храниться в метафайле.</span><span class="sxs-lookup"><span data-stu-id="bf984-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="bf984-117">При отображении метафайла рисование выполняется в соответствии с сохраненными свойствами.</span><span class="sxs-lookup"><span data-stu-id="bf984-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="bf984-118">В следующем примере предполагается, что для режима сглаживания было задано значение Смусингмоденормал во время записи метафайла.</span><span class="sxs-lookup"><span data-stu-id="bf984-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="bf984-119">Несмотря на то, что режим сглаживания объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , используемый для воспроизведения, имеет значение смусингмодехигхкуалити, метафайл будет воспроизводиться в соответствии с параметром смусингмоденормал.</span><span class="sxs-lookup"><span data-stu-id="bf984-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="bf984-120">Это режим сглаживания, заданный во время записи, а не в режиме сглаживания, установленном перед воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="bf984-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



