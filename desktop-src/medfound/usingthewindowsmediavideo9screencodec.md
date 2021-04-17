---
description: Использование экранного видеокодека Windows Media видео 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Экранный кодек Windows Media видео 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684734"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="8cea4-103">Экранный кодек Windows Media видео 9 (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8cea4-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8cea4-104">Экранный кодек Windows Media Video 9 оптимизирован для сжатия *видео приложения*, который состоит из последовательных снимков экрана для отображения на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8cea4-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="8cea4-105">Кодек использует стандартную простоту изображения (относительно небольшое число цветов, множество прямых линий и т. д.) и относительный недостаток движения для достижения очень высокого коэффициента сжатия.</span><span class="sxs-lookup"><span data-stu-id="8cea4-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="8cea4-106">Недостаток этой оптимизации заключается в том, что видео, не соответствующее ожидаемым характеристикам видео приложения, может быть сложно сжимать с приемлемым уровнем качества.</span><span class="sxs-lookup"><span data-stu-id="8cea4-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="8cea4-107">Экранный кодировщик Windows Media Video 9 определяется идентификатором класса CLSID \_ CMSSEncMediaObject2, а декодер определяет идентификатор класса CLSID \_ кмссдекмедиаобжект.</span><span class="sxs-lookup"><span data-stu-id="8cea4-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="8cea4-108">Значение FOURCC для типов мультимедиа, использующих этот кодек, — "MSS2".</span><span class="sxs-lookup"><span data-stu-id="8cea4-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="8cea4-109">Настройка кодировщика</span><span class="sxs-lookup"><span data-stu-id="8cea4-109">Configuring the Encoder</span></span>

<span data-ttu-id="8cea4-110">Кодировщик экранного кодека Windows Media видео 9 настраивается так же, как и стандартный видеодекодер.</span><span class="sxs-lookup"><span data-stu-id="8cea4-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="8cea4-111">Кодировщик экрана поддерживает только однопроходную кодировку.</span><span class="sxs-lookup"><span data-stu-id="8cea4-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="8cea4-112">Свойство [мфпкэй \_ пассесусед](mfpkey-passesusedproperty.md) можно задать равным 2 и обработать входные данные дважды без ошибок, но это не дает никаких преимуществ.</span><span class="sxs-lookup"><span data-stu-id="8cea4-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="8cea4-113">Это известная проблема, которую можно исправить в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="8cea4-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="8cea4-114">Получение лучших результатов</span><span class="sxs-lookup"><span data-stu-id="8cea4-114">Getting the Best Results</span></span>

<span data-ttu-id="8cea4-115">Если вы обнаружите, что требуемое качество содержимого для захвата экрана требует более высоких разрядов, чем вы можете использовать для вашего сценария доставки, вы можете воспользоваться следующими методами, чтобы повысить эффективность кодека:</span><span class="sxs-lookup"><span data-stu-id="8cea4-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="8cea4-116">Используйте меньшее разрешение снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="8cea4-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="8cea4-117">При захвате большего разрешения экрана средство просмотра может запутаться с ненужными сведениями.</span><span class="sxs-lookup"><span data-stu-id="8cea4-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="8cea4-118">Используйте более низкую частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="8cea4-118">Use a slower frame rate.</span></span> <span data-ttu-id="8cea4-119">Снимки экрана часто могут быть эффективны при очень низких частоте кадров (иногда как минимум 4 или 5 кадров в секунду).</span><span class="sxs-lookup"><span data-stu-id="8cea4-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="8cea4-120">Используйте меньше изображений в снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="8cea4-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="8cea4-121">Экранный кодек Windows Media Video 9 оптимизирован для кодирования примитивов и текста Windows с высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="8cea4-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="8cea4-122">Обычно проблемы возникают из-за точечной графики, которая часто содержит тысячи отдельных цветов.</span><span class="sxs-lookup"><span data-stu-id="8cea4-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="8cea4-123">Чем меньше точечных рисунков на экране при захвате, тем лучше будут результаты.</span><span class="sxs-lookup"><span data-stu-id="8cea4-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="8cea4-124">Если не удается удалить графику из снимка экрана, существует несколько способов свести к сведению, что точечный рисунок имеет качество изображения:</span><span class="sxs-lookup"><span data-stu-id="8cea4-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="8cea4-125">Уменьшите размер рисунка.</span><span class="sxs-lookup"><span data-stu-id="8cea4-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="8cea4-126">Сократите число отдельных графических объектов, отображаемых на экране одновременно.</span><span class="sxs-lookup"><span data-stu-id="8cea4-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="8cea4-127">Уменьшите объем передвижения изображения.</span><span class="sxs-lookup"><span data-stu-id="8cea4-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="8cea4-128">Например, если изображение находится в окне, не задерживайте окно как можно более стационарным.</span><span class="sxs-lookup"><span data-stu-id="8cea4-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="8cea4-129">Старайтесь не перемещать указатель мыши над графикой или перетаскивать окна или другие элементы на изображении.</span><span class="sxs-lookup"><span data-stu-id="8cea4-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="8cea4-130">Декодирование</span><span class="sxs-lookup"><span data-stu-id="8cea4-130">Decoding</span></span>

<span data-ttu-id="8cea4-131">Не существует специальных требований для декодирования видео снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="8cea4-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="8cea4-132">Однако, как и в случае со всеми кодеками Windows Media Video 9, декодер записи экрана не может правильно распаковать закодированное содержимое без личных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="8cea4-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cea4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="8cea4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cea4-134">Настройка кодирования видео</span><span class="sxs-lookup"><span data-stu-id="8cea4-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="8cea4-135">Использование личных данных видеокодека</span><span class="sxs-lookup"><span data-stu-id="8cea4-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="8cea4-136">Кодировщик экрана Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="8cea4-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="8cea4-137">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="8cea4-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



