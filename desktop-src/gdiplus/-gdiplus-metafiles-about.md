---
description: Windows GDI+ предоставляет класс Metafile, чтобы можно было записывать и отображать метафайлы.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Метафайлы (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343405"
---
# <a name="metafiles-gdi"></a><span data-ttu-id="8f199-103">Метафайлы (GDI+)</span><span class="sxs-lookup"><span data-stu-id="8f199-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="8f199-104">Windows GDI+ предоставляет класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , чтобы можно было записывать и отображать метафайлы.</span><span class="sxs-lookup"><span data-stu-id="8f199-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="8f199-105">Метафайл, также называемый векторным изображением, — это изображение, которое хранится в виде последовательности команд и параметров рисования.</span><span class="sxs-lookup"><span data-stu-id="8f199-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="8f199-106">Команды и параметры, записанные в объекте **Metafile** , могут храниться в памяти или сохраняться в файле или потоке.</span><span class="sxs-lookup"><span data-stu-id="8f199-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="8f199-107">GDI+ может отображать метафайлы, сохраненные в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="8f199-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="8f199-108">Формат WMF (WMF)</span><span class="sxs-lookup"><span data-stu-id="8f199-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="8f199-109">EMF (Enhanced Metafile —расширенный метафайл)</span><span class="sxs-lookup"><span data-stu-id="8f199-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="8f199-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="8f199-110">EMF+</span></span>

<span data-ttu-id="8f199-111">GDI+ может записывать метафайлы в форматах EMF и EMF +, но не в формате WMF.</span><span class="sxs-lookup"><span data-stu-id="8f199-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="8f199-112">EMF + — это расширение EMF, позволяющее сохранять записи GDI+.</span><span class="sxs-lookup"><span data-stu-id="8f199-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="8f199-113">Существует два варианта формата EMF +: EMF + only и EMF + Dual.</span><span class="sxs-lookup"><span data-stu-id="8f199-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="8f199-114">Только Метафайлы EMF + содержат только записи GDI+.</span><span class="sxs-lookup"><span data-stu-id="8f199-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="8f199-115">Такие метафайлы могут отображаться в GDI+, но не в Windows интерфейс графических устройств (GDI).</span><span class="sxs-lookup"><span data-stu-id="8f199-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="8f199-116">Метафайлы EMF + Dual содержат записи GDI+ и GDI.</span><span class="sxs-lookup"><span data-stu-id="8f199-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="8f199-117">Каждая запись GDI+ в метафайле EMF + Dual объединяется с альтернативной записью GDI.</span><span class="sxs-lookup"><span data-stu-id="8f199-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="8f199-118">Такие метафайлы могут отображаться в GDI+ или GDI.</span><span class="sxs-lookup"><span data-stu-id="8f199-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="8f199-119">В следующем примере один параметр и одна команда рисования записываются в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="8f199-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="8f199-120">Обратите внимание, что в примере создается объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и конструктор объекта **Graphics** получает адрес объекта [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="8f199-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



<span data-ttu-id="8f199-121">Как показано в предыдущем примере, класс [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) является ключом к записи инструкций и параметров в объекте [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="8f199-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="8f199-122">Любой вызов метода **графического** объекта может быть записан в объект **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="8f199-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="8f199-123">Аналогичным образом можно задать любое свойство объекта **Graphics** и записать этот параметр в объект **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="8f199-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="8f199-124">Запись заканчивается, когда объект **Graphics** удаляется или выходит за пределы области.</span><span class="sxs-lookup"><span data-stu-id="8f199-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="8f199-125">В следующем примере показан метафайл, созданный в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="8f199-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="8f199-126">Метафайл отображается в левом верхнем углу в (100, 100).</span><span class="sxs-lookup"><span data-stu-id="8f199-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="8f199-127">В следующем примере записывается несколько параметров свойств (область отсечения, универсальное преобразование и режим сглаживания) в объекте [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="8f199-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="8f199-128">Затем код записывает несколько инструкций по рисованию.</span><span class="sxs-lookup"><span data-stu-id="8f199-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="8f199-129">Инструкции и параметры сохраняются в файле на диске.</span><span class="sxs-lookup"><span data-stu-id="8f199-129">The instructions and settings are saved in a disk file.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



<span data-ttu-id="8f199-130">В следующем примере отображается изображение метафайла, созданное в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="8f199-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="8f199-131">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="8f199-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="8f199-132">Обратите внимание на сглаживание, Область эллиптической обрезки и поворот на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="8f199-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![снимок экрана окна, содержащего эллипс, заполненный строками, находящимися за пределами эллипса](images/aboutgdip05-art00.png)

 

 



