---
description: Запись звука
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Запись звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342015"
---
# <a name="audio-capture"></a><span data-ttu-id="64d39-103">Запись звука</span><span class="sxs-lookup"><span data-stu-id="64d39-103">Audio Capture</span></span>

<span data-ttu-id="64d39-104">Приложение может использовать DirectShow для записи звуковых данных с микрофонов, проигрывателей лент и других устройств с помощью входов на звуковой карте.</span><span class="sxs-lookup"><span data-stu-id="64d39-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="64d39-105">Типичные сценарии включают:</span><span class="sxs-lookup"><span data-stu-id="64d39-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="64d39-106">Запись речевого сопровождения VoiceOver для последующего дуббинг в потоке видео.</span><span class="sxs-lookup"><span data-stu-id="64d39-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="64d39-107">Преобразование устаревшего аналогового звукового содержимого в цифровой формат.</span><span class="sxs-lookup"><span data-stu-id="64d39-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="64d39-108">Запись голоса или музыки для передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="64d39-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="64d39-109">У конечных пользователей есть несколько вариантов записи звука с звуковой платы на жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="64d39-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="64d39-110">Большинство карт предоставляют приложениям для смешивания звуковых входов и записи.</span><span class="sxs-lookup"><span data-stu-id="64d39-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="64d39-111">Windows предоставляет средство записи звука, простое служебное приложение для записи с микрофона.</span><span class="sxs-lookup"><span data-stu-id="64d39-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="64d39-112">Кодировщик Windows Media можно встроить в приложение DirectShow как [объект мультимедиа DirectX](directx-media-objects.md) (DMO).</span><span class="sxs-lookup"><span data-stu-id="64d39-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="64d39-113">В этом разделе описывается интеграция функций аудиозаписи в свое приложение с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="64d39-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="64d39-114">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="64d39-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="64d39-115">О фильтре записи звука</span><span class="sxs-lookup"><span data-stu-id="64d39-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="64d39-116">Выбор устройства записи</span><span class="sxs-lookup"><span data-stu-id="64d39-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="64d39-117">Создание графика записи звука</span><span class="sxs-lookup"><span data-stu-id="64d39-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="64d39-118">Создание графика аудиозаписи с предварительной версией</span><span class="sxs-lookup"><span data-stu-id="64d39-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="64d39-119">Настройка свойств записи звука</span><span class="sxs-lookup"><span data-stu-id="64d39-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="64d39-120">См. также</span><span class="sxs-lookup"><span data-stu-id="64d39-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d39-121">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="64d39-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



