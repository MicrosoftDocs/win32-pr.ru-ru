---
description: Точечные рисунки должны сохраняться в файле, использующем установленный формат файла точечного рисунка, и иметь имя с расширением BMP.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Растровое хранилище
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155691"
---
# <a name="bitmap-storage"></a><span data-ttu-id="96f75-103">Растровое хранилище</span><span class="sxs-lookup"><span data-stu-id="96f75-103">Bitmap Storage</span></span>

<span data-ttu-id="96f75-104">Точечные рисунки должны сохраняться в файле, использующем установленный формат файла точечного рисунка, и иметь имя с расширением BMP.</span><span class="sxs-lookup"><span data-stu-id="96f75-104">Bitmaps should be saved in a file that uses the established bitmap file format and assigned a name with the three-character .bmp extension.</span></span> <span data-ttu-id="96f75-105">Установленный формат файла точечного рисунка состоит из структуры [**битмапфилехеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) , за которой следует структура [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)или [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .</span><span class="sxs-lookup"><span data-stu-id="96f75-105">The established bitmap file format consists of a [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure followed by a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure.</span></span> <span data-ttu-id="96f75-106">Массив структур [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (также называемый таблицей цветов) следует за структурой заголовка растровой информации.</span><span class="sxs-lookup"><span data-stu-id="96f75-106">An array of [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures (also called a color table) follows the bitmap information header structure.</span></span> <span data-ttu-id="96f75-107">За таблицей цветов следует второй массив индексов в таблице цветов (фактические данные точечного рисунка).</span><span class="sxs-lookup"><span data-stu-id="96f75-107">The color table is followed by a second array of indexes into the color table (the actual bitmap data).</span></span>

<span data-ttu-id="96f75-108">Формат файла точечного рисунка показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="96f75-108">The bitmap file format is shown in the following illustration.</span></span>

![Схема формата файла точечного рисунка, в котором показаны массивы битмапфилехеадер, битмапинфохеадер, ргбкуад и Color-index](images/csbmp-02.png)

<span data-ttu-id="96f75-110">Элементы структуры [**битмапфилехеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) указывают файл; Укажите размер файла в байтах; и укажите смещение от первого байта в заголовке до первого байта данных точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="96f75-110">The members of the [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure identify the file; specify the size of the file, in bytes; and specify the offset from the first byte in the header to the first byte of bitmap data.</span></span> <span data-ttu-id="96f75-111">Элементы структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)или [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) задают ширину и высоту точечного рисунка в пикселях; формат цвета (число цветовых плоскостей и цветовых битов на пиксель) устройства вывода, на котором был создан точечный рисунок; были ли сжаты данные растрового изображения до хранения и тип используемого сжатия; число байтов данных точечного рисунка; разрешение устройства вывода, на котором был создан точечный рисунок; и количество цветов, представленных в данных.</span><span class="sxs-lookup"><span data-stu-id="96f75-111">The members of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure specify the width and height of the bitmap, in pixels; the color format (count of color planes and color bits-per-pixel) of the display device on which the bitmap was created; whether the bitmap data was compressed before storage and the type of compression used; the number of bytes of bitmap data; the resolution of the display device on which the bitmap was created; and the number of colors represented in the data.</span></span> <span data-ttu-id="96f75-112">Структуры [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) задают значения интенсивности RGB для каждого цвета в палитре устройства.</span><span class="sxs-lookup"><span data-stu-id="96f75-112">The [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures specify the RGB intensity values for each of the colors in the device's palette.</span></span>

<span data-ttu-id="96f75-113">Массив цветового индекса связывает цвет в виде индекса со структурой [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , где каждый пиксель точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="96f75-113">The color-index array associates a color, in the form of an index to an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, with each pixel in a bitmap.</span></span> <span data-ttu-id="96f75-114">Таким же числом битов в массиве цветового индекса соответствует число в пикселях, превышающее количество бит, необходимых для индексации структур **ргбкуад** .</span><span class="sxs-lookup"><span data-stu-id="96f75-114">Thus, the number of bits in the color-index array equals the number of pixels times the number of bits needed to index the **RGBQUAD** structures.</span></span> <span data-ttu-id="96f75-115">Например, точечный рисунок 8x8 черно-белый имеет массив цветового индекса 8 \* 8 \* 1 = 64 бит, поскольку один бит необходим для индексации двух цветов.</span><span class="sxs-lookup"><span data-stu-id="96f75-115">For example, an 8x8 black-and-white bitmap has a color-index array of 8 \* 8 \* 1 = 64 bits, because one bit is needed to index two colors.</span></span> <span data-ttu-id="96f75-116">Redbrick.bmp, о которых упоминалось в статье [о точечных рисунках](about-bitmaps.md), представляет собой битовую карту размером 32x32, 16 цветов. его массив цветового индекса равен 32 \* 32 \* 4 = 4096 бит, так как четыре бита индексируют 16 цветов.</span><span class="sxs-lookup"><span data-stu-id="96f75-116">The Redbrick.bmp, mentioned in [About Bitmaps](about-bitmaps.md), is a 32x32 bitmap with 16 colors; its color-index array is 32 \* 32 \* 4 = 4096 bits because four bits index 16 colors.</span></span>

<span data-ttu-id="96f75-117">Чтобы создать массив цветового индекса для точечного рисунка сверху вниз, начните с верхней строки точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="96f75-117">To create a color-index array for a top-down bitmap, start at the top line in the bitmap.</span></span> <span data-ttu-id="96f75-118">Индекс [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) для цвета самого левого пикселя является первыми *n* битами в массиве цветового индекса (где *n* — число битов, необходимое для указания всех структур **ргбкуад** ).</span><span class="sxs-lookup"><span data-stu-id="96f75-118">The index of the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) for the color of the left-most pixel is the first *n* bits in the color-index array (where *n* is the number of bits needed to indicate all of the **RGBQUAD** structures).</span></span> <span data-ttu-id="96f75-119">Цвет следующего пикселя справа — это следующие *n* бит в массиве и т. д.</span><span class="sxs-lookup"><span data-stu-id="96f75-119">The color of the next pixel to the right is the next *n* bits in the array, and so forth.</span></span> <span data-ttu-id="96f75-120">Когда вы найдете правый пиксел в строке, продолжайте с самого левого пикселя в строке ниже.</span><span class="sxs-lookup"><span data-stu-id="96f75-120">After you reach the right-most pixel in the line, continue with the left-most pixel in the line below.</span></span> <span data-ttu-id="96f75-121">Продолжайте, пока не завершите все растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="96f75-121">Continue until you finish with the entire bitmap.</span></span> <span data-ttu-id="96f75-122">Если это растровое изображение снизу вверх, начните с нижней строки точечного рисунка, а не с верхней строки, по-прежнему переходите слева направо и переходите к верхней строке точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="96f75-122">If it is a bottom-up bitmap, start at the bottom line of the bitmap instead of the top line, still going from left to right, and continue to the top line of the bitmap.</span></span>

<span data-ttu-id="96f75-123">В следующих шестнадцатеричных выходных данных показано содержимое файла Redbrick.bmp.</span><span class="sxs-lookup"><span data-stu-id="96f75-123">The following hexadecimal output shows the contents of the file Redbrick.bmp.</span></span>


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



<span data-ttu-id="96f75-124">В следующей таблице показаны байты данных, связанные с структурами в файле точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="96f75-124">The following table shows the data bytes associated with the structures in a bitmap file.</span></span>



| <span data-ttu-id="96f75-125">Структура</span><span class="sxs-lookup"><span data-stu-id="96f75-125">Structure</span></span>                                    | <span data-ttu-id="96f75-126">Соответствующие байты</span><span class="sxs-lookup"><span data-stu-id="96f75-126">Corresponding bytes</span></span> |
|----------------------------------------------|---------------------|
| [<span data-ttu-id="96f75-127">**битмапфилехеадер**</span><span class="sxs-lookup"><span data-stu-id="96f75-127">**BITMAPFILEHEADER**</span></span>](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | <span data-ttu-id="96f75-128">0x00 0x0D</span><span class="sxs-lookup"><span data-stu-id="96f75-128">0x00 0x0D</span></span>           |
| <span data-ttu-id="96f75-129">[**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96f75-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span></span> | <span data-ttu-id="96f75-130">0x0E 0x35</span><span class="sxs-lookup"><span data-stu-id="96f75-130">0x0E 0x35</span></span>           |
| <span data-ttu-id="96f75-131">Массив [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)</span><span class="sxs-lookup"><span data-stu-id="96f75-131">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) array</span></span>             | <span data-ttu-id="96f75-132">0x36 0x75</span><span class="sxs-lookup"><span data-stu-id="96f75-132">0x36 0x75</span></span>           |
| <span data-ttu-id="96f75-133">Массив цветов-индексов</span><span class="sxs-lookup"><span data-stu-id="96f75-133">Color-index array</span></span>                            | <span data-ttu-id="96f75-134">0x76 0x275</span><span class="sxs-lookup"><span data-stu-id="96f75-134">0x76 0x275</span></span>          |



 

 

 
