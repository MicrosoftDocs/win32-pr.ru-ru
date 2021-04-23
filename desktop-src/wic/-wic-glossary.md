---
description: Определяет термины, используемые в WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Глоссарий по компонентам работы с образами Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693252"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="a0610-103">Глоссарий по компонентам работы с образами Windows</span><span class="sxs-lookup"><span data-stu-id="a0610-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="a0610-104">B</span><span class="sxs-lookup"><span data-stu-id="a0610-104">B</span></span>

<dl> <dt>

<span data-ttu-id="a0610-105">**Битовая глубина**</span><span class="sxs-lookup"><span data-stu-id="a0610-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-106">Число значений цвета, которые могут быть назначены одному пикселю в изображении.</span><span class="sxs-lookup"><span data-stu-id="a0610-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="a0610-107">Глубина цвета может находиться в диапазоне от 1 бита (черный и белый) до 32 бит (более 16 700 000 цветов).</span><span class="sxs-lookup"><span data-stu-id="a0610-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="a0610-108">См. также: глубина цвета</span><span class="sxs-lookup"><span data-stu-id="a0610-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="a0610-109">**бит на пиксель (в бит)**</span><span class="sxs-lookup"><span data-stu-id="a0610-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-110">Число битов, представляющих значение цвета каждого пикселя в цифровом изображении.</span><span class="sxs-lookup"><span data-stu-id="a0610-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="a0610-111">См. также: бит на ПКС</span><span class="sxs-lookup"><span data-stu-id="a0610-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="a0610-112">C</span><span class="sxs-lookup"><span data-stu-id="a0610-112">C</span></span>

<dl> <dt>

<span data-ttu-id="a0610-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="a0610-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-114">Объект Ивикбитмапклиппер.</span><span class="sxs-lookup"><span data-stu-id="a0610-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-115">**равн**</span><span class="sxs-lookup"><span data-stu-id="a0610-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-116">Фильтр, который сжимает (кодирует) или распаковывает (декодирует) поток данных.</span><span class="sxs-lookup"><span data-stu-id="a0610-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-117">**контекст цвета**</span><span class="sxs-lookup"><span data-stu-id="a0610-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-118">Абстракция для цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="a0610-118">An abstraction for a color profile.</span></span> <span data-ttu-id="a0610-119">Профиль можно загрузить из файла (IE). "цветовой пространство sRGB. ICM") или из буфера памяти, полученного при чтении.</span><span class="sxs-lookup"><span data-stu-id="a0610-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="a0610-120">Сведения о контексте цвета определяются интерфейсом Ивикколорконтекст для WIC и извлекаются с помощью метода Жетколорконтекст.</span><span class="sxs-lookup"><span data-stu-id="a0610-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-121">**Преобразование цветов**</span><span class="sxs-lookup"><span data-stu-id="a0610-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-122">Сопоставление цветов из контекста исходного цвета с контекстом целевого цвета в заданном выходном формате пикселей.</span><span class="sxs-lookup"><span data-stu-id="a0610-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-123">**Цветовая модель ЦИМК**</span><span class="sxs-lookup"><span data-stu-id="a0610-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-124">Многомерное цветовое пространство, состоящее из голубого, пурпурного, желтого и черного интенситиес, составляющих заданный цвет.</span><span class="sxs-lookup"><span data-stu-id="a0610-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="a0610-125">D</span><span class="sxs-lookup"><span data-stu-id="a0610-125">D</span></span>

<dl> <dt>

<span data-ttu-id="a0610-126">**показан**</span><span class="sxs-lookup"><span data-stu-id="a0610-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-127">См. другой термин: кодек</span><span class="sxs-lookup"><span data-stu-id="a0610-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="a0610-128">E</span><span class="sxs-lookup"><span data-stu-id="a0610-128">E</span></span>

<dl> <dt>

<span data-ttu-id="a0610-129">**кодировщик**</span><span class="sxs-lookup"><span data-stu-id="a0610-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-130">См. другой термин: кодек</span><span class="sxs-lookup"><span data-stu-id="a0610-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="a0610-131">L</span><span class="sxs-lookup"><span data-stu-id="a0610-131">L</span></span>

<dl> <dt>

<span data-ttu-id="a0610-132">**качества**</span><span class="sxs-lookup"><span data-stu-id="a0610-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-133">Тип сжатия, который гарантирует, что исходные данные могут быть восстановлены точно, без потери качества изображения.</span><span class="sxs-lookup"><span data-stu-id="a0610-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-134">**потерь**</span><span class="sxs-lookup"><span data-stu-id="a0610-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-135">Процесс сжатия данных, в котором изменяются ненужные сведения, удаляется и не может быть восстановлен после распаковки.</span><span class="sxs-lookup"><span data-stu-id="a0610-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="a0610-136">Обычно используется с звуковыми и визуальными данными, в которых приемлемое ухудшение качества допустимо.</span><span class="sxs-lookup"><span data-stu-id="a0610-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="a0610-137">M</span><span class="sxs-lookup"><span data-stu-id="a0610-137">M</span></span>

<dl> <dt>

<span data-ttu-id="a0610-138">**многопоточный апартамент (MTA)**</span><span class="sxs-lookup"><span data-stu-id="a0610-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-139">Форма многопоточности, поддерживаемая объектной моделью Component (COM).</span><span class="sxs-lookup"><span data-stu-id="a0610-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="a0610-140">В многопоточной модели апартамента все потоки в процессе, которые были инициализированы как свободные, находятся в одном апартаменте.</span><span class="sxs-lookup"><span data-stu-id="a0610-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="a0610-141">Нет</span><span class="sxs-lookup"><span data-stu-id="a0610-141">N</span></span>

<dl> <dt>

<span data-ttu-id="a0610-142">**собственный формат пикселей**</span><span class="sxs-lookup"><span data-stu-id="a0610-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-143">Один из форматов пикселей, предоставляемых WIC, где описывается макет памяти каждого пикселя в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="a0610-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="a0610-144">С</span><span class="sxs-lookup"><span data-stu-id="a0610-144">P</span></span>

<dl> <dt>

<span data-ttu-id="a0610-145">**задания**</span><span class="sxs-lookup"><span data-stu-id="a0610-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-146">Набор цветов, используемых объектом или приложением.</span><span class="sxs-lookup"><span data-stu-id="a0610-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-147">**Политика метаданных фотографий**</span><span class="sxs-lookup"><span data-stu-id="a0610-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-148">Политика Windows для чтения, записи и удаления метаданных образа.</span><span class="sxs-lookup"><span data-stu-id="a0610-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-149">**формат пикселей**</span><span class="sxs-lookup"><span data-stu-id="a0610-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-150">Размер и расположение компонентов цвета пикселя в памяти.</span><span class="sxs-lookup"><span data-stu-id="a0610-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="a0610-151">Он определяется общим числом бит, используемых на пиксель, и числом битов, используемых для хранения компонентов цвета: красный, зеленый, синий и альфа.</span><span class="sxs-lookup"><span data-stu-id="a0610-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="a0610-152">Например, формат пикселей RGB24 использует 24 бита для хранения цвета пикселя, с восемью битами на красный, зеленый и синий.</span><span class="sxs-lookup"><span data-stu-id="a0610-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="a0610-153">Формат пикселей ARGB32 использует 32 бит, где 24 бита информации о цвете и 8 бит информации о альфа-канале.</span><span class="sxs-lookup"><span data-stu-id="a0610-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="a0610-154">**прогрессивное декодирование**</span><span class="sxs-lookup"><span data-stu-id="a0610-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-155">Процесс декодирования изображений, которые были закодированы со сведениями о различных уровнях декодирования.</span><span class="sxs-lookup"><span data-stu-id="a0610-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="a0610-156">S</span><span class="sxs-lookup"><span data-stu-id="a0610-156">S</span></span>

<dl> <dt>

<span data-ttu-id="a0610-157">**вышестоящий**</span><span class="sxs-lookup"><span data-stu-id="a0610-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-158">Ссылается на интерфейс IStream COM, который можно использовать для последовательного чтения или записи данных в файлах, памяти или сетевых расположениях.</span><span class="sxs-lookup"><span data-stu-id="a0610-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="a0610-159">T</span><span class="sxs-lookup"><span data-stu-id="a0610-159">T</span></span>

<dl> <dt>

<span data-ttu-id="a0610-160">**кривая тона**</span><span class="sxs-lookup"><span data-stu-id="a0610-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-161">Граф, используемый в цифровой фотографии, который отображает тональный диапазон изображения.</span><span class="sxs-lookup"><span data-stu-id="a0610-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="a0610-162">W</span><span class="sxs-lookup"><span data-stu-id="a0610-162">W</span></span>

<dl> <dt>

<span data-ttu-id="a0610-163">**Компонент обработки изображений Windows (WIC)**</span><span class="sxs-lookup"><span data-stu-id="a0610-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="a0610-164">Расширяемая платформа, предоставляющая низкоуровневые API для цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="a0610-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



