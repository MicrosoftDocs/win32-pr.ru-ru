---
description: High Definition (ДКСВА-HD) ускорение видео Microsoft DirectX — это API для обработки видео с аппаратным ускорением.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808092"
---
# <a name="dxva-hd"></a><span data-ttu-id="86883-103">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-103">DXVA-HD</span></span>

<span data-ttu-id="86883-104">High Definition (ДКСВА-HD) ускорение видео Microsoft DirectX — это API для обработки видео с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="86883-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="86883-105">ДКСВА-HD использует GPU для выполнения таких функций, как декомпозиция, композиция и преобразование цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="86883-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="86883-106">ДКСВА-HD аналогичен [дксваной обработке видео](dxva-video-processing.md) (ДКСВА-президент), но предлагает расширенные возможности и более простую модель обработки.</span><span class="sxs-lookup"><span data-stu-id="86883-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="86883-107">Предоставляя более гибкую модель композиции, ДКСВА-HD обеспечивает поддержку нового поколения HD оптических форматов и стандартов вещания.</span><span class="sxs-lookup"><span data-stu-id="86883-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="86883-108">API ДКСВА-HD требует наличия драйвера экрана WDDM, поддерживающего интерфейс драйвера устройства ДКСВА-HD (DDI) или программного процессора подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="86883-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="86883-109">Улучшения по сравнению с ДКСВА — вице-президент</span><span class="sxs-lookup"><span data-stu-id="86883-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="86883-110">См. также</span><span class="sxs-lookup"><span data-stu-id="86883-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="86883-111">Улучшения по сравнению с ДКСВА — вице-президент</span><span class="sxs-lookup"><span data-stu-id="86883-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="86883-112">ДКСВА-HD расширяет набор функций, предоставляемых ДКСВА-президента.</span><span class="sxs-lookup"><span data-stu-id="86883-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="86883-113">К усовершенствованиям относятся:</span><span class="sxs-lookup"><span data-stu-id="86883-113">Enhancements include:</span></span>

-   <span data-ttu-id="86883-114">Смешение RGB и YUV.</span><span class="sxs-lookup"><span data-stu-id="86883-114">RGB and YUV mixing.</span></span> <span data-ttu-id="86883-115">Любой поток может быть либо RGB, либо YUV.</span><span class="sxs-lookup"><span data-stu-id="86883-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="86883-116">Между основным потоком и подпотоками больше нет различий.</span><span class="sxs-lookup"><span data-stu-id="86883-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="86883-117">Разчередование нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="86883-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="86883-118">Любой поток может быть либо прогрессивным, либо чередованием.</span><span class="sxs-lookup"><span data-stu-id="86883-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="86883-119">Кроме того, ритмичность и частота кадров могут меняться от одного потока ввода к другому.</span><span class="sxs-lookup"><span data-stu-id="86883-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="86883-120">Цвета фона RGB.</span><span class="sxs-lookup"><span data-stu-id="86883-120">RGB background colors.</span></span> <span data-ttu-id="86883-121">Ранее поддерживались только цвета фона YUV.</span><span class="sxs-lookup"><span data-stu-id="86883-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="86883-122">Ключ яркости.</span><span class="sxs-lookup"><span data-stu-id="86883-122">Luma keying.</span></span> <span data-ttu-id="86883-123">Если ключ яркости включен, значения яркости, которые попадают в указанный диапазон, становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="86883-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="86883-124">Динамическое переключение между режимами с разчередованием.</span><span class="sxs-lookup"><span data-stu-id="86883-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="86883-125">ДКСВА-HD также определяет некоторые дополнительные функции, которые могут поддерживаться драйверами.</span><span class="sxs-lookup"><span data-stu-id="86883-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="86883-126">Однако приложения не должны рассчитывать, что все драйверы будут поддерживать эти функции.</span><span class="sxs-lookup"><span data-stu-id="86883-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="86883-127">К дополнительным функциям относятся:</span><span class="sxs-lookup"><span data-stu-id="86883-127">The advanced features include:</span></span>

-   <span data-ttu-id="86883-128">Обратный чересстрочности (например, 60i в 24p).</span><span class="sxs-lookup"><span data-stu-id="86883-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="86883-129">Преобразование ставок кадров (например, 24p в 120p).</span><span class="sxs-lookup"><span data-stu-id="86883-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="86883-130">Режимы заливки альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="86883-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="86883-131">Фильтрация шумов и расширения границы.</span><span class="sxs-lookup"><span data-stu-id="86883-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="86883-132">Анаморфик нелинейное масштабирование.</span><span class="sxs-lookup"><span data-stu-id="86883-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="86883-133">Расширенная Икбкр (Ксвикк).</span><span class="sxs-lookup"><span data-stu-id="86883-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="86883-134">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="86883-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="86883-135">Создание видеопроцессора ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="86883-136">Проверка поддерживаемых форматов ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="86883-137">Создание видеоподсистем ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="86883-138">Настройка состояний ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="86883-139">Выполнение ДКСВА-HD Блит</span><span class="sxs-lookup"><span data-stu-id="86883-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="86883-140">См. также</span><span class="sxs-lookup"><span data-stu-id="86883-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86883-141">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="86883-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="86883-142">Пример ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="86883-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



