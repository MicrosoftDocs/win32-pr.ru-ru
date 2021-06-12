---
title: Узнайте о DirectShow в пакете SDK для Windows Media Format 11 — высокоуровневой, модульной, расширяемой и потоковой передачи данных для платформы Windows.
description: О DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011297"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="4b829-107">О программе DirectShow (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="4b829-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4b829-108">DirectShow — Это высокоуровневая, Модульная и расширяемая архитектура потоковой передачи данных для платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="4b829-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="4b829-109">Он предоставляет базовые программные компоненты и API-интерфейсы для широкого спектра цифровых аудио-и видеоприложений на рынке.</span><span class="sxs-lookup"><span data-stu-id="4b829-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="4b829-110">DirectShow доступна в составе пакета средств разработки программного обеспечения Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="4b829-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="4b829-111">Дополнительные сведения о DirectShow см. в разделе пакет SDK для платформы Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4b829-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="4b829-112">В DirectShow все компоненты потоковой передачи данных называются *фильтрами*.</span><span class="sxs-lookup"><span data-stu-id="4b829-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="4b829-113">Фильтр может представлять устройство, программный кодировщик или декодер, модуль подготовки звука или видео или любую возможность обработки звуковых видео.</span><span class="sxs-lookup"><span data-stu-id="4b829-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="4b829-114">Чтобы позволить приложениям на основе DirectShow читать и записывать содержимое формата Windows Media, включая содержимое, защищенное цифровыми Rights Management (DRM), корпорация Майкрософт предоставляет два фильтра, которые инкапсулируют части пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4b829-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="4b829-115">Это [средство чтения WM ASF](wm-asf-reader-filter.md) и [модуль записи WM ASF](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4b829-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="4b829-116">Эти фильтры и интерфейсы, которые они предоставляют, вместе называются компонентами КАСФ после библиотеки DLL, в которой они упакованы.</span><span class="sxs-lookup"><span data-stu-id="4b829-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="4b829-117">(Q означает Quartz, то есть раннее кодовое имя для DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="4b829-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="4b829-118">Использование кодеков Windows Media Audio и Video 9 с помощью компонентов DirectShow КАСФ требует наличия Microsoft Windows Millennium Edition или более поздней версии или DirectX 8,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4b829-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="4b829-119">На следующей схеме показан граф фильтра DirectShow для воспроизведения видеофайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4b829-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Граф воспроизведения видео Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="4b829-121">[Модуль чтения WM ASF](wm-asf-reader-filter.md) — это компонент касф, декодеры — это компоненты пакета SDK для Windows Media Format, размещенные в фильтре оболочки DMO (компонент касф), а модули подготовки отчетов — компоненты DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4b829-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




