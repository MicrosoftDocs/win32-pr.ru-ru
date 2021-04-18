---
description: Сравнение Top-Down
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down и Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663552"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="d2036-103">Top-Down и Bottom-Up DIB</span><span class="sxs-lookup"><span data-stu-id="d2036-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="d2036-104">Если вы не знакомы с программированием графики, вы можете ожидать, что точечный рисунок будет упорядочен в память, чтобы верхняя строка изображения отображалась в начале буфера, затем Следующая строка и так далее.</span><span class="sxs-lookup"><span data-stu-id="d2036-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="d2036-105">Однако это не всегда так.</span><span class="sxs-lookup"><span data-stu-id="d2036-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="d2036-106">В Windows растровые изображения, независимые от устройства (DIB), могут размещаться в памяти в двух разных ориентациях: снизу вверх и сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="d2036-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="d2036-107">В снимке рисунка снизу вверх буфер изображения начинается с нижней строки пикселей, за которой следует следующая строка вверх и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2036-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="d2036-108">Верхняя строка изображения — это последняя строка в буфере.</span><span class="sxs-lookup"><span data-stu-id="d2036-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="d2036-109">Таким образом, первый байт в памяти является левым нижним пикселем изображения.</span><span class="sxs-lookup"><span data-stu-id="d2036-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="d2036-110">В GDI все изображения сохраняются снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="d2036-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="d2036-111">На следующей диаграмме показана физическая структура рисунка в формате "снизу вверх".</span><span class="sxs-lookup"><span data-stu-id="d2036-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![DIB снизу вверх](images/pixel-layout-bottomup.png)

<span data-ttu-id="d2036-113">В списке DIB в верхнем углу порядок строк изменяется на обратный.</span><span class="sxs-lookup"><span data-stu-id="d2036-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="d2036-114">Верхняя строка изображения — это первая строка в памяти, за которой следует следующая строка.</span><span class="sxs-lookup"><span data-stu-id="d2036-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="d2036-115">Нижняя строка изображения — это последняя строка в буфере.</span><span class="sxs-lookup"><span data-stu-id="d2036-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="d2036-116">При использовании элемента списка DIB («сверху вниз») первый байт в памяти является верхним левым пикселем изображения.</span><span class="sxs-lookup"><span data-stu-id="d2036-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="d2036-117">В DirectDraw используются нисходящие DIB-изображения.</span><span class="sxs-lookup"><span data-stu-id="d2036-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="d2036-118">На следующей диаграмме показана физическая структура элемента списка DIB.</span><span class="sxs-lookup"><span data-stu-id="d2036-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![рисунок сверху вниз](images/pixel-layout-topdown.png)

<span data-ttu-id="d2036-120">Для RGB DIB ориентация изображения определяется элементом **бихеигхт** структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="d2036-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="d2036-121">Если **бихеигхт** положительное, изображение будет снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="d2036-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="d2036-122">Если **бихеигхт** является отрицательным, изображение будет сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="d2036-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="d2036-123">Изображения DIB в форматах YUV всегда находятся сверху вниз, а знак элемента **бихеигхт** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d2036-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="d2036-124">Декодеры должны предлагать форматы YUV с положительным **бихеигхт**, но они также должны принимать форматы YUV с отрицательным **бихеигхт** и игнорировать знак.</span><span class="sxs-lookup"><span data-stu-id="d2036-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="d2036-125">Кроме того, любой тип DIB, использующий **FourCC** в члене **бикомпрессион** , должен выразить свой **бихеигхт** как положительное число независимо от того, что имеет его ориентация, так как объект **FourCC** определяет схему сжатия, ориентация изображения которой должна быть понятна любым совместимым фильтром.</span><span class="sxs-lookup"><span data-stu-id="d2036-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2036-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d2036-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2036-127">Работа с кадрами видео</span><span class="sxs-lookup"><span data-stu-id="d2036-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



