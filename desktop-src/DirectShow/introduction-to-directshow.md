---
description: Введение в DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Введение в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139887"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="3402f-103">Введение в DirectShow</span><span class="sxs-lookup"><span data-stu-id="3402f-103">Introduction to DirectShow</span></span>

<span data-ttu-id="3402f-104">Microsoft® DirectShow® — это архитектура для потоковой передачи мультимедиа на платформе Microsoft Windows®.</span><span class="sxs-lookup"><span data-stu-id="3402f-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="3402f-105">DirectShow обеспечивает высококачественный захват и воспроизведение мультимедийных потоков.</span><span class="sxs-lookup"><span data-stu-id="3402f-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="3402f-106">Он поддерживает разнообразные форматы, в том числе расширенный системный формат (ASF), группу экспертов по воспроизведению изображений (MPEG), Audio-Video с чередованием (AVI), MPEG Audio Layer-3 (MP3) и звуковые файлы WAV.</span><span class="sxs-lookup"><span data-stu-id="3402f-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="3402f-107">Он поддерживает захват из цифровых и аналоговых устройств на основе WDM (WDM) или видео для Windows.</span><span class="sxs-lookup"><span data-stu-id="3402f-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="3402f-108">Он автоматически обнаруживает и использует аппаратное ускорение видео и звука, если доступно, но также поддерживает системы без аппаратного ускорения.</span><span class="sxs-lookup"><span data-stu-id="3402f-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="3402f-109">DirectShow основана на модели COM.</span><span class="sxs-lookup"><span data-stu-id="3402f-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="3402f-110">Для написания приложения или компонента DirectShow необходимо иметь представление о программировании клиента COM.</span><span class="sxs-lookup"><span data-stu-id="3402f-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="3402f-111">Для большинства приложений не требуется реализовывать собственные COM-объекты.</span><span class="sxs-lookup"><span data-stu-id="3402f-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="3402f-112">DirectShow предоставляет необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="3402f-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="3402f-113">Однако, если требуется расширить DirectShow путем написания собственных компонентов, необходимо реализовать их как COM-объекты.</span><span class="sxs-lookup"><span data-stu-id="3402f-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="3402f-114">DirectShow разработана для C++.</span><span class="sxs-lookup"><span data-stu-id="3402f-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="3402f-115">Корпорация Майкрософт не предоставляет управляемый API для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3402f-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="3402f-116">DirectShow упрощает воспроизведение мультимедиа, преобразование формата и отслеживание задач.</span><span class="sxs-lookup"><span data-stu-id="3402f-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="3402f-117">В то же время он предоставляет доступ к базовой архитектуре управления потоком для приложений, которым требуются пользовательские решения.</span><span class="sxs-lookup"><span data-stu-id="3402f-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="3402f-118">Вы также можете создавать собственные компоненты DirectShow для поддержки новых форматов или пользовательских эффектов.</span><span class="sxs-lookup"><span data-stu-id="3402f-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="3402f-119">Примерами типов приложений, которые можно написать с помощью DirectShow, являются проигрыватели файлов, ТЕЛЕВИЗОРы и DVD-проигрыватели, приложения для редактирования видео, конвертеры формата файлов, приложения для захвата видео, кодировщики и декодеры, обработчики цифровых сигналов и многое другое.</span><span class="sxs-lookup"><span data-stu-id="3402f-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="3402f-120">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="3402f-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="3402f-121">Новые возможности DirectShow</span><span class="sxs-lookup"><span data-stu-id="3402f-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="3402f-122">Поддерживаемые форматы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="3402f-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="3402f-123">Вопросы и ответы по DirectShow</span><span class="sxs-lookup"><span data-stu-id="3402f-123">DirectShow FAQ</span></span>](directshow-faq.md)

## <a name="related-topics"></a><span data-ttu-id="3402f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3402f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3402f-125">Начало работы</span><span class="sxs-lookup"><span data-stu-id="3402f-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="3402f-126">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="3402f-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



