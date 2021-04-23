---
description: Собственный кодек XR JPEG доступен через компонент Windows Imaging Component (WIC). Формат JPEG XR, который поддерживает кодек, предназначен для бытовой цифровой фотографии.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Общие сведения о коде XR JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702783"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="cc1b7-104">Общие сведения о коде XR JPEG</span><span class="sxs-lookup"><span data-stu-id="cc1b7-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="cc1b7-105">Собственный кодек XR JPEG доступен через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="cc1b7-106">Формат JPEG XR, который поддерживает кодек, предназначен для бытовой цифровой фотографии.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="cc1b7-107">Формат JPEG XR может добиться удвоенной эффективности сжатия исходного формата JPEG с менее заметными артефактами сжатия.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="cc1b7-108">К функциям JPEG XR относятся:</span><span class="sxs-lookup"><span data-stu-id="cc1b7-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="cc1b7-109">Поддержка монохромных изображений, RGB, CMYK и n-канального изображения</span><span class="sxs-lookup"><span data-stu-id="cc1b7-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="cc1b7-110">8-, 16-и 32-разрядные форматы целых чисел</span><span class="sxs-lookup"><span data-stu-id="cc1b7-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="cc1b7-111">Высокий динамический диапазон, форматы с широкими охватами, использующие значения цвета с фиксированной точкой или с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="cc1b7-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="cc1b7-112">Прогрессивное декодирование</span><span class="sxs-lookup"><span data-stu-id="cc1b7-112">Progressive decoding</span></span>
-   <span data-ttu-id="cc1b7-113">Шифрование с потерей или без потерь с использованием того же алгоритма сжатия</span><span class="sxs-lookup"><span data-stu-id="cc1b7-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="cc1b7-114">Поддержка декодирования интересующих регионов в больших изображениях</span><span class="sxs-lookup"><span data-stu-id="cc1b7-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="cc1b7-115">Формат JPEG XR определяется в следующих документах стандартов:</span><span class="sxs-lookup"><span data-stu-id="cc1b7-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="cc1b7-116">ITU-T T. 832: *информационная технология — JPEG XR Image система кодирования — спецификация кодирования изображения*</span><span class="sxs-lookup"><span data-stu-id="cc1b7-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="cc1b7-117">ISO/IEC 29199-2:2010: *информационные технологии — система кодирования изображений JPEG XR — часть 2. Спецификация кодирования изображения*</span><span class="sxs-lookup"><span data-stu-id="cc1b7-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="cc1b7-118">Стандарт JPEG XR Standard в основном основан на [фотографическом формате HD](hdphoto-format-overview.md) , но существуют некоторые различия между двумя форматами.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="cc1b7-119">В Windows 8 кодек HD Photo был обновлен для поддержки JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="cc1b7-120">Теперь кодировщик всегда выводит двоичный поток, соответствующий XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="cc1b7-121">Декодер может декодировать изображения JPEG XR и HD Photo.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="cc1b7-122">В кодеке XR JPEG были внесены существенные улучшения производительности по отношению к графическому кодеку HD.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="cc1b7-123">Например, улучшено декодирование изображений с подразрешением, например создание эскизов, а также декодирование изображений с низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="cc1b7-124">Рекомендуется использовать формат JPEG XR вместо формата фотографии HD.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="cc1b7-125">Сведения о кодека</span><span class="sxs-lookup"><span data-stu-id="cc1b7-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-126">Расширение имени файла</span><span class="sxs-lookup"><span data-stu-id="cc1b7-126">File name extension</span></span> | <span data-ttu-id="cc1b7-127">"жкср" и "формате WDP"</span><span class="sxs-lookup"><span data-stu-id="cc1b7-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="cc1b7-128">Идентификатор GUID контейнера</span><span class="sxs-lookup"><span data-stu-id="cc1b7-128">Container GUID</span></span>      | <span data-ttu-id="cc1b7-129">**GUID \_ контаинерформатвмп**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="cc1b7-130">GUID декодера</span><span class="sxs-lookup"><span data-stu-id="cc1b7-130">Decoder GUID</span></span>        | <span data-ttu-id="cc1b7-131">**\_ВИКВМПДЕКОДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="cc1b7-132">GUID кодировщика</span><span class="sxs-lookup"><span data-stu-id="cc1b7-132">Encoder GUID</span></span>        | <span data-ttu-id="cc1b7-133">**\_ВИКВМПЕНКОДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="cc1b7-134">Поддержка профилей</span><span class="sxs-lookup"><span data-stu-id="cc1b7-134">Profile Support</span></span>     | <span data-ttu-id="cc1b7-135">Кодировщик и декодер поддерживают до основного профиля и до уровня 128.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="cc1b7-136">Функции кодеков</span><span class="sxs-lookup"><span data-stu-id="cc1b7-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="cc1b7-137">Высокий динамический диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-137">High Dynamic Range</span></span>

<span data-ttu-id="cc1b7-138">JPEG XR поддерживает высокодинамические изображения диапазонов с плавающей запятой или цвета с фиксированной точкой.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="cc1b7-139">В этих цветовых форматах числовой диапазон пикселей больше видимого диапазона, поэтому можно настроить цвета выше или ниже видимого диапазона на промежуточных этапах обработки.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="cc1b7-140">Фиксированная точка: в представлении с фиксированной запятой 0 представляет черный, а 1,0 — максимальную насыщенность.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="cc1b7-141">Кодек JPEG XR поддерживает 16-разрядные и 32-разрядные форматы с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="cc1b7-142">Для 16-разрядной версии 1,0 = 0x2000h, которая предоставляет 13 бит для видимого диапазона \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="cc1b7-143">Общий диапазон составляет от – 4,0 до + 3,999 и сопоставляется линейно.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="cc1b7-144">Для 32-bit, 1,0 = 0x01000000h видимым диапазоном является 24 бита, а общий диапазон — от – 128 до + 127,999.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="cc1b7-145">С плавающей запятой: в представлении с плавающей запятой 0 представляет черный, а 1,0 — максимальную насыщенность.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="cc1b7-146">Кодек JPEG XR поддерживает 16-разрядные и 32-разрядные форматы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="cc1b7-147">Плитки</span><span class="sxs-lookup"><span data-stu-id="cc1b7-147">Tiles</span></span>

<span data-ttu-id="cc1b7-148">Фрейм можно секционировать на прямоугольные подобласти, называемые *плитками*.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="cc1b7-149">Плитка — это область изображения, содержащая прямоугольные массивы макроблоккс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="cc1b7-150">Плитки позволяют декодировать регионы изображения без обработки всего изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="cc1b7-151">Во время кодирования выберите число плиток, задав свойства **хоризонталтилеслицес** и **вертикалтилеслицес** .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="cc1b7-152">Минимальный размер плитки — 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="cc1b7-153">Кодировщик корректирует количество плиток, чтобы поддерживать это ограничение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="cc1b7-154">Существует дополнительная нагрузка на хранилище и обработку, связанная с каждой плиткой, поэтому следует учитывать количество плиток, необходимых для конкретных сценариев.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="cc1b7-155">Выходные данные потока изображений</span><span class="sxs-lookup"><span data-stu-id="cc1b7-155">Image Stream Output</span></span>

<span data-ttu-id="cc1b7-156">Стандарт JPEG-XR определяет две части файла JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="cc1b7-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="cc1b7-157">Поток битов образа, определенный в тексте стандарта.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="cc1b7-158">Контейнер изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-158">The image container.</span></span> <span data-ttu-id="cc1b7-159">Файл содержит метаданные EXIF и XMP и определяется в приложении A из стандарта.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="cc1b7-160">Можно и в стандартном случае внедрять поток изображения в контейнер файлов другого типа.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="cc1b7-161">Кодировщик поддерживает режим только потоковой передачи, который выводит поток битов необработанного изображения без контейнера изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="cc1b7-162">Приложение может хранить битовый поток в каком бы то ни было другом формате контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="cc1b7-163">Чтобы включить режим «только потоковая передача», установите свойство **стреамонли** .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="cc1b7-164">Параметры качества изображения</span><span class="sxs-lookup"><span data-stu-id="cc1b7-164">Image Quality Settings</span></span>

<span data-ttu-id="cc1b7-165">Несколько свойств кодека управляют качеством выходного изображения из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="cc1b7-166">[Имажекуалити](#imagequality) — это свойство, которое является общим для кодеков WIC.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="cc1b7-167">Он задает качество изображения как одно значение с плавающей запятой от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="cc1b7-168">Свойства [Quality](#image-quality-settings), [перекрытия](#overlap)и [подвыборки](#subsampling) обеспечивают больший контроль над параметрами качества.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="cc1b7-169">Чтобы использовать свойства " [качество](#image-quality-settings)", " [Перекрытие](#overlap)" и " [подвыборка](#subsampling) ", задайте для свойства [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="cc1b7-170">Если [усекодекоптионс](#usecodecoptions) имеет значение **Variant \_ false** (по умолчанию используется **вариант \_ false** ), кодировщик использует свойство [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="cc1b7-171">Кодировщик сопоставляет значение Имажекуалити с [качеством](#image-quality-settings), [перекрытием](#overlap)и [подвыборкой](#subsampling) с помощью таблицы подстановки.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="cc1b7-172">Кодировщик не поддерживает свойство **компрессионкуалити** .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="cc1b7-173">Сжатый перекодированный домен</span><span class="sxs-lookup"><span data-stu-id="cc1b7-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="cc1b7-174">Кодек JPEG XR может выполнять определенные преобразования изображений без фактического декодирования сжатых данных и их повторной кодировки.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="cc1b7-175">Операции со сжатыми доменами очень эффективны и позволяют избежать дополнительной потери качества, типичной при расшифровке и повторном кодировании сжатого с потерей изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="cc1b7-176">Поддерживаются следующие операции со сжатыми доменами:</span><span class="sxs-lookup"><span data-stu-id="cc1b7-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="cc1b7-177">Обрезать область изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="cc1b7-178">Поворот или отражение изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="cc1b7-179">Отбросить данные частоты, чтобы создать файл изображения меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="cc1b7-180">Реорганизовать изображение между пространственным и частотным порядком.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="cc1b7-181">Кодировщик XR JPEG использует сжатое перекодирование домена, если это возможно, если исходный образ является JPEG-изображением XR.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="cc1b7-182">Когда кодировщик выполняет операцию со сжатым доменом, он игнорирует следующие свойства кодека: [алфакуалити](#alphaquality), [имажекуалити](#imagequality), [интерлеаведалфа](#interleavedalpha), [](#lossless)[Перекрытие](#overlap)без потери [качества](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="cc1b7-183">Если свойства [хоризонталтилеслицес](/windows) и [вертикалтилеслицес](/windows) существуют, их необходимо присвоить нулю.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="cc1b7-184">Нельзя изменить размер плитки изображения в составе сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="cc1b7-185">В приведенном ниже списке описывается выполнение преобразований изображений.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="cc1b7-186">Чтобы обрезать изображение, задайте нужный регион в параметре [**викрект**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) метода **вритесаурце** .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="cc1b7-187">Чтобы повернуть или перевернуть изображение, установите свойство [битмаптрансформ](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="cc1b7-188">Чтобы отменить данные частоты в изображении, установите свойство [имажедатадискард](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="cc1b7-189">Чтобы отбросить данные частоты в альфа-канале, установите свойство [алфадатадискард](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="cc1b7-190">При отклонении данных частоты уменьшается размер закодированного файла и может снизиться разрешение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="cc1b7-191">Чтобы изменить организацию изображения между частотой и пространственной сортировкой, задайте свойство [фрекуенциордеринг](/windows) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="cc1b7-192">Чтобы отключить сжатый перекодировку домена и заставить кодировщик повторно закодировать образ, присвойте параметру [усекодекоптионс](#usecodecoptions) **значение Variant \_ true** и присвойте параметру [компресседдомаинтранскоде](#compresseddomaintranscode) значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="cc1b7-193">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="cc1b7-193">Encoder Options</span></span>

<span data-ttu-id="cc1b7-194">Чтобы задать свойства кодировки, используйте интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="cc1b7-195">Дополнительные сведения см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="cc1b7-196">В следующем списке указаны параметры кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="cc1b7-197">алфадатадискард</span><span class="sxs-lookup"><span data-stu-id="cc1b7-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="cc1b7-198">алфакуалити</span><span class="sxs-lookup"><span data-stu-id="cc1b7-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="cc1b7-199">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="cc1b7-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="cc1b7-200">компресседдомаинтранскоде</span><span class="sxs-lookup"><span data-stu-id="cc1b7-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="cc1b7-201">фрекуенциордер</span><span class="sxs-lookup"><span data-stu-id="cc1b7-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="cc1b7-202">хоризонталтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cc1b7-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="cc1b7-203">игнореоверлап</span><span class="sxs-lookup"><span data-stu-id="cc1b7-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="cc1b7-204">имажедатадискард</span><span class="sxs-lookup"><span data-stu-id="cc1b7-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="cc1b7-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="cc1b7-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="cc1b7-206">интерлеаведалфа</span><span class="sxs-lookup"><span data-stu-id="cc1b7-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="cc1b7-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="cc1b7-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="cc1b7-208">Перекрытие</span><span class="sxs-lookup"><span data-stu-id="cc1b7-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="cc1b7-209">прогрессивемоде</span><span class="sxs-lookup"><span data-stu-id="cc1b7-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="cc1b7-210">Качество</span><span class="sxs-lookup"><span data-stu-id="cc1b7-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="cc1b7-211">стреамонли</span><span class="sxs-lookup"><span data-stu-id="cc1b7-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="cc1b7-212">Подвыборка</span><span class="sxs-lookup"><span data-stu-id="cc1b7-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="cc1b7-213">усекодекоптионс</span><span class="sxs-lookup"><span data-stu-id="cc1b7-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="cc1b7-214">вертикалтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cc1b7-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="cc1b7-215">алфадатадискард</span><span class="sxs-lookup"><span data-stu-id="cc1b7-215">AlphaDataDiscard</span></span>

<span data-ttu-id="cc1b7-216">Задает объем данных альфа-частоты, которые должны быть удалены во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="cc1b7-217">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-217">Data type</span></span> | <span data-ttu-id="cc1b7-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-218">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-219">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-219">Range</span></span> | <span data-ttu-id="cc1b7-220">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cc1b7-221">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-221">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-222">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-222">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-223">0 – 4</span><span class="sxs-lookup"><span data-stu-id="cc1b7-223">0–4</span></span>   | <span data-ttu-id="cc1b7-224">Нет</span><span class="sxs-lookup"><span data-stu-id="cc1b7-224">None</span></span>    |



 

<span data-ttu-id="cc1b7-225">Это свойство применяется, только если свойство [компресседдомаинтранскоде](#compresseddomaintranscode) имеет значение **Variant \_ true** , а изображение содержит плоский альфа-канал или альфа-канал с чередованием; в противном случае он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="cc1b7-226">Для изображений, содержащих плоский альфа-канал, допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="cc1b7-227">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-227">Value</span></span> | <span data-ttu-id="cc1b7-228">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-229">0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-229">0</span></span>     | <span data-ttu-id="cc1b7-230">Данные частоты изображения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cc1b7-231">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-231">1</span></span>     | <span data-ttu-id="cc1b7-232">Флексбитс отклоняется.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-232">The flexbits are discarded.</span></span> <span data-ttu-id="cc1b7-233">Это произвольно сокращает качество плоского альфа-канала для перекодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="cc1b7-234">, без изменения эффективного разрешения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="cc1b7-235">Точное уменьшение размера и качества файла зависит от множества факторов и не может быть точно указано.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="cc1b7-236">2</span><span class="sxs-lookup"><span data-stu-id="cc1b7-236">2</span></span>     | <span data-ttu-id="cc1b7-237">Полоса данных высокой тактовой частоты отбрасывается, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="cc1b7-238">Это эффективно сокращает разрешение плоского альфа-канала на коэффициент 4 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="cc1b7-239">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждом блоке 4x4 пикселей альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="cc1b7-240">Как правило, это значение следует задавать, только если свойство [имажедатадискард](#imagedatadiscard) имеет то же значение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="cc1b7-241">3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-241">3</span></span>     | <span data-ttu-id="cc1b7-242">Полосы данных с высокой и низкой тактовой частотой отбрасываются, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="cc1b7-243">Это ффективели уменьшает разрешение плоского альфа-канала на коэффициент 16 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="cc1b7-244">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждой 16x16 макроблокк пикселов альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="cc1b7-245">Как правило, это значение следует задавать, только если свойство [имажедатадискард](#imagedatadiscard) имеет то же значение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="cc1b7-246">4</span><span class="sxs-lookup"><span data-stu-id="cc1b7-246">4</span></span>     | <span data-ttu-id="cc1b7-247">Полностью удаляется альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="cc1b7-248">Формат пикселей перекодированного изображения изменяется в соответствии с удалением альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="cc1b7-249">Для образов, содержащих альфа-канал с чередованием, допустимо следующее значение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="cc1b7-250">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-250">Value</span></span> | <span data-ttu-id="cc1b7-251">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-252">4</span><span class="sxs-lookup"><span data-stu-id="cc1b7-252">4</span></span>     | <span data-ttu-id="cc1b7-253">Полностью удаляется альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="cc1b7-254">Формат пикселей перекодированного изображения изменяется в соответствии с удалением альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="cc1b7-255">Для Alpha с чередованием, если это свойство не имеет значение 4, альфа-канал обрабатывается так же, как данные изображения, в соответствии со значением свойства [имажедатадискард](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="cc1b7-256">алфакуалити</span><span class="sxs-lookup"><span data-stu-id="cc1b7-256">AlphaQuality</span></span>

<span data-ttu-id="cc1b7-257">Задает качество сжатия для изображения плоского альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="cc1b7-258">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-258">Data type</span></span> | <span data-ttu-id="cc1b7-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-259">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-260">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-260">Range</span></span> | <span data-ttu-id="cc1b7-261">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cc1b7-262">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-262">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-263">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-263">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-264">1 – 255</span><span class="sxs-lookup"><span data-stu-id="cc1b7-264">1–255</span></span> | <span data-ttu-id="cc1b7-265">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-265">1</span></span>       |



 

<span data-ttu-id="cc1b7-266">Это свойство применяется, если изображение имеет альфа-канал, а свойство [интерлеаведалфа](#interleavedalpha) имеет значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="cc1b7-267">Значение 1 означает режим без потерь.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="cc1b7-268">Увеличение значений приводит к увеличению коэффициента сжатия и более низкому качеству изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="cc1b7-269">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="cc1b7-269">BitmapTransform</span></span>

<span data-ttu-id="cc1b7-270">Указывает, будет ли изображение повернуто или отражено при декодировании.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="cc1b7-271">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-271">Data type</span></span> | <span data-ttu-id="cc1b7-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-272">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-273">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-273">Range</span></span>                                                                     | <span data-ttu-id="cc1b7-274">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="cc1b7-275">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-275">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-276">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-276">**VT\_UI1**</span></span> | [<span data-ttu-id="cc1b7-277">**викбитмаптрансформоптионс**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="cc1b7-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="cc1b7-279">компресседдомаинтранскоде</span><span class="sxs-lookup"><span data-stu-id="cc1b7-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="cc1b7-280">Включает или отключает перекодирование сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="cc1b7-281">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-281">Data type</span></span>         | <span data-ttu-id="cc1b7-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-282">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-283">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="cc1b7-284">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-285">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-285">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-286">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="cc1b7-287">Чтобы отключить сжатые операции домена, задайте для этого свойства значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="cc1b7-288">фрекуенциордер</span><span class="sxs-lookup"><span data-stu-id="cc1b7-288">FrequencyOrder</span></span>

<span data-ttu-id="cc1b7-289">Включает кодирование в порядке частот.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="cc1b7-290">Реализации устройств кодировщиков JPEG XR могут организовывать файл в пространственном порядке, чтобы уменьшить объем памяти, необходимый для кодирования.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="cc1b7-291">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-291">Data type</span></span>         | <span data-ttu-id="cc1b7-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-292">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-293">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="cc1b7-294">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-295">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-295">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-296">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="cc1b7-297">**Вариант \_ TRUE**: порядок частот.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="cc1b7-298">Данные с наименьшей частотой отображаются в файле первыми, а содержимое изображения группируются по частоте, а не к пространственной ориентации.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="cc1b7-299">Упорядочение файла по частоте обеспечивает лучшую производительность при декодировании на основе частоты.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="cc1b7-300">**Вариант \_ FALSE**: пространственный порядок.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="cc1b7-301">Пространственный порядок сокращает объем памяти, необходимый для кодирования</span><span class="sxs-lookup"><span data-stu-id="cc1b7-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="cc1b7-302">Рекомендуется использовать частотный порядок, если нет причин, связанных с производительностью или конкретными приложениями, для использования пространственного порядка.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="cc1b7-303">хоризонталтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cc1b7-303">HorizontalTileSlices</span></span>

<span data-ttu-id="cc1b7-304">Задает количество горизонтальных плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="cc1b7-305">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-305">Data type</span></span>  | <span data-ttu-id="cc1b7-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-306">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-307">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-307">Range</span></span>  | <span data-ttu-id="cc1b7-308">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="cc1b7-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-309">**USHORT**</span></span> | <span data-ttu-id="cc1b7-310">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-310">**VT\_UI2**</span></span> | <span data-ttu-id="cc1b7-311">0 — 4095</span><span class="sxs-lookup"><span data-stu-id="cc1b7-311">0–4095</span></span> | <span data-ttu-id="cc1b7-312">(ширина изображения — 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="cc1b7-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="cc1b7-313">Значение — это число горизонтальных делений; то есть числом горизонтальных плиток — 1.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="cc1b7-314">игнореоверлап</span><span class="sxs-lookup"><span data-stu-id="cc1b7-314">IgnoreOverlap</span></span>

<span data-ttu-id="cc1b7-315">Указывает, как кодировщик обрабатывает границы плиток во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="cc1b7-316">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-316">Data type</span></span>         | <span data-ttu-id="cc1b7-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-317">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-318">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cc1b7-319">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-320">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-320">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-321">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="cc1b7-322">Это свойство применяется только в том случае, если для свойства [компресседдомаинтранскоде](#compresseddomaintranscode) задано значение **Variant \_ true** , а в подобласти выполняется перекодировка только одной или нескольких плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="cc1b7-323">Операция по умолчанию для перекодировки региона заключается в том, чтобы расширить запрошенную область, включив в нее окружающие Пиксели, необходимые для перекрытия границ области.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="cc1b7-324">Если для этого свойства задано значение **Variant \_ true**, кодек игнорирует окружающие пикселы и извлекаются только выбранные плитка или плитки.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="cc1b7-325">Если исходное изображение не является мозаичным или если запрошенная область содержит частичные плитки, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="cc1b7-326">имажедатадискард</span><span class="sxs-lookup"><span data-stu-id="cc1b7-326">ImageDataDiscard</span></span>

<span data-ttu-id="cc1b7-327">Задает объем данных частоты образа, которые должны быть удалены во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="cc1b7-328">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-328">Data type</span></span> | <span data-ttu-id="cc1b7-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-329">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-330">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-330">Range</span></span> | <span data-ttu-id="cc1b7-331">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cc1b7-332">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-332">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-333">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-333">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-334">0 – 3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-334">0–3</span></span>   | <span data-ttu-id="cc1b7-335">0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-335">0</span></span>       |



 

<span data-ttu-id="cc1b7-336">Это свойство применяется только в том случае, если свойство [компресседдомаинтранскоде](#compresseddomaintranscode) имеет значение **Variant \_ true**; в противном случае оно игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="cc1b7-337">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-337">Value</span></span> | <span data-ttu-id="cc1b7-338">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-339">0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-339">0</span></span>     | <span data-ttu-id="cc1b7-340">Данные частоты изображения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cc1b7-341">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-341">1</span></span>     | <span data-ttu-id="cc1b7-342">Флексбитс отклоняется.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-342">The flexbits are discarded.</span></span> <span data-ttu-id="cc1b7-343">Это произвольно сокращает качество перекодированного изображения без изменения эффективного разрешения изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="cc1b7-344">Точное уменьшение размера и качества файла зависит от множества факторов и не может быть точно указано.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="cc1b7-345">Это значение возвращает ошибку, указанную для альфа-канала с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="cc1b7-346">2</span><span class="sxs-lookup"><span data-stu-id="cc1b7-346">2</span></span>     | <span data-ttu-id="cc1b7-347">Полоса данных высокой тактовой частоты отбрасывается, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="cc1b7-348">Это уменьшает разрешение перекодированного изображения с помощью коэффициента 4 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="cc1b7-349">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждом блоке 4x4 пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="cc1b7-350">Таким образом, перекодированный образ должен быть downsampled соответствующим образом при его декодировании.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="cc1b7-351">3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-351">3</span></span>     | <span data-ttu-id="cc1b7-352">Полосы данных с высокой и низкой тактовой частотой отбрасываются, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="cc1b7-353">Это уменьшает разрешение перекодированного изображения с помощью коэффициента 16 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="cc1b7-354">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждой 16x16 макроблокк пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="cc1b7-355">Таким образом, перекодированный образ должен быть downsampled соответствующим образом при его декодировании.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="cc1b7-356">Если изображение содержит альфа-канал с чередованием, значение [имажедатадискард](#imagedatadiscard) применяется к альфа-каналу, если только свойство [алфадатадискард](#alphadatadiscard) не имеет значение 4. в этом случае альфа-канал отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="cc1b7-357">Для плоского альфа-канала данные частоты, которые отбрасываются, управляются свойством [алфадатадискард](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="cc1b7-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="cc1b7-358">ImageQuality</span></span>

<span data-ttu-id="cc1b7-359">Задает качество изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-359">Sets the image quality.</span></span>



| <span data-ttu-id="cc1b7-360">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-360">Data type</span></span> | <span data-ttu-id="cc1b7-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-361">VARTYPE</span></span>    | <span data-ttu-id="cc1b7-362">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-362">Range</span></span> | <span data-ttu-id="cc1b7-363">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="cc1b7-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-364">**FLOAT**</span></span> | <span data-ttu-id="cc1b7-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-365">**VT\_R4**</span></span> | <span data-ttu-id="cc1b7-366">от 0 до 1,0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-366">0–1.0</span></span> | <span data-ttu-id="cc1b7-367">0,9</span><span class="sxs-lookup"><span data-stu-id="cc1b7-367">0.9</span></span>     |



 

<span data-ttu-id="cc1b7-368">Уровень 1,0 обеспечивает сжатие с математическим коэффициентом потери данных.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="cc1b7-369">Уровень 0,0 является самым низким значением качества.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="cc1b7-370">интерлеаведалфа</span><span class="sxs-lookup"><span data-stu-id="cc1b7-370">InterleavedAlpha</span></span>

<span data-ttu-id="cc1b7-371">Указывает, кодировать альфа-или плоскую альфа-канал с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="cc1b7-372">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-372">Data type</span></span>         | <span data-ttu-id="cc1b7-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-373">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-374">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cc1b7-375">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-376">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-376">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-377">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="cc1b7-378">**Вариант \_ TRUE**: альфа-канал с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="cc1b7-379">Сведения о альфа-канале кодируются как дополнительный канал с чередованием, без корреляции с каналами содержимого изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="cc1b7-380">Этот режим удобен для декодирования альфа-канала одновременно с изображением при потоковой передаче изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="cc1b7-381">ВАРИАНТ \_ false: плоский альфа.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="cc1b7-382">Плоский альфа-канал кодируется как отдельное изображение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="cc1b7-383">Данные изображения и альфа-канал декодированы независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="cc1b7-384">При необходимости можно задать уровень качества альфа-канала, задав свойство [алфакуалити](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="cc1b7-385">Альфа-канал с чередованием поддерживается только для определенных форматов пикселей RGB.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="cc1b7-386">Плоская альфа-версия поддерживается для любого формата изображения, определяющего альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="cc1b7-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="cc1b7-387">Lossless</span></span>

<span data-ttu-id="cc1b7-388">Включает сжатие потерь.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-388">Enables losses compression.</span></span>



| <span data-ttu-id="cc1b7-389">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-389">Data type</span></span>         | <span data-ttu-id="cc1b7-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-390">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-391">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="cc1b7-392">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-393">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-393">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-394">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="cc1b7-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="cc1b7-395">Если значение является **вариантным \_ true**, кодировщик использует сжатие без потерь.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="cc1b7-396">Если задано **\_ значение true**, это свойство переопределяет свойство [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="cc1b7-397">Перекрытие</span><span class="sxs-lookup"><span data-stu-id="cc1b7-397">Overlap</span></span>

<span data-ttu-id="cc1b7-398">Задает уровень фильтрации перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="cc1b7-399">При фильтрации наложения коэффициенты преобразования применяются для границ блока и макроблокк.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="cc1b7-400">Это может сократить количество блокирующих артефактов.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="cc1b7-401">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-401">Data type</span></span> | <span data-ttu-id="cc1b7-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-402">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-403">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-403">Range</span></span> | <span data-ttu-id="cc1b7-404">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cc1b7-405">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-405">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-406">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-406">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-407">0 – 4</span><span class="sxs-lookup"><span data-stu-id="cc1b7-407">0–4</span></span>   | <span data-ttu-id="cc1b7-408">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-408">1</span></span>       |



 



| <span data-ttu-id="cc1b7-409">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-409">Value</span></span> | <span data-ttu-id="cc1b7-410">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="cc1b7-411">0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-411">0</span></span>     | <span data-ttu-id="cc1b7-412">Без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-412">No overlap.</span></span>                                   |
| <span data-ttu-id="cc1b7-413">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-413">1</span></span>     | <span data-ttu-id="cc1b7-414">Один уровень перекрытия, мягкое мозаичное разбиение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="cc1b7-415">(по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-415">(Default.)</span></span> |
| <span data-ttu-id="cc1b7-416">2</span><span class="sxs-lookup"><span data-stu-id="cc1b7-416">2</span></span>     | <span data-ttu-id="cc1b7-417">Два уровня перекрытия, мягкое мозаичное разбиение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="cc1b7-418">3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-418">3</span></span>     | <span data-ttu-id="cc1b7-419">Один уровень перекрытия, жесткое разбиение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="cc1b7-420">4</span><span class="sxs-lookup"><span data-stu-id="cc1b7-420">4</span></span>     | <span data-ttu-id="cc1b7-421">Два уровня перекрытия, жесткое разбиение.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="cc1b7-422">Определения:</span><span class="sxs-lookup"><span data-stu-id="cc1b7-422">Definitions:</span></span>

-   <span data-ttu-id="cc1b7-423">Один уровень перекрытия: закодированные значения для блоков 4x4 изменяются на основе соседних блоков.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="cc1b7-424">Два уровня перекрытия: применяется первый уровень перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="cc1b7-425">Кроме того, закодированные значения 16x16 макроблоккс изменяются на основе соседних макроблоккс.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="cc1b7-426">Мягкое разбиение: Фильтрация наложения применяется к границам плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="cc1b7-427">Жесткое разбиение: Фильтрация наложения не применяется к границам плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="cc1b7-428">Сложные плитки могут представлять некоторые визуальные артефакты, а также границы плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="cc1b7-429">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="cc1b7-430">прогрессивемоде</span><span class="sxs-lookup"><span data-stu-id="cc1b7-430">ProgressiveMode</span></span>

<span data-ttu-id="cc1b7-431">Включает или отключает прогрессивную кодировку.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="cc1b7-432">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-432">Data type</span></span>         | <span data-ttu-id="cc1b7-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-433">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-434">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cc1b7-435">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-436">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-436">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-437">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="cc1b7-438">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-438">Value</span></span>              | <span data-ttu-id="cc1b7-439">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="cc1b7-440">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="cc1b7-441">Последовательный режим (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="cc1b7-442">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="cc1b7-443">Прогрессивный режим.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="cc1b7-444">Качество</span><span class="sxs-lookup"><span data-stu-id="cc1b7-444">Quality</span></span>

<span data-ttu-id="cc1b7-445">Задает качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-445">Sets the compression quality.</span></span>



| <span data-ttu-id="cc1b7-446">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-446">Data type</span></span> | <span data-ttu-id="cc1b7-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-447">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-448">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-448">Range</span></span> | <span data-ttu-id="cc1b7-449">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cc1b7-450">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-450">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-451">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-451">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-452">1 – 255</span><span class="sxs-lookup"><span data-stu-id="cc1b7-452">1–255</span></span> | <span data-ttu-id="cc1b7-453">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-453">1</span></span>       |



 

<span data-ttu-id="cc1b7-454">Значение 1 означает режим без потерь.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="cc1b7-455">Увеличение значений приводит к увеличению коэффициента сжатия и более низкому качеству изображения.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="cc1b7-456">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="cc1b7-457">стреамонли</span><span class="sxs-lookup"><span data-stu-id="cc1b7-457">StreamOnly</span></span>

<span data-ttu-id="cc1b7-458">Включает или отключает режим "только потоковая передача".</span><span class="sxs-lookup"><span data-stu-id="cc1b7-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="cc1b7-459">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-459">Data type</span></span>         | <span data-ttu-id="cc1b7-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-460">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-461">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cc1b7-462">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-463">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-463">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-464">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="cc1b7-465">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-465">Value</span></span>              | <span data-ttu-id="cc1b7-466">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-467">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="cc1b7-468">Кодировщик выводит поток необработанных изображений без метаданных.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="cc1b7-469">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="cc1b7-470">Кодировщик выводит формат контейнера (поток изображений и метаданные).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="cc1b7-471">Подвыборка</span><span class="sxs-lookup"><span data-stu-id="cc1b7-471">Subsampling</span></span>

<span data-ttu-id="cc1b7-472">Задает подвыборку чрома.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="cc1b7-473">Это свойство применяется только к изображениям RGB.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="cc1b7-474">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-474">Data type</span></span> | <span data-ttu-id="cc1b7-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-475">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-476">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-476">Range</span></span> | <span data-ttu-id="cc1b7-477">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="cc1b7-478">**учар**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-478">**UCHAR**</span></span> | <span data-ttu-id="cc1b7-479">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-479">**VT\_UI1**</span></span> | <span data-ttu-id="cc1b7-480">0 – 3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-480">0–3</span></span>   | <span data-ttu-id="cc1b7-481">3, если [имажекуалити](#imagequality) > 0,8; в противном случае 1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc1b7-482">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1b7-482">Value</span></span></th>
<th><span data-ttu-id="cc1b7-483">Описание</span><span class="sxs-lookup"><span data-stu-id="cc1b7-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc1b7-484">3</span><span class="sxs-lookup"><span data-stu-id="cc1b7-484">3</span></span></td>
<td><span data-ttu-id="cc1b7-485">Кодировка 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-485">4:4:4 encoding.</span></span> <span data-ttu-id="cc1b7-486">Сохраняет полное разрешение чрома.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1b7-487">2</span><span class="sxs-lookup"><span data-stu-id="cc1b7-487">2</span></span></td>
<td><span data-ttu-id="cc1b7-488">Кодировка 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-488">4:2:2 encoding.</span></span> <span data-ttu-id="cc1b7-489">Разрешение чрома — 1/2 для разрешения освещенности.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1b7-490">1</span><span class="sxs-lookup"><span data-stu-id="cc1b7-490">1</span></span></td>
<td><span data-ttu-id="cc1b7-491">Кодировка 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-491">4:2:0 encoding.</span></span> <span data-ttu-id="cc1b7-492">Разрешение чрома — 1/4 для разрешения освещенности.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1b7-493">0</span><span class="sxs-lookup"><span data-stu-id="cc1b7-493">0</span></span></td>
<td><span data-ttu-id="cc1b7-494">Кодирование 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-494">4:0:0 encoding.</span></span> <span data-ttu-id="cc1b7-495">Отменяет все значения чрома и сохраняет только светимость.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1b7-496">Этот режим не рекомендуется, поскольку кодек использует немного измененное определение светимости для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="cc1b7-497">Вместо этого лучше преобразовать изображение в монохромную перед кодированием.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cc1b7-498">4:2:2 и 4:2:0 сохраняют сведения о освещенности за счет сведений о цвете.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="cc1b7-499">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="cc1b7-500">усекодекоптионс</span><span class="sxs-lookup"><span data-stu-id="cc1b7-500">UseCodecOptions</span></span>

<span data-ttu-id="cc1b7-501">Указывает, следует ли использовать свойства [Quality](#image-quality-settings), [перекрытия](#overlap)и [подвыборки](#subsampling) вместо универсального свойства [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cc1b7-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="cc1b7-502">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-502">Data type</span></span>         | <span data-ttu-id="cc1b7-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-503">VARTYPE</span></span>      | <span data-ttu-id="cc1b7-504">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cc1b7-505">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-506">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-506">**VT\_BOOL**</span></span> | <span data-ttu-id="cc1b7-507">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="cc1b7-508">вертикалтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cc1b7-508">VerticalTileSlices</span></span>

<span data-ttu-id="cc1b7-509">Задает количество горизонтальных плиток.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="cc1b7-510">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc1b7-510">Data type</span></span>  | <span data-ttu-id="cc1b7-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-511">VARTYPE</span></span>     | <span data-ttu-id="cc1b7-512">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cc1b7-512">Range</span></span>  | <span data-ttu-id="cc1b7-513">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc1b7-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="cc1b7-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-514">**USHORT**</span></span> | <span data-ttu-id="cc1b7-515">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-515">**VT\_UI2**</span></span> | <span data-ttu-id="cc1b7-516">0 — 4095</span><span class="sxs-lookup"><span data-stu-id="cc1b7-516">0–4095</span></span> | <span data-ttu-id="cc1b7-517">(высота изображения – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="cc1b7-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="cc1b7-518">Значение — это число вертикальных подразделений; то есть число вертикальных плиток — 1.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="cc1b7-519">Поддерживаемые форматы цвета</span><span class="sxs-lookup"><span data-stu-id="cc1b7-519">Supported Color Formats</span></span>

<span data-ttu-id="cc1b7-520">Дополнительные сведения об этих форматах см. в разделе [собственные форматы пикселей](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="cc1b7-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="cc1b7-521">**Форматы целых чисел RGB**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="cc1b7-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="cc1b7-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="cc1b7-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="cc1b7-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="cc1b7-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="cc1b7-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="cc1b7-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="cc1b7-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="cc1b7-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="cc1b7-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="cc1b7-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="cc1b7-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="cc1b7-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="cc1b7-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="cc1b7-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="cc1b7-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="cc1b7-530">**Форматы RGB с фиксированной запятой**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="cc1b7-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="cc1b7-536">**Форматы RGB с плавающей запятой**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="cc1b7-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="cc1b7-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="cc1b7-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="cc1b7-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="cc1b7-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="cc1b7-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="cc1b7-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="cc1b7-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="cc1b7-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="cc1b7-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="cc1b7-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="cc1b7-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="cc1b7-544">**Форматы в градациях серого**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="cc1b7-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="cc1b7-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="cc1b7-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="cc1b7-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="cc1b7-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="cc1b7-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="cc1b7-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cc1b7-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="cc1b7-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="cc1b7-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="cc1b7-551">**Упакованные форматы**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-551">**Packed formats**</span></span>
    -   <span data-ttu-id="cc1b7-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="cc1b7-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="cc1b7-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="cc1b7-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="cc1b7-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="cc1b7-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="cc1b7-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="cc1b7-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="cc1b7-556">**Форматы CMYK**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="cc1b7-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="cc1b7-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="cc1b7-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="cc1b7-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="cc1b7-560">**Форматы N-Channel**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="cc1b7-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="cc1b7-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="cc1b7-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="cc1b7-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="cc1b7-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="cc1b7-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="cc1b7-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="cc1b7-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="cc1b7-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="cc1b7-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="cc1b7-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="cc1b7-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="cc1b7-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cc1b7-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
