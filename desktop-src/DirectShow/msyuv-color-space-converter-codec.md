---
description: МСЮВ — это модульный кодек YUV-RGB для преобразователя цветового пространства.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Кодек преобразователя цветового пространства МСЮВ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689337"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="57d69-103">Кодек преобразователя цветового пространства МСЮВ</span><span class="sxs-lookup"><span data-stu-id="57d69-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="57d69-104">МСЮВ — это модульный кодек YUV-RGB для преобразователя цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="57d69-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="57d69-105">Он позволяет воспроизводить исходные данные видео в форматах YUV на клиентах, видеоадаптер которых не может использоваться для преобразования YUV в RGB в оборудовании.</span><span class="sxs-lookup"><span data-stu-id="57d69-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="57d69-106">Кодек участвует в графах фильтров с помощью фильтра программы [распаковки AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="57d69-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="57d69-107">Камеры цифровых конференций с 1394 или USB-интерфейсами могут создавать данные изображений в различных форматах YUV.</span><span class="sxs-lookup"><span data-stu-id="57d69-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="57d69-108">Если устройство отображения не поддерживает встроенное преобразование YUV-to-RGB или если не удается использовать функцию аппаратного преобразования по какой-либо другой причине, то перед отправкой в модуль подготовки отчетов необходимо преобразовать данные изображения YUV в формат RGB.</span><span class="sxs-lookup"><span data-stu-id="57d69-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="57d69-109">Из-за требований модуля [подготовки видео](video-renderer-filter.md)к входному типу RGB во время соединения этот фильтр может быть вставлен в поток на диаграмме из модуля подготовки видео во время автоматического построения графа.</span><span class="sxs-lookup"><span data-stu-id="57d69-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="57d69-110">В частности, если построитель Graph обнаруживает формат YUV в типе мультимедиа для выходного ПИН-кода вышестоящего фильтра, построитель Graph вставляет файл AVI, который затем загружает кодек МСЮВ и изначально настраивает его для преобразования в RGB.</span><span class="sxs-lookup"><span data-stu-id="57d69-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="57d69-111">После того, как граф сначала переходит в состояние выполнения или приостановлено, фильтр модуля подготовки отчетов может определить, может ли видеоадаптер видеоизображения выполнить преобразование в оборудование.</span><span class="sxs-lookup"><span data-stu-id="57d69-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="57d69-112">Если это возможно, программа распаковки AVI уведомляется и перенастраивает МСЮВ для взаимодействия в режиме сквозного режима, что приводит к тому, что кодек пропускает преобразование и копирует данные образа YUV непосредственно на поверхность наложения DirectDraw в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="57d69-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="57d69-113">Поскольку модули подготовки видео (VMR-7 и VMR-9) никогда не используют GDI, для них не требуется тип RGB во время соединения, а преобразователь цветового пространства МСЮВ никогда не вставляется перед фильтром VMR в графе.</span><span class="sxs-lookup"><span data-stu-id="57d69-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="57d69-114">МСЮВ преобразует Упакованные форматы YUV в RGB, как показано в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="57d69-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="57d69-115">Форматы входных данных: UYVY, YUY2, ИВЮ</span><span class="sxs-lookup"><span data-stu-id="57d69-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="57d69-116">Форматы вывода: RGB 8, RGB 16, RGB 24, RGB 32</span><span class="sxs-lookup"><span data-stu-id="57d69-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="57d69-117">Кодек преобразователя цветового пространства МСЮВ — это кодек ВКМ (Video Compression Manager).</span><span class="sxs-lookup"><span data-stu-id="57d69-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="57d69-118">Он используется в DirectShow в фильтре [распаковки AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="57d69-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="57d69-119">Для более общего универсального преобразователя используйте [**конвертер для цветов DSP**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="57d69-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57d69-120">Требования</span><span class="sxs-lookup"><span data-stu-id="57d69-120">Requirements</span></span>



| <span data-ttu-id="57d69-121">Требование</span><span class="sxs-lookup"><span data-stu-id="57d69-121">Requirement</span></span> | <span data-ttu-id="57d69-122">Значение</span><span class="sxs-lookup"><span data-stu-id="57d69-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57d69-123">DLL</span><span class="sxs-lookup"><span data-stu-id="57d69-123">DLL</span></span><br/> | <dl> <span data-ttu-id="57d69-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57d69-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57d69-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57d69-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d69-126">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="57d69-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
