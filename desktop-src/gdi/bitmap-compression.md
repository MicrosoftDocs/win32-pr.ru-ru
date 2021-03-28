---
description: Windows поддерживает форматы для сжатия точечных рисунков, которые определяют их цвета с 8 или 4 битами на пиксель. Сжатие сокращает объем дискового пространства и хранилища памяти, необходимого для точечного рисунка.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Сжатие растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155699"
---
# <a name="bitmap-compression"></a><span data-ttu-id="bca67-104">Сжатие растрового изображения</span><span class="sxs-lookup"><span data-stu-id="bca67-104">Bitmap Compression</span></span>

<span data-ttu-id="bca67-105">Windows поддерживает форматы для сжатия точечных рисунков, которые определяют их цвета с 8 или 4 битами на пиксель.</span><span class="sxs-lookup"><span data-stu-id="bca67-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="bca67-106">Сжатие сокращает объем дискового пространства и хранилища памяти, необходимого для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="bca67-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="bca67-107">Если элементу **Compression** структуры заголовка данных Bitmap является BI \_ RLE8, для сжатия 8-разрядного точечного рисунка используется формат кодирования длины выполнения (RLE).</span><span class="sxs-lookup"><span data-stu-id="bca67-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="bca67-108">Этот формат можно сжать в закодированных или абсолютных режимах.</span><span class="sxs-lookup"><span data-stu-id="bca67-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="bca67-109">Оба режима могут находиться в одном и том же битовом рисунке:</span><span class="sxs-lookup"><span data-stu-id="bca67-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="bca67-110">*Режим кодирования* состоит из двух байтов: первый байт определяет число последовательных пикселей, которое должно быть выведено с использованием индекса цвета, содержащегося во втором байте.</span><span class="sxs-lookup"><span data-stu-id="bca67-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="bca67-111">Кроме того, первый байт пары может быть установлен в ноль, чтобы указать escape-символ, обозначающий конец строки, конец точечного рисунка или разностный текст, в зависимости от значения второго байта.</span><span class="sxs-lookup"><span data-stu-id="bca67-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="bca67-112">Интерпретация escape-последовательности зависит от значения второго байта пары, которое может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bca67-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="bca67-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bca67-113">Value</span></span> | <span data-ttu-id="bca67-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bca67-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca67-115">0</span><span class="sxs-lookup"><span data-stu-id="bca67-115">0</span></span>     | <span data-ttu-id="bca67-116">Конец строки.</span><span class="sxs-lookup"><span data-stu-id="bca67-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="bca67-117">1</span><span class="sxs-lookup"><span data-stu-id="bca67-117">1</span></span>     | <span data-ttu-id="bca67-118">Конец точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="bca67-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="bca67-119">2</span><span class="sxs-lookup"><span data-stu-id="bca67-119">2</span></span>     | <span data-ttu-id="bca67-120">Изменений.</span><span class="sxs-lookup"><span data-stu-id="bca67-120">Delta.</span></span> <span data-ttu-id="bca67-121">2 байта после escape-последовательности содержат значения без знака, указывающие горизонтальное и вертикальное смещение следующего пикселя от текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="bca67-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="bca67-122">В *абсолютном режиме* первый байт равен нулю, а второй байт — значению в диапазоне от 03H до ФФХ.</span><span class="sxs-lookup"><span data-stu-id="bca67-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="bca67-123">Второй байт представляет число следующих байтов, каждое из которых содержит индекс цвета для одного пикселя.</span><span class="sxs-lookup"><span data-stu-id="bca67-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="bca67-124">Если второй байт равен двум или меньшим, то escape-последовательность имеет то же значение, что и закодированный режим.</span><span class="sxs-lookup"><span data-stu-id="bca67-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="bca67-125">В абсолютном режиме каждый запуск должен быть согласован по границе слова.</span><span class="sxs-lookup"><span data-stu-id="bca67-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="bca67-126">В следующем примере показаны шестнадцатеричные значения 8-разрядного сжатого растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="bca67-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="bca67-127">Точечный рисунок разворачивается следующим образом (значения из двух цифр представляют цветовой индекс для одного пикселя):</span><span class="sxs-lookup"><span data-stu-id="bca67-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="bca67-128">Если элемент **Compression** — BI \_ RLE4, точечный рисунок сжимается с использованием формата кодирования длины выполнения для 4-разрядного точечного рисунка, который также использует закодированные и абсолютные режимы.</span><span class="sxs-lookup"><span data-stu-id="bca67-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="bca67-129">В закодированном режиме первый байт пары содержит число пикселей, которые должны быть выведены с использованием цветовых индексов во втором байте.</span><span class="sxs-lookup"><span data-stu-id="bca67-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="bca67-130">Второй байт содержит два цветовых индекса: один — в его старших битах, а второй — в младших старших битах.</span><span class="sxs-lookup"><span data-stu-id="bca67-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="bca67-131">Первая из пикселов рисуется с помощью цвета, заданного старшим размером 4 бита, второй — с помощью цвета в младших 4 битах, третий — с помощью цвета в 4 битах и так далее, пока не будут выведены все пикселы, заданные первым байтом.</span><span class="sxs-lookup"><span data-stu-id="bca67-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="bca67-132">В абсолютном режиме первый байт равен нулю.</span><span class="sxs-lookup"><span data-stu-id="bca67-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="bca67-133">Второй байт содержит количество цветных индексов, которые следуют за.</span><span class="sxs-lookup"><span data-stu-id="bca67-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="bca67-134">Последующие байты содержат индексы цветов в высоком и низком порядке 4 бит, один цветовой индекс для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="bca67-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="bca67-135">В абсолютном режиме каждый запуск должен быть согласован по границе слова.</span><span class="sxs-lookup"><span data-stu-id="bca67-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="bca67-136">Символы конца строки, конца растрового изображения и последовательности изменений, описанные для бизнес-аналитики RLE8, \_ также применяются к \_ сжатию RLE4 BI.</span><span class="sxs-lookup"><span data-stu-id="bca67-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="bca67-137">В следующем примере показаны шестнадцатеричные значения 4-битового сжатого битового рисунка:</span><span class="sxs-lookup"><span data-stu-id="bca67-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="bca67-138">Точечный рисунок разворачивается следующим образом (однозначные значения представляют собой цветовой индекс для одного пикселя):</span><span class="sxs-lookup"><span data-stu-id="bca67-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



