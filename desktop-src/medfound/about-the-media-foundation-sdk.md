---
description: Microsoft Media Foundation — это платформа мультимедийных данных нового поколения для Windows, которая позволяет разработчикам, потребителям и поставщикам содержимого поддерживать новую волновую информацию о расширенном содержимом с повышенной надежностью, непревзойденным качеством и легкостью взаимодействия.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: О Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703431"
---
# <a name="about-media-foundation"></a><span data-ttu-id="a53e1-103">О Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-103">About Media Foundation</span></span>

<span data-ttu-id="a53e1-104">Microsoft Media Foundation — это платформа мультимедийных данных нового поколения для Windows, которая позволяет разработчикам, потребителям и поставщикам содержимого поддерживать новую волновую информацию о расширенном содержимом с повышенной надежностью, непревзойденным качеством и легкостью взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a53e1-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="a53e1-105">Для Media Foundation требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="a53e1-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="a53e1-106">Он использует объектную модель COM и требует C/C++.</span><span class="sxs-lookup"><span data-stu-id="a53e1-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="a53e1-107">Корпорация Майкрософт не предоставляет управляемый API для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53e1-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="a53e1-108">Media Foundation интерфейсы API являются частью [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a53e1-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a53e1-109">Чтобы разработать приложение Media Foundation, установите последнюю версию Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a53e1-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="a53e1-110">Качество звука и видео</span><span class="sxs-lookup"><span data-stu-id="a53e1-110">Audio and Video Quality</span></span>

<span data-ttu-id="a53e1-111">Media Foundation была разработана для удовлетворения проблем, возникающих в содержимом высокой четкости.</span><span class="sxs-lookup"><span data-stu-id="a53e1-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="a53e1-112">Улучшение качества звука и видео, сделанное на всей платформе, теперь позволяет обеспечить превосходную работу с содержимым высокой четкости нового поколения.</span><span class="sxs-lookup"><span data-stu-id="a53e1-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="a53e1-113">Ускорение видео DirectX (ДКСВА) 2,0 предлагает более эффективное ускорение видео по сравнению с ДКСВА 1,0, благодаря более надежному и упрощенному декодированию видео и расширенному использованию оборудования при обработке видео.</span><span class="sxs-lookup"><span data-stu-id="a53e1-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="a53e1-114">С помощью ДКСВА 2,0 Windows может работать с наиболее требовательным содержимым высокой четкости с высоким качеством и повышенной устойчивостью к сбоям.</span><span class="sxs-lookup"><span data-stu-id="a53e1-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="a53e1-115">Информация о цветовых пространствах сохраняется во время конвейера видео.</span><span class="sxs-lookup"><span data-stu-id="a53e1-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="a53e1-116">Пользователи могут получать видеоматериалы с полной точностью.</span><span class="sxs-lookup"><span data-stu-id="a53e1-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="a53e1-117">Сведения о цвете и чередующиеся изображения теперь передаются на оборудование для однопроходных композиций.</span><span class="sxs-lookup"><span data-stu-id="a53e1-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="a53e1-118">Сохранение сведений о цветовых пространствах также сокращает ненужные преобразования цветового пространства, что освобождает больше циклов для обработки ресурсоемких данных HD.</span><span class="sxs-lookup"><span data-stu-id="a53e1-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="a53e1-119">Улучшенный модуль подготовки видео (Евр) обеспечивает лучшую поддержку времени, улучшенную обработку видео и повышает устойчивость к сбоям.</span><span class="sxs-lookup"><span data-stu-id="a53e1-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="a53e1-120">Улучшена поддержка воспроизведения в полноэкранном режиме, и воспроизведение видео в окне режима было минимальным.</span><span class="sxs-lookup"><span data-stu-id="a53e1-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="a53e1-121">Media Foundation использует службу диспетчера классов мультимедиа (MMCSS), новую системную службу в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a53e1-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="a53e1-122">Служба MMCSS позволяет приложениям мультимедиа гарантировать, что их обработка с учетом времени получит приоритетный доступ к ресурсам ЦП.</span><span class="sxs-lookup"><span data-stu-id="a53e1-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="a53e1-123">Доступ к содержимому</span><span class="sxs-lookup"><span data-stu-id="a53e1-123">Content Access</span></span>

<span data-ttu-id="a53e1-124">Когда цифровые развлечения переходят в эпоху высокого определения и содержимое становится более переносимым и повсеместным, защита содержимого станет неотъемлемой частью цифровых мультимедийных продуктов.</span><span class="sxs-lookup"><span data-stu-id="a53e1-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="a53e1-125">Расширяемость Media Foundation гарантирует, что она сможет поддерживать эти тенденции.</span><span class="sxs-lookup"><span data-stu-id="a53e1-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="a53e1-126">Кроме того, Media Foundation расширяемость позволяет различным системам защиты содержимого взаимодействовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="a53e1-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="a53e1-127">О Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-127">About Media Foundation</span></span>

<span data-ttu-id="a53e1-128">В этом разделе содержатся общие сведения об API-интерфейсах Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53e1-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="a53e1-129">Подробные сведения о программировании можно найти в [Media Foundationном руководством по программированию](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="a53e1-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="a53e1-130">Section</span><span class="sxs-lookup"><span data-stu-id="a53e1-130">Section</span></span>                                                                              | <span data-ttu-id="a53e1-131">Описание</span><span class="sxs-lookup"><span data-stu-id="a53e1-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a53e1-132">Новые возможности для Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="a53e1-133">Описание новых функций в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53e1-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="a53e1-134">Заголовки и библиотеки Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="a53e1-135">Список файлов заголовков и библиотек, определяющих интерфейсы API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53e1-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="a53e1-136">Средства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="a53e1-137">Описание средств разработки, доступных для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53e1-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="a53e1-138">Media Foundation не входит в состав выпусков Windows 8 и N и KN.</span><span class="sxs-lookup"><span data-stu-id="a53e1-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="a53e1-139">Дополнительные сведения см. в [статье пакет дополнительных компонентов Microsoft Windows Media для версий N и kn всех выпусков Windows 8](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="a53e1-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a53e1-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a53e1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a53e1-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a53e1-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



