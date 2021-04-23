---
description: Обзор системы DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Обзор системы DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536593"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="5fbee-103">Обзор системы DirectShow</span><span class="sxs-lookup"><span data-stu-id="5fbee-103">DirectShow System Overview</span></span>

<span data-ttu-id="5fbee-104">**Задача мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="5fbee-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="5fbee-105">Работа с мультимедиа представляет ряд основных проблем:</span><span class="sxs-lookup"><span data-stu-id="5fbee-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="5fbee-106">Мультимедийные потоки содержат большие объемы данных, которые должны обрабатываться очень быстро.</span><span class="sxs-lookup"><span data-stu-id="5fbee-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="5fbee-107">Необходимо синхронизировать аудио и видео, чтобы они были запущены и остановлены одновременно и воспроизводились с одинаковой скоростью.</span><span class="sxs-lookup"><span data-stu-id="5fbee-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="5fbee-108">Данные могут поступать из многих источников, включая локальные файлы, компьютерные сети, телевизионные трансляции и видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="5fbee-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="5fbee-109">Данные поступают в различных форматах, таких как Audio-Video с чередованием (AVI), расширенный потоковый формат (ASF), Группа экспертов по воспроизведению изображений (MPEG) и цифровое видео (DV).</span><span class="sxs-lookup"><span data-stu-id="5fbee-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="5fbee-110">Программист не знает заранее, какие аппаратные устройства будут присутствовать в системе конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5fbee-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="5fbee-111">**Решение DirectShow**</span><span class="sxs-lookup"><span data-stu-id="5fbee-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="5fbee-112">DirectShow предназначена для решения каждой из этих задач.</span><span class="sxs-lookup"><span data-stu-id="5fbee-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="5fbee-113">Его основная цель проектирования — упростить задачу создания мультимедийных приложений на платформе Windows, изолируя приложения от сложных транспортов данных, аппаратных различий и синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5fbee-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="5fbee-114">Для достижения пропускной способности, необходимой для потоковой передачи видео и аудио, DirectShow использует Direct3D и DirectSound, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="5fbee-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="5fbee-115">Эти технологии эффективно отображают данные для звуковых и графических плат пользователя.</span><span class="sxs-lookup"><span data-stu-id="5fbee-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="5fbee-116">DirectShow синхронизирует воспроизведение, инкапсулируются данные мультимедиа в образцах с отметкой времени.</span><span class="sxs-lookup"><span data-stu-id="5fbee-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="5fbee-117">Для решения разнообразных источников, форматов и устройств, которые можно использовать, DirectShow использует модульную архитектуру, в которой приложение смешивается и соответствует различным программным компонентам, называемым *фильтрами*.</span><span class="sxs-lookup"><span data-stu-id="5fbee-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="5fbee-118">DirectShow предоставляет фильтры, поддерживающие запись и настройку устройств на основе WDM (WDM), а также фильтры, поддерживающие старые карты записи видео для Windows (VfW), и кодеки, написанные для интерфейсов диспетчера аудиосжатия (ACM) и диспетчера сжатия видео (ВКМ).</span><span class="sxs-lookup"><span data-stu-id="5fbee-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="5fbee-119">На следующей схеме показана связь между приложением, компонентами DirectShow и некоторыми аппаратными и программными компонентами, поддерживаемыми DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5fbee-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![Высокоуровневая архитектура](images/arch-oview2.png)

<span data-ttu-id="5fbee-121">Как показано здесь, фильтры DirectShow взаимодействуют с широким спектром устройств, а также управляют им, включая локальную файловую систему, ТЕЛЕВИЗИОНные тюнеры и видеокарты, кодеки VfW, видеомонитор (с помощью DirectDraw или GDI) и звуковую карту (с помощью DirectSound).</span><span class="sxs-lookup"><span data-stu-id="5fbee-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="5fbee-122">Таким же DirectShow изолирует приложение от многих сложностей этих устройств.</span><span class="sxs-lookup"><span data-stu-id="5fbee-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="5fbee-123">DirectShow также обеспечивает собственные фильтры сжатия и распаковки для определенных форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="5fbee-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fbee-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5fbee-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fbee-125">О DirectShow</span><span class="sxs-lookup"><span data-stu-id="5fbee-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



