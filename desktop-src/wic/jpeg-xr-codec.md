---
description: Собственный кодек XR JPEG доступен через компонент Windows Imaging Component (WIC). Формат JPEG XR, который поддерживает кодек, предназначен для бытовой цифровой фотографии.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Общие сведения о коде XR JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444467"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="cbe4e-104">Общие сведения о коде XR JPEG</span><span class="sxs-lookup"><span data-stu-id="cbe4e-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="cbe4e-105">Собственный кодек XR JPEG доступен через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="cbe4e-106">Формат JPEG XR, который поддерживает кодек, предназначен для бытовой цифровой фотографии.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="cbe4e-107">Формат JPEG XR может добиться удвоенной эффективности сжатия исходного формата JPEG с менее заметными артефактами сжатия.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="cbe4e-108">К функциям JPEG XR относятся:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="cbe4e-109">Поддержка монохромных изображений, RGB, CMYK и n-канального изображения</span><span class="sxs-lookup"><span data-stu-id="cbe4e-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="cbe4e-110">8-, 16-и 32-разрядные форматы целых чисел</span><span class="sxs-lookup"><span data-stu-id="cbe4e-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="cbe4e-111">Высокий динамический диапазон, форматы с широкими охватами, использующие значения цвета с фиксированной точкой или с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="cbe4e-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="cbe4e-112">Прогрессивное декодирование</span><span class="sxs-lookup"><span data-stu-id="cbe4e-112">Progressive decoding</span></span>
-   <span data-ttu-id="cbe4e-113">Шифрование с потерей или без потерь с использованием того же алгоритма сжатия</span><span class="sxs-lookup"><span data-stu-id="cbe4e-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="cbe4e-114">Поддержка декодирования интересующих регионов в больших изображениях</span><span class="sxs-lookup"><span data-stu-id="cbe4e-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="cbe4e-115">Формат JPEG XR определяется в следующих документах стандартов:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="cbe4e-116">ITU-T T. 832: *информационная технология — JPEG XR Image система кодирования — спецификация кодирования изображения*</span><span class="sxs-lookup"><span data-stu-id="cbe4e-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="cbe4e-117">ISO/IEC 29199-2:2010: *информационные технологии — система кодирования изображений JPEG XR — часть 2. Спецификация кодирования изображения*</span><span class="sxs-lookup"><span data-stu-id="cbe4e-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="cbe4e-118">Стандарт JPEG XR Standard в основном основан на [фотографическом формате HD](hdphoto-format-overview.md) , но существуют некоторые различия между двумя форматами.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="cbe4e-119">В Windows 8 кодек HD Photo был обновлен для поддержки JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="cbe4e-120">Теперь кодировщик всегда выводит двоичный поток, соответствующий XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="cbe4e-121">Декодер может декодировать изображения JPEG XR и HD Photo.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="cbe4e-122">В кодеке XR JPEG были внесены существенные улучшения производительности по отношению к графическому кодеку HD.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="cbe4e-123">Например, улучшено декодирование изображений с подразрешением, например создание эскизов, а также декодирование изображений с низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="cbe4e-124">Рекомендуется использовать формат JPEG XR вместо формата фотографии HD.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="cbe4e-125">Сведения о кодека</span><span class="sxs-lookup"><span data-stu-id="cbe4e-125">Codec Information</span></span>



|      <span data-ttu-id="cbe4e-126">Компонент</span><span class="sxs-lookup"><span data-stu-id="cbe4e-126">Component</span></span>      |    <span data-ttu-id="cbe4e-127">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-127">Description</span></span>                                                          |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-128">Расширение имени файла</span><span class="sxs-lookup"><span data-stu-id="cbe4e-128">File name extension</span></span> | <span data-ttu-id="cbe4e-129">"жкср" и "формате WDP"</span><span class="sxs-lookup"><span data-stu-id="cbe4e-129">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="cbe4e-130">Идентификатор GUID контейнера</span><span class="sxs-lookup"><span data-stu-id="cbe4e-130">Container GUID</span></span>      | <span data-ttu-id="cbe4e-131">**GUID \_ контаинерформатвмп**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-131">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="cbe4e-132">GUID декодера</span><span class="sxs-lookup"><span data-stu-id="cbe4e-132">Decoder GUID</span></span>        | <span data-ttu-id="cbe4e-133">**\_ВИКВМПДЕКОДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-133">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="cbe4e-134">GUID кодировщика</span><span class="sxs-lookup"><span data-stu-id="cbe4e-134">Encoder GUID</span></span>        | <span data-ttu-id="cbe4e-135">**\_ВИКВМПЕНКОДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-135">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="cbe4e-136">Поддержка профилей</span><span class="sxs-lookup"><span data-stu-id="cbe4e-136">Profile Support</span></span>     | <span data-ttu-id="cbe4e-137">Кодировщик и декодер поддерживают до основного профиля и до уровня 128.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-137">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="cbe4e-138">Функции кодеков</span><span class="sxs-lookup"><span data-stu-id="cbe4e-138">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="cbe4e-139">Высокий динамический диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-139">High Dynamic Range</span></span>

<span data-ttu-id="cbe4e-140">JPEG XR поддерживает высокодинамические изображения диапазонов с плавающей запятой или цвета с фиксированной точкой.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-140">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="cbe4e-141">В этих цветовых форматах числовой диапазон пикселей больше видимого диапазона, поэтому можно настроить цвета выше или ниже видимого диапазона на промежуточных этапах обработки.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-141">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="cbe4e-142">Фиксированная точка: в представлении с фиксированной запятой 0 представляет черный, а 1,0 — максимальную насыщенность.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-142">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="cbe4e-143">Кодек JPEG XR поддерживает 16-разрядные и 32-разрядные форматы с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-143">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="cbe4e-144">Для 16-разрядной версии 1,0 = 0x2000h, которая предоставляет 13 бит для видимого диапазона \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-144">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="cbe4e-145">Общий диапазон составляет от – 4,0 до + 3,999 и сопоставляется линейно.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-145">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="cbe4e-146">Для 32-bit, 1,0 = 0x01000000h видимым диапазоном является 24 бита, а общий диапазон — от – 128 до + 127,999.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-146">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="cbe4e-147">С плавающей запятой: в представлении с плавающей запятой 0 представляет черный, а 1,0 — максимальную насыщенность.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-147">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="cbe4e-148">Кодек JPEG XR поддерживает 16-разрядные и 32-разрядные форматы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-148">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="cbe4e-149">Плитки</span><span class="sxs-lookup"><span data-stu-id="cbe4e-149">Tiles</span></span>

<span data-ttu-id="cbe4e-150">Фрейм можно секционировать на прямоугольные подобласти, называемые *плитками*.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-150">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="cbe4e-151">Плитка — это область изображения, содержащая прямоугольные массивы макроблоккс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-151">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="cbe4e-152">Плитки позволяют декодировать регионы изображения без обработки всего изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-152">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="cbe4e-153">Во время кодирования выберите число плиток, задав свойства **хоризонталтилеслицес** и **вертикалтилеслицес** .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-153">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="cbe4e-154">Минимальный размер плитки — 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-154">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="cbe4e-155">Кодировщик корректирует количество плиток, чтобы поддерживать это ограничение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-155">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="cbe4e-156">Существует дополнительная нагрузка на хранилище и обработку, связанная с каждой плиткой, поэтому следует учитывать количество плиток, необходимых для конкретных сценариев.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-156">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="cbe4e-157">Выходные данные потока изображений</span><span class="sxs-lookup"><span data-stu-id="cbe4e-157">Image Stream Output</span></span>

<span data-ttu-id="cbe4e-158">Стандарт JPEG-XR определяет две части файла JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-158">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="cbe4e-159">Поток битов образа, определенный в тексте стандарта.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-159">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="cbe4e-160">Контейнер изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-160">The image container.</span></span> <span data-ttu-id="cbe4e-161">Файл содержит метаданные EXIF и XMP и определяется в приложении A из стандарта.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-161">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="cbe4e-162">Можно и в стандартном случае внедрять поток изображения в контейнер файлов другого типа.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-162">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="cbe4e-163">Кодировщик поддерживает режим только потоковой передачи, который выводит поток битов необработанного изображения без контейнера изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-163">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="cbe4e-164">Приложение может хранить битовый поток в каком бы то ни было другом формате контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-164">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="cbe4e-165">Чтобы включить режим «только потоковая передача», установите свойство **стреамонли** .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-165">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="cbe4e-166">Параметры качества изображения</span><span class="sxs-lookup"><span data-stu-id="cbe4e-166">Image Quality Settings</span></span>

<span data-ttu-id="cbe4e-167">Несколько свойств кодека управляют качеством выходного изображения из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-167">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="cbe4e-168">[Имажекуалити](#imagequality) — это свойство, которое является общим для кодеков WIC.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-168">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="cbe4e-169">Он задает качество изображения как одно значение с плавающей запятой от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-169">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="cbe4e-170">Свойства [Quality](#image-quality-settings), [перекрытия](#overlap)и [подвыборки](#subsampling) обеспечивают больший контроль над параметрами качества.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-170">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="cbe4e-171">Чтобы использовать свойства " [качество](#image-quality-settings)", " [Перекрытие](#overlap)" и " [подвыборка](#subsampling) ", задайте для свойства [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-171">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="cbe4e-172">Если [усекодекоптионс](#usecodecoptions) имеет значение **Variant \_ false** (по умолчанию используется **вариант \_ false** ), кодировщик использует свойство [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-172">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="cbe4e-173">Кодировщик сопоставляет значение Имажекуалити с [качеством](#image-quality-settings), [перекрытием](#overlap)и [подвыборкой](#subsampling) с помощью таблицы подстановки.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-173">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="cbe4e-174">Кодировщик не поддерживает свойство **компрессионкуалити** .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-174">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="cbe4e-175">Сжатый перекодированный домен</span><span class="sxs-lookup"><span data-stu-id="cbe4e-175">Compressed Domain Transcode</span></span>

<span data-ttu-id="cbe4e-176">Кодек JPEG XR может выполнять определенные преобразования изображений без фактического декодирования сжатых данных и их повторной кодировки.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-176">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="cbe4e-177">Операции со сжатыми доменами очень эффективны и позволяют избежать дополнительной потери качества, типичной при расшифровке и повторном кодировании сжатого с потерей изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-177">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="cbe4e-178">Поддерживаются следующие операции со сжатыми доменами:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-178">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="cbe4e-179">Обрезать область изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-179">Crop a region of the image.</span></span>
-   <span data-ttu-id="cbe4e-180">Поворот или отражение изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-180">Rotate or flip the image.</span></span>
-   <span data-ttu-id="cbe4e-181">Отбросить данные частоты, чтобы создать файл изображения меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-181">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="cbe4e-182">Реорганизовать изображение между пространственным и частотным порядком.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-182">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="cbe4e-183">Кодировщик XR JPEG использует сжатое перекодирование домена, если это возможно, если исходный образ является JPEG-изображением XR.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-183">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="cbe4e-184">Когда кодировщик выполняет операцию со сжатым доменом, он игнорирует следующие свойства кодека: [алфакуалити](#alphaquality), [имажекуалити](#imagequality), [интерлеаведалфа](#interleavedalpha), [](#lossless)[Перекрытие](#overlap)без потери [качества](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-184">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="cbe4e-185">Если свойства [хоризонталтилеслицес](/windows) и [вертикалтилеслицес](/windows) существуют, их необходимо присвоить нулю.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-185">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="cbe4e-186">Нельзя изменить размер плитки изображения в составе сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-186">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="cbe4e-187">В приведенном ниже списке описывается выполнение преобразований изображений.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-187">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="cbe4e-188">Чтобы обрезать изображение, задайте нужный регион в параметре [**викрект**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) метода **вритесаурце** .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-188">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="cbe4e-189">Чтобы повернуть или перевернуть изображение, установите свойство [битмаптрансформ](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-189">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="cbe4e-190">Чтобы отменить данные частоты в изображении, установите свойство [имажедатадискард](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-190">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="cbe4e-191">Чтобы отбросить данные частоты в альфа-канале, установите свойство [алфадатадискард](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-191">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="cbe4e-192">При отклонении данных частоты уменьшается размер закодированного файла и может снизиться разрешение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-192">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="cbe4e-193">Чтобы изменить организацию изображения между частотой и пространственной сортировкой, задайте свойство [фрекуенциордеринг](/windows) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-193">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="cbe4e-194">Чтобы отключить сжатый перекодировку домена и заставить кодировщик повторно закодировать образ, присвойте параметру [усекодекоптионс](#usecodecoptions) **значение Variant \_ true** и присвойте параметру [компресседдомаинтранскоде](#compresseddomaintranscode) значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-194">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="cbe4e-195">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="cbe4e-195">Encoder Options</span></span>

<span data-ttu-id="cbe4e-196">Чтобы задать свойства кодировки, используйте интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-196">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="cbe4e-197">Дополнительные сведения см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-197">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="cbe4e-198">В следующем списке указаны параметры кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-198">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="cbe4e-199">алфадатадискард</span><span class="sxs-lookup"><span data-stu-id="cbe4e-199">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="cbe4e-200">алфакуалити</span><span class="sxs-lookup"><span data-stu-id="cbe4e-200">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="cbe4e-201">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="cbe4e-201">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="cbe4e-202">компресседдомаинтранскоде</span><span class="sxs-lookup"><span data-stu-id="cbe4e-202">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="cbe4e-203">фрекуенциордер</span><span class="sxs-lookup"><span data-stu-id="cbe4e-203">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="cbe4e-204">хоризонталтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cbe4e-204">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="cbe4e-205">игнореоверлап</span><span class="sxs-lookup"><span data-stu-id="cbe4e-205">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="cbe4e-206">имажедатадискард</span><span class="sxs-lookup"><span data-stu-id="cbe4e-206">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="cbe4e-207">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="cbe4e-207">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="cbe4e-208">интерлеаведалфа</span><span class="sxs-lookup"><span data-stu-id="cbe4e-208">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="cbe4e-209">Lossless</span><span class="sxs-lookup"><span data-stu-id="cbe4e-209">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="cbe4e-210">Перекрытие</span><span class="sxs-lookup"><span data-stu-id="cbe4e-210">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="cbe4e-211">прогрессивемоде</span><span class="sxs-lookup"><span data-stu-id="cbe4e-211">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="cbe4e-212">Качество</span><span class="sxs-lookup"><span data-stu-id="cbe4e-212">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="cbe4e-213">стреамонли</span><span class="sxs-lookup"><span data-stu-id="cbe4e-213">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="cbe4e-214">Подвыборка</span><span class="sxs-lookup"><span data-stu-id="cbe4e-214">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="cbe4e-215">усекодекоптионс</span><span class="sxs-lookup"><span data-stu-id="cbe4e-215">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="cbe4e-216">вертикалтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cbe4e-216">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="cbe4e-217">алфадатадискард</span><span class="sxs-lookup"><span data-stu-id="cbe4e-217">AlphaDataDiscard</span></span>

<span data-ttu-id="cbe4e-218">Задает объем данных альфа-частоты, которые должны быть удалены во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-218">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="cbe4e-219">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-219">Data type</span></span> | <span data-ttu-id="cbe4e-220">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-220">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-221">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-221">Range</span></span> | <span data-ttu-id="cbe4e-222">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-222">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cbe4e-223">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-223">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-224">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-224">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-225">0 – 4</span><span class="sxs-lookup"><span data-stu-id="cbe4e-225">0–4</span></span>   | <span data-ttu-id="cbe4e-226">Нет</span><span class="sxs-lookup"><span data-stu-id="cbe4e-226">None</span></span>    |



 

<span data-ttu-id="cbe4e-227">Это свойство применяется, только если свойство [компресседдомаинтранскоде](#compresseddomaintranscode) имеет значение **Variant \_ true** , а изображение содержит плоский альфа-канал или альфа-канал с чередованием; в противном случае он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-227">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="cbe4e-228">Для изображений, содержащих плоский альфа-канал, допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-228">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="cbe4e-229">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-229">Value</span></span> | <span data-ttu-id="cbe4e-230">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-230">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-231">0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-231">0</span></span>     | <span data-ttu-id="cbe4e-232">Данные частоты изображения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-232">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cbe4e-233">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-233">1</span></span>     | <span data-ttu-id="cbe4e-234">Флексбитс отклоняется.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-234">The flexbits are discarded.</span></span> <span data-ttu-id="cbe4e-235">Это произвольно сокращает качество плоского альфа-канала для перекодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-235">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="cbe4e-236">, без изменения эффективного разрешения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-236">, without a change in the effective resolution.</span></span> <span data-ttu-id="cbe4e-237">Точное уменьшение размера и качества файла зависит от множества факторов и не может быть точно указано.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-237">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="cbe4e-238">2</span><span class="sxs-lookup"><span data-stu-id="cbe4e-238">2</span></span>     | <span data-ttu-id="cbe4e-239">Полоса данных высокой тактовой частоты отбрасывается, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-239">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="cbe4e-240">Это эффективно сокращает разрешение плоского альфа-канала на коэффициент 4 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-240">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="cbe4e-241">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждом блоке 4x4 пикселей альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-241">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="cbe4e-242">Как правило, это значение следует задавать, только если свойство [имажедатадискард](#imagedatadiscard) имеет то же значение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-242">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="cbe4e-243">3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-243">3</span></span>     | <span data-ttu-id="cbe4e-244">Полосы данных с высокой и низкой тактовой частотой отбрасываются, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-244">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="cbe4e-245">Это ффективели уменьшает разрешение плоского альфа-канала на коэффициент 16 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-245">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="cbe4e-246">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждой 16x16 макроблокк пикселов альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-246">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="cbe4e-247">Как правило, это значение следует задавать, только если свойство [имажедатадискард](#imagedatadiscard) имеет то же значение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-247">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="cbe4e-248">4</span><span class="sxs-lookup"><span data-stu-id="cbe4e-248">4</span></span>     | <span data-ttu-id="cbe4e-249">Полностью удаляется альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-249">The alpha channel is completely discarded.</span></span> <span data-ttu-id="cbe4e-250">Формат пикселей перекодированного изображения изменяется в соответствии с удалением альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-250">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="cbe4e-251">Для образов, содержащих альфа-канал с чередованием, допустимо следующее значение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-251">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="cbe4e-252">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-252">Value</span></span> | <span data-ttu-id="cbe4e-253">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-253">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-254">4</span><span class="sxs-lookup"><span data-stu-id="cbe4e-254">4</span></span>     | <span data-ttu-id="cbe4e-255">Полностью удаляется альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-255">The alpha channel is completely discarded.</span></span> <span data-ttu-id="cbe4e-256">Формат пикселей перекодированного изображения изменяется в соответствии с удалением альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-256">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="cbe4e-257">Для Alpha с чередованием, если это свойство не имеет значение 4, альфа-канал обрабатывается так же, как данные изображения, в соответствии со значением свойства [имажедатадискард](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-257">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="cbe4e-258">алфакуалити</span><span class="sxs-lookup"><span data-stu-id="cbe4e-258">AlphaQuality</span></span>

<span data-ttu-id="cbe4e-259">Задает качество сжатия для изображения плоского альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-259">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="cbe4e-260">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-260">Data type</span></span> | <span data-ttu-id="cbe4e-261">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-261">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-262">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-262">Range</span></span> | <span data-ttu-id="cbe4e-263">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-263">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cbe4e-264">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-264">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-265">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-265">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-266">1 – 255</span><span class="sxs-lookup"><span data-stu-id="cbe4e-266">1–255</span></span> | <span data-ttu-id="cbe4e-267">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-267">1</span></span>       |



 

<span data-ttu-id="cbe4e-268">Это свойство применяется, если изображение имеет альфа-канал, а свойство [интерлеаведалфа](#interleavedalpha) имеет значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-268">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="cbe4e-269">Значение 1 означает режим без потерь.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-269">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="cbe4e-270">Увеличение значений приводит к увеличению коэффициента сжатия и более низкому качеству изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-270">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="cbe4e-271">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="cbe4e-271">BitmapTransform</span></span>

<span data-ttu-id="cbe4e-272">Указывает, будет ли изображение повернуто или отражено при декодировании.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-272">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="cbe4e-273">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-273">Data type</span></span> | <span data-ttu-id="cbe4e-274">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-274">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-275">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-275">Range</span></span>                                                                     | <span data-ttu-id="cbe4e-276">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-276">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="cbe4e-277">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-277">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-278">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-278">**VT\_UI1**</span></span> | [<span data-ttu-id="cbe4e-279">**викбитмаптрансформоптионс**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-279">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="cbe4e-280">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-280">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="cbe4e-281">компресседдомаинтранскоде</span><span class="sxs-lookup"><span data-stu-id="cbe4e-281">CompressedDomainTranscode</span></span>

<span data-ttu-id="cbe4e-282">Включает или отключает перекодирование сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-282">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="cbe4e-283">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-283">Data type</span></span>         | <span data-ttu-id="cbe4e-284">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-284">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-285">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-285">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="cbe4e-286">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-286">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-287">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-287">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-288">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-288">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="cbe4e-289">Чтобы отключить сжатые операции домена, задайте для этого свойства значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-289">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="cbe4e-290">фрекуенциордер</span><span class="sxs-lookup"><span data-stu-id="cbe4e-290">FrequencyOrder</span></span>

<span data-ttu-id="cbe4e-291">Включает кодирование в порядке частот.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-291">Enables encoding in frequency order.</span></span> <span data-ttu-id="cbe4e-292">Реализации устройств кодировщиков JPEG XR могут организовывать файл в пространственном порядке, чтобы уменьшить объем памяти, необходимый для кодирования.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-292">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="cbe4e-293">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-293">Data type</span></span>         | <span data-ttu-id="cbe4e-294">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-294">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-295">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-295">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="cbe4e-296">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-296">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-297">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-297">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-298">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-298">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="cbe4e-299">**Вариант \_ TRUE**: порядок частот.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-299">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="cbe4e-300">Данные с наименьшей частотой отображаются в файле первыми, а содержимое изображения группируются по частоте, а не к пространственной ориентации.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-300">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="cbe4e-301">Упорядочение файла по частоте обеспечивает лучшую производительность при декодировании на основе частоты.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-301">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="cbe4e-302">**Вариант \_ FALSE**: пространственный порядок.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-302">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="cbe4e-303">Пространственный порядок сокращает объем памяти, необходимый для кодирования</span><span class="sxs-lookup"><span data-stu-id="cbe4e-303">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="cbe4e-304">Рекомендуется использовать частотный порядок, если нет причин, связанных с производительностью или конкретными приложениями, для использования пространственного порядка.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-304">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="cbe4e-305">хоризонталтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cbe4e-305">HorizontalTileSlices</span></span>

<span data-ttu-id="cbe4e-306">Задает количество горизонтальных плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-306">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="cbe4e-307">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-307">Data type</span></span>  | <span data-ttu-id="cbe4e-308">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-308">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-309">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-309">Range</span></span>  | <span data-ttu-id="cbe4e-310">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-310">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="cbe4e-311">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-311">**USHORT**</span></span> | <span data-ttu-id="cbe4e-312">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-312">**VT\_UI2**</span></span> | <span data-ttu-id="cbe4e-313">0 — 4095</span><span class="sxs-lookup"><span data-stu-id="cbe4e-313">0–4095</span></span> | <span data-ttu-id="cbe4e-314">(ширина изображения — 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="cbe4e-314">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="cbe4e-315">Значение — это число горизонтальных делений; то есть числом горизонтальных плиток — 1.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-315">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="cbe4e-316">игнореоверлап</span><span class="sxs-lookup"><span data-stu-id="cbe4e-316">IgnoreOverlap</span></span>

<span data-ttu-id="cbe4e-317">Указывает, как кодировщик обрабатывает границы плиток во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-317">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="cbe4e-318">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-318">Data type</span></span>         | <span data-ttu-id="cbe4e-319">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-319">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-320">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-320">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cbe4e-321">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-321">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-322">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-322">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-323">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-323">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="cbe4e-324">Это свойство применяется только в том случае, если для свойства [компресседдомаинтранскоде](#compresseddomaintranscode) задано значение **Variant \_ true** , а в подобласти выполняется перекодировка только одной или нескольких плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-324">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="cbe4e-325">Операция по умолчанию для перекодировки региона заключается в том, чтобы расширить запрошенную область, включив в нее окружающие Пиксели, необходимые для перекрытия границ области.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-325">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="cbe4e-326">Если для этого свойства задано значение **Variant \_ true**, кодек игнорирует окружающие пикселы и извлекаются только выбранные плитка или плитки.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-326">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="cbe4e-327">Если исходное изображение не является мозаичным или если запрошенная область содержит частичные плитки, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-327">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="cbe4e-328">имажедатадискард</span><span class="sxs-lookup"><span data-stu-id="cbe4e-328">ImageDataDiscard</span></span>

<span data-ttu-id="cbe4e-329">Задает объем данных частоты образа, которые должны быть удалены во время перекодирования сжатого домена.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-329">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="cbe4e-330">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-330">Data type</span></span> | <span data-ttu-id="cbe4e-331">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-331">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-332">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-332">Range</span></span> | <span data-ttu-id="cbe4e-333">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-333">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cbe4e-334">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-334">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-335">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-335">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-336">0 – 3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-336">0–3</span></span>   | <span data-ttu-id="cbe4e-337">0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-337">0</span></span>       |



 

<span data-ttu-id="cbe4e-338">Это свойство применяется только в том случае, если свойство [компресседдомаинтранскоде](#compresseddomaintranscode) имеет значение **Variant \_ true**; в противном случае оно игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-338">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="cbe4e-339">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-339">Value</span></span> | <span data-ttu-id="cbe4e-340">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-340">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-341">0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-341">0</span></span>     | <span data-ttu-id="cbe4e-342">Данные частоты изображения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-342">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cbe4e-343">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-343">1</span></span>     | <span data-ttu-id="cbe4e-344">Флексбитс отклоняется.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-344">The flexbits are discarded.</span></span> <span data-ttu-id="cbe4e-345">Это произвольно сокращает качество перекодированного изображения без изменения эффективного разрешения изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-345">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="cbe4e-346">Точное уменьшение размера и качества файла зависит от множества факторов и не может быть точно указано.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-346">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="cbe4e-347">Это значение возвращает ошибку, указанную для альфа-канала с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-347">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="cbe4e-348">2</span><span class="sxs-lookup"><span data-stu-id="cbe4e-348">2</span></span>     | <span data-ttu-id="cbe4e-349">Полоса данных высокой тактовой частоты отбрасывается, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-349">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="cbe4e-350">Это уменьшает разрешение перекодированного изображения с помощью коэффициента 4 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-350">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="cbe4e-351">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждом блоке 4x4 пикселей.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-351">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="cbe4e-352">Таким образом, перекодированный образ должен быть downsampled соответствующим образом при его декодировании.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-352">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="cbe4e-353">3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-353">3</span></span>     | <span data-ttu-id="cbe4e-354">Полосы данных с высокой и низкой тактовой частотой отбрасываются, включая флексбитс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-354">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="cbe4e-355">Это уменьшает разрешение перекодированного изображения с помощью коэффициента 16 в обоих измерениях.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-355">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="cbe4e-356">Фактические размеры перекодированного изображения остаются неизменными, но изображение теряет все детали в каждой 16x16 макроблокк пикселей.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-356">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="cbe4e-357">Таким образом, перекодированный образ должен быть downsampled соответствующим образом при его декодировании.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-357">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="cbe4e-358">Если изображение содержит альфа-канал с чередованием, значение [имажедатадискард](#imagedatadiscard) применяется к альфа-каналу, если только свойство [алфадатадискард](#alphadatadiscard) не имеет значение 4. в этом случае альфа-канал отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-358">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="cbe4e-359">Для плоского альфа-канала данные частоты, которые отбрасываются, управляются свойством [алфадатадискард](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-359">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="cbe4e-360">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="cbe4e-360">ImageQuality</span></span>

<span data-ttu-id="cbe4e-361">Задает качество изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-361">Sets the image quality.</span></span>



| <span data-ttu-id="cbe4e-362">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-362">Data type</span></span> | <span data-ttu-id="cbe4e-363">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-363">VARTYPE</span></span>    | <span data-ttu-id="cbe4e-364">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-364">Range</span></span> | <span data-ttu-id="cbe4e-365">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-365">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="cbe4e-366">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-366">**FLOAT**</span></span> | <span data-ttu-id="cbe4e-367">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-367">**VT\_R4**</span></span> | <span data-ttu-id="cbe4e-368">от 0 до 1,0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-368">0–1.0</span></span> | <span data-ttu-id="cbe4e-369">0,9</span><span class="sxs-lookup"><span data-stu-id="cbe4e-369">0.9</span></span>     |



 

<span data-ttu-id="cbe4e-370">Уровень 1,0 обеспечивает сжатие с математическим коэффициентом потери данных.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-370">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="cbe4e-371">Уровень 0,0 является самым низким значением качества.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-371">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="cbe4e-372">интерлеаведалфа</span><span class="sxs-lookup"><span data-stu-id="cbe4e-372">InterleavedAlpha</span></span>

<span data-ttu-id="cbe4e-373">Указывает, кодировать альфа-или плоскую альфа-канал с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-373">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="cbe4e-374">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-374">Data type</span></span>         | <span data-ttu-id="cbe4e-375">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-375">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-376">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-376">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cbe4e-377">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-377">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-378">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-378">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-379">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-379">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="cbe4e-380">**Вариант \_ TRUE**: альфа-канал с чередованием.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-380">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="cbe4e-381">Сведения о альфа-канале кодируются как дополнительный канал с чередованием, без корреляции с каналами содержимого изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-381">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="cbe4e-382">Этот режим удобен для декодирования альфа-канала одновременно с изображением при потоковой передаче изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-382">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="cbe4e-383">ВАРИАНТ \_ false: плоский альфа.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-383">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="cbe4e-384">Плоский альфа-канал кодируется как отдельное изображение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-384">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="cbe4e-385">Данные изображения и альфа-канал декодированы независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-385">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="cbe4e-386">При необходимости можно задать уровень качества альфа-канала, задав свойство [алфакуалити](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-386">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="cbe4e-387">Альфа-канал с чередованием поддерживается только для определенных форматов пикселей RGB.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-387">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="cbe4e-388">Плоская альфа-версия поддерживается для любого формата изображения, определяющего альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-388">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="cbe4e-389">Lossless</span><span class="sxs-lookup"><span data-stu-id="cbe4e-389">Lossless</span></span>

<span data-ttu-id="cbe4e-390">Включает сжатие потерь.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-390">Enables losses compression.</span></span>



| <span data-ttu-id="cbe4e-391">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-391">Data type</span></span>         | <span data-ttu-id="cbe4e-392">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-392">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-393">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-393">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="cbe4e-394">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-394">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-395">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-395">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-396">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="cbe4e-396">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="cbe4e-397">Если значение является **вариантным \_ true**, кодировщик использует сжатие без потерь.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-397">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="cbe4e-398">Если задано **\_ значение true**, это свойство переопределяет свойство [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-398">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="cbe4e-399">Перекрытие</span><span class="sxs-lookup"><span data-stu-id="cbe4e-399">Overlap</span></span>

<span data-ttu-id="cbe4e-400">Задает уровень фильтрации перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-400">Sets the level of overlap filtering.</span></span> <span data-ttu-id="cbe4e-401">При фильтрации наложения коэффициенты преобразования применяются для границ блока и макроблокк.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-401">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="cbe4e-402">Это может сократить количество блокирующих артефактов.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-402">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="cbe4e-403">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-403">Data type</span></span> | <span data-ttu-id="cbe4e-404">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-404">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-405">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-405">Range</span></span> | <span data-ttu-id="cbe4e-406">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-406">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cbe4e-407">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-407">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-408">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-408">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-409">0 – 4</span><span class="sxs-lookup"><span data-stu-id="cbe4e-409">0–4</span></span>   | <span data-ttu-id="cbe4e-410">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-410">1</span></span>       |



 



| <span data-ttu-id="cbe4e-411">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-411">Value</span></span> | <span data-ttu-id="cbe4e-412">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-412">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="cbe4e-413">0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-413">0</span></span>     | <span data-ttu-id="cbe4e-414">Без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-414">No overlap.</span></span>                                   |
| <span data-ttu-id="cbe4e-415">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-415">1</span></span>     | <span data-ttu-id="cbe4e-416">Один уровень перекрытия, мягкое мозаичное разбиение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-416">One level of overlap, soft tiling.</span></span> <span data-ttu-id="cbe4e-417">(по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-417">(Default.)</span></span> |
| <span data-ttu-id="cbe4e-418">2</span><span class="sxs-lookup"><span data-stu-id="cbe4e-418">2</span></span>     | <span data-ttu-id="cbe4e-419">Два уровня перекрытия, мягкое мозаичное разбиение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-419">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="cbe4e-420">3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-420">3</span></span>     | <span data-ttu-id="cbe4e-421">Один уровень перекрытия, жесткое разбиение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-421">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="cbe4e-422">4</span><span class="sxs-lookup"><span data-stu-id="cbe4e-422">4</span></span>     | <span data-ttu-id="cbe4e-423">Два уровня перекрытия, жесткое разбиение.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-423">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="cbe4e-424">Определения:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-424">Definitions:</span></span>

-   <span data-ttu-id="cbe4e-425">Один уровень перекрытия: закодированные значения для блоков 4x4 изменяются на основе соседних блоков.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-425">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="cbe4e-426">Два уровня перекрытия: применяется первый уровень перекрытия.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-426">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="cbe4e-427">Кроме того, закодированные значения 16x16 макроблоккс изменяются на основе соседних макроблоккс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-427">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="cbe4e-428">Мягкое разбиение: Фильтрация наложения применяется к границам плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-428">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="cbe4e-429">Жесткое разбиение: Фильтрация наложения не применяется к границам плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-429">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="cbe4e-430">Сложные плитки могут представлять некоторые визуальные артефакты, а также границы плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-430">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="cbe4e-431">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-431">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="cbe4e-432">прогрессивемоде</span><span class="sxs-lookup"><span data-stu-id="cbe4e-432">ProgressiveMode</span></span>

<span data-ttu-id="cbe4e-433">Включает или отключает прогрессивную кодировку.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-433">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="cbe4e-434">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-434">Data type</span></span>         | <span data-ttu-id="cbe4e-435">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-435">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-436">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-436">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cbe4e-437">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-437">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-438">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-438">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-439">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-439">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="cbe4e-440">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-440">Value</span></span>              | <span data-ttu-id="cbe4e-441">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-441">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="cbe4e-442">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-442">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="cbe4e-443">Последовательный режим (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-443">Sequential mode (default).</span></span> |
| <span data-ttu-id="cbe4e-444">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-444">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="cbe4e-445">Прогрессивный режим.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-445">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="cbe4e-446">Качество</span><span class="sxs-lookup"><span data-stu-id="cbe4e-446">Quality</span></span>

<span data-ttu-id="cbe4e-447">Задает качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-447">Sets the compression quality.</span></span>



| <span data-ttu-id="cbe4e-448">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-448">Data type</span></span> | <span data-ttu-id="cbe4e-449">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-449">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-450">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-450">Range</span></span> | <span data-ttu-id="cbe4e-451">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-451">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="cbe4e-452">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-452">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-453">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-453">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-454">1 – 255</span><span class="sxs-lookup"><span data-stu-id="cbe4e-454">1–255</span></span> | <span data-ttu-id="cbe4e-455">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-455">1</span></span>       |



 

<span data-ttu-id="cbe4e-456">Значение 1 означает режим без потерь.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-456">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="cbe4e-457">Увеличение значений приводит к увеличению коэффициента сжатия и более низкому качеству изображения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-457">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="cbe4e-458">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-458">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="cbe4e-459">стреамонли</span><span class="sxs-lookup"><span data-stu-id="cbe4e-459">StreamOnly</span></span>

<span data-ttu-id="cbe4e-460">Включает или отключает режим "только потоковая передача".</span><span class="sxs-lookup"><span data-stu-id="cbe4e-460">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="cbe4e-461">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-461">Data type</span></span>         | <span data-ttu-id="cbe4e-462">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-462">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-463">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-463">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cbe4e-464">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-464">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-465">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-465">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-466">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-466">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="cbe4e-467">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-467">Value</span></span>              | <span data-ttu-id="cbe4e-468">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-468">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-469">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-469">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="cbe4e-470">Кодировщик выводит поток необработанных изображений без метаданных.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-470">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="cbe4e-471">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-471">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="cbe4e-472">Кодировщик выводит формат контейнера (поток изображений и метаданные).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-472">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="cbe4e-473">Подвыборка</span><span class="sxs-lookup"><span data-stu-id="cbe4e-473">Subsampling</span></span>

<span data-ttu-id="cbe4e-474">Задает подвыборку чрома.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-474">Sets the chroma subsampling.</span></span> <span data-ttu-id="cbe4e-475">Это свойство применяется только к изображениям RGB.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-475">This property applies only to RGB images.</span></span>



| <span data-ttu-id="cbe4e-476">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-476">Data type</span></span> | <span data-ttu-id="cbe4e-477">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-477">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-478">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-478">Range</span></span> | <span data-ttu-id="cbe4e-479">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-479">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="cbe4e-480">**учар**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-480">**UCHAR**</span></span> | <span data-ttu-id="cbe4e-481">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-481">**VT\_UI1**</span></span> | <span data-ttu-id="cbe4e-482">0 – 3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-482">0–3</span></span>   | <span data-ttu-id="cbe4e-483">3, если [имажекуалити](#imagequality) > 0,8; в противном случае 1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-483">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbe4e-484">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-484">Value</span></span></th>
<th><span data-ttu-id="cbe4e-485">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe4e-485">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbe4e-486">3</span><span class="sxs-lookup"><span data-stu-id="cbe4e-486">3</span></span></td>
<td><span data-ttu-id="cbe4e-487">Кодировка 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-487">4:4:4 encoding.</span></span> <span data-ttu-id="cbe4e-488">Сохраняет полное разрешение чрома.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-488">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-489">2</span><span class="sxs-lookup"><span data-stu-id="cbe4e-489">2</span></span></td>
<td><span data-ttu-id="cbe4e-490">Кодировка 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-490">4:2:2 encoding.</span></span> <span data-ttu-id="cbe4e-491">Разрешение чрома — 1/2 для разрешения освещенности.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-491">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbe4e-492">1</span><span class="sxs-lookup"><span data-stu-id="cbe4e-492">1</span></span></td>
<td><span data-ttu-id="cbe4e-493">Кодировка 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-493">4:2:0 encoding.</span></span> <span data-ttu-id="cbe4e-494">Разрешение чрома — 1/4 для разрешения освещенности.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-494">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-495">0</span><span class="sxs-lookup"><span data-stu-id="cbe4e-495">0</span></span></td>
<td><span data-ttu-id="cbe4e-496">Кодирование 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-496">4:0:0 encoding.</span></span> <span data-ttu-id="cbe4e-497">Отменяет все значения чрома и сохраняет только светимость.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-497">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="cbe4e-498">Этот режим не рекомендуется, поскольку кодек использует немного измененное определение светимости для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-498">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="cbe4e-499">Вместо этого лучше преобразовать изображение в монохромную перед кодированием.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-499">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cbe4e-500">4:2:2 и 4:2:0 сохраняют сведения о освещенности за счет сведений о цвете.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-500">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="cbe4e-501">Если задать это свойство, также установите для [усекодекоптионс](#usecodecoptions) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-501">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="cbe4e-502">усекодекоптионс</span><span class="sxs-lookup"><span data-stu-id="cbe4e-502">UseCodecOptions</span></span>

<span data-ttu-id="cbe4e-503">Указывает, следует ли использовать свойства [Quality](#image-quality-settings), [перекрытия](#overlap)и [подвыборки](#subsampling) вместо универсального свойства [имажекуалити](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-503">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="cbe4e-504">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-504">Data type</span></span>         | <span data-ttu-id="cbe4e-505">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-505">VARTYPE</span></span>      | <span data-ttu-id="cbe4e-506">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-506">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="cbe4e-507">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-507">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-508">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-508">**VT\_BOOL**</span></span> | <span data-ttu-id="cbe4e-509">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-509">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="cbe4e-510">вертикалтилеслицес</span><span class="sxs-lookup"><span data-stu-id="cbe4e-510">VerticalTileSlices</span></span>

<span data-ttu-id="cbe4e-511">Задает количество горизонтальных плиток.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-511">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="cbe4e-512">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cbe4e-512">Data type</span></span>  | <span data-ttu-id="cbe4e-513">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-513">VARTYPE</span></span>     | <span data-ttu-id="cbe4e-514">Диапазон</span><span class="sxs-lookup"><span data-stu-id="cbe4e-514">Range</span></span>  | <span data-ttu-id="cbe4e-515">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cbe4e-515">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="cbe4e-516">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-516">**USHORT**</span></span> | <span data-ttu-id="cbe4e-517">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-517">**VT\_UI2**</span></span> | <span data-ttu-id="cbe4e-518">0 — 4095</span><span class="sxs-lookup"><span data-stu-id="cbe4e-518">0–4095</span></span> | <span data-ttu-id="cbe4e-519">(высота изображения – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="cbe4e-519">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="cbe4e-520">Значение — это число вертикальных подразделений; то есть число вертикальных плиток — 1.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-520">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="cbe4e-521">Поддерживаемые форматы цвета</span><span class="sxs-lookup"><span data-stu-id="cbe4e-521">Supported Color Formats</span></span>

<span data-ttu-id="cbe4e-522">Дополнительные сведения об этих форматах см. в разделе [собственные форматы пикселей](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-522">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="cbe4e-523">**Форматы целых чисел RGB**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-523">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="cbe4e-524">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="cbe4e-524">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="cbe4e-525">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="cbe4e-525">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="cbe4e-526">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="cbe4e-526">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="cbe4e-527">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="cbe4e-527">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="cbe4e-528">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="cbe4e-528">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="cbe4e-529">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="cbe4e-529">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="cbe4e-530">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="cbe4e-530">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="cbe4e-531">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="cbe4e-531">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="cbe4e-532">**Форматы RGB с фиксированной запятой**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-532">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="cbe4e-533">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-533">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-534">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-534">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-535">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-535">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-536">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-536">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-537">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-537">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="cbe4e-538">**Форматы RGB с плавающей запятой**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-538">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="cbe4e-539">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="cbe4e-539">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="cbe4e-540">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="cbe4e-540">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="cbe4e-541">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="cbe4e-541">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="cbe4e-542">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-542">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-543">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="cbe4e-543">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="cbe4e-544">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="cbe4e-544">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="cbe4e-545">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="cbe4e-545">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="cbe4e-546">**Форматы в градациях серого**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-546">**Grayscale formats**</span></span>
    -   <span data-ttu-id="cbe4e-547">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="cbe4e-547">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="cbe4e-548">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="cbe4e-548">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="cbe4e-549">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-549">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-550">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="cbe4e-550">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="cbe4e-551">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="cbe4e-551">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="cbe4e-552">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="cbe4e-552">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="cbe4e-553">**Упакованные форматы**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-553">**Packed formats**</span></span>
    -   <span data-ttu-id="cbe4e-554">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="cbe4e-554">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="cbe4e-555">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="cbe4e-555">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="cbe4e-556">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="cbe4e-556">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="cbe4e-557">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-557">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="cbe4e-558">**Форматы CMYK**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-558">**CMYK formats**</span></span>
    -   <span data-ttu-id="cbe4e-559">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-559">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="cbe4e-560">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="cbe4e-560">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="cbe4e-561">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-561">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="cbe4e-562">**Форматы N-Channel**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-562">**N-channel formats**</span></span>
    -   <span data-ttu-id="cbe4e-563">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-563">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="cbe4e-564">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-564">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="cbe4e-565">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-565">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="cbe4e-566">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-566">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="cbe4e-567">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-567">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="cbe4e-568">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-568">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-569">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-569">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-570">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-570">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-571">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-571">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-572">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-572">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-573">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-573">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-574">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-574">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="cbe4e-575">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-575">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="cbe4e-576">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-576">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="cbe4e-577">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-577">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="cbe4e-578">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="cbe4e-578">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="cbe4e-579">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-579">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-580">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-580">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-581">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-581">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-582">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-582">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-583">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-583">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="cbe4e-584">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="cbe4e-584">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
