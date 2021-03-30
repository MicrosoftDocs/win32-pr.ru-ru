---
description: Другие исходные объекты
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Другие исходные объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806437"
---
# <a name="other-source-objects"></a><span data-ttu-id="d901c-103">Другие исходные объекты</span><span class="sxs-lookup"><span data-stu-id="d901c-103">Other Source Objects</span></span>

<span data-ttu-id="d901c-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="d901c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d901c-105">В дополнение к источникам видео и аудио, [службы редактирования DirectShow](directshow-editing-services.md) (DES) поддерживают следующие исходные объекты.</span><span class="sxs-lookup"><span data-stu-id="d901c-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="d901c-106">**Изображения по-прежнему**</span><span class="sxs-lookup"><span data-stu-id="d901c-106">**Still Images**</span></span>

<span data-ttu-id="d901c-107">DES поддерживает следующие форматы файлов для изображений по-прежнему:</span><span class="sxs-lookup"><span data-stu-id="d901c-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="d901c-108">Растровое изображение (.bmp)</span><span class="sxs-lookup"><span data-stu-id="d901c-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="d901c-109">GIF (формат обмена изображениями)</span><span class="sxs-lookup"><span data-stu-id="d901c-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="d901c-110">JPEG (совместная группа экспертов)</span><span class="sxs-lookup"><span data-stu-id="d901c-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="d901c-111">Графический адаптер Targa или формат (TGA): режим 2 (несжатый RGB) в 16-разрядном, 24-разрядном или 32-разрядном формате.</span><span class="sxs-lookup"><span data-stu-id="d901c-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="d901c-112">Эти файлы можно использовать как изображения по-прежнему или создавать анимации.</span><span class="sxs-lookup"><span data-stu-id="d901c-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="d901c-113">Для файлов Bitmap, JPEG и Targa, если файл используется как изображение по-прежнему, вызовите метод [**иамтимелинесрк:: сетдефаултфпс**](iamtimelinesrc-setdefaultfps.md) , чтобы установить частоту кадров равным нулю.</span><span class="sxs-lookup"><span data-stu-id="d901c-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="d901c-114">**Последовательности DIB**</span><span class="sxs-lookup"><span data-stu-id="d901c-114">**DIB Sequences**</span></span>

<span data-ttu-id="d901c-115">При наличии последовательности файлов Bitmap, JPEG или Targa механизм визуализации может создать последовательность DIB.</span><span class="sxs-lookup"><span data-stu-id="d901c-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="d901c-116">Чтобы создать последовательность DIB, присвойте файлам числовые последовательные имена, такие как Image001.bmp, Image002.bmp, Image003.bmp и т. д.</span><span class="sxs-lookup"><span data-stu-id="d901c-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="d901c-117">Использовать первый файл в последовательности в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="d901c-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="d901c-118">Задайте частоту кадров для последовательности, вызвав [**иамтимелинесрк:: сетдефаултфпс**](iamtimelinesrc-setdefaultfps.md).</span><span class="sxs-lookup"><span data-stu-id="d901c-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="d901c-119">Модуль подготовки отчетов циклически проходит по изображениям в последовательности с заданной частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="d901c-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="d901c-120">Если последовательность слишком мала для заполнения длительности, учитывая частоту кадров, оставшаяся часть длительности будет сплошным черным.</span><span class="sxs-lookup"><span data-stu-id="d901c-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="d901c-121">Во время отрисовки ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="d901c-121">No error occurs during rendering.</span></span>

<span data-ttu-id="d901c-122">**Источники в формате GIF**</span><span class="sxs-lookup"><span data-stu-id="d901c-122">**GIF Sources**</span></span>

<span data-ttu-id="d901c-123">DES поддерживает источники в формате GIF, включая анимированные и прозрачные GIF, с использованием спецификации GIF89a.</span><span class="sxs-lookup"><span data-stu-id="d901c-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="d901c-124">При использовании анимированного GIF, в отличие от других типов файлов, не нужно задавать частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="d901c-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="d901c-125">В GIF-файле указывается задержка между каждым изображением в анимации.</span><span class="sxs-lookup"><span data-stu-id="d901c-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="d901c-126">Для поддержки прозрачных GIF DES преобразует прозрачные области изображения в RGB Triplet RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d901c-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="d901c-127">Затем можно использовать [ключ перехода](key-transition.md) к ключу в RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d901c-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="d901c-128">DES также преобразует любые черные регионы, попадающие в диапазон RGB (0 – 7, 0 – 7, 0 – 7), в значение RGB (8, 8, 8), за исключением индекса прозрачности, если он попадает в этот диапазон.</span><span class="sxs-lookup"><span data-stu-id="d901c-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="d901c-129">Это преобразование не обнаруживается для глаза.</span><span class="sxs-lookup"><span data-stu-id="d901c-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="d901c-130">**Источник цвета видео**</span><span class="sxs-lookup"><span data-stu-id="d901c-130">**Video Color Source**</span></span>

<span data-ttu-id="d901c-131">[Исходный объект цвета видео](video-color-source.md) создает непрерывное изображение сплошного цвета.</span><span class="sxs-lookup"><span data-stu-id="d901c-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="d901c-132">Один из способов использования этого объекта — сделать его слоем в переходе.</span><span class="sxs-lookup"><span data-stu-id="d901c-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="d901c-133">Например, используйте его в видеоролике или появление.</span><span class="sxs-lookup"><span data-stu-id="d901c-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="d901c-134">**Настраиваемые фильтры источников**</span><span class="sxs-lookup"><span data-stu-id="d901c-134">**Custom Source Filters**</span></span>

<span data-ttu-id="d901c-135">DES может использовать фильтр источника DirectShow в качестве источника временной шкалы, если фильтр удовлетворяет следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="d901c-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="d901c-136">Он поддерживает поиск</span><span class="sxs-lookup"><span data-stu-id="d901c-136">It supports seeking</span></span>
-   <span data-ttu-id="d901c-137">Он создает формат, поддерживаемый DES.</span><span class="sxs-lookup"><span data-stu-id="d901c-137">It produces a format that DES supports.</span></span> <span data-ttu-id="d901c-138">Формат можно сжать, если система пользователя имеет фильтр DirectShow, способный декодировать его.</span><span class="sxs-lookup"><span data-stu-id="d901c-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="d901c-139">Чтобы использовать настраиваемый источник, укажите идентификатор CLSID фильтра в качестве идентификатора GUID подобъекта исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d901c-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="d901c-140">Дополнительные сведения см. в разделе [подобъекты](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="d901c-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="d901c-141">Для поддержки пользовательских свойств реализуйте их как свойства "размещение" **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="d901c-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="d901c-142">В исходных объектах поддерживаются только статические свойства. Динамические свойства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d901c-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d901c-143">См. также</span><span class="sxs-lookup"><span data-stu-id="d901c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d901c-144">Работа с источниками</span><span class="sxs-lookup"><span data-stu-id="d901c-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



