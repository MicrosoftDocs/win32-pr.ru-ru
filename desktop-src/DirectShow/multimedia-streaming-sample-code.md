---
description: Пример кода для потоковой передачи мультимедиа
ms.assetid: 3fe2996b-b4de-40ad-bd02-d850a45f3a2c
title: Пример кода для потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2035e7d8038adeae19cd847801ec4c23e97485c6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351682"
---
# <a name="multimedia-streaming-sample-code"></a><span data-ttu-id="465c4-103">Пример кода для потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="465c4-103">Multimedia Streaming Sample Code</span></span>

> [!Note]  
> <span data-ttu-id="465c4-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="465c4-104">These APIs are deprecated.</span></span> <span data-ttu-id="465c4-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="465c4-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="465c4-106">В этой статье приведен пример кода, который реализует интерфейсы потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="465c4-106">This article provides sample code that implements the multimedia streaming interfaces.</span></span> <span data-ttu-id="465c4-107">В примере кода для потоковой передачи видео показано, как прочитать файл и преобразовать его в основную поверхность® Microsoft® DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="465c4-107">The video streaming sample code demonstrates how to read a file and render it to a primary Microsoft® DirectDraw® surface.</span></span> <span data-ttu-id="465c4-108">Для краткости этот код не содержит проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="465c4-108">For brevity, this code contains no error checking.</span></span>

<span data-ttu-id="465c4-109">Во втором образце кода показано, как использовать интерфейсы потоковой передачи аудио для потокового воспроизведения звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="465c4-109">The second code sample demonstrates how to use the audio streaming interfaces to stream audio data.</span></span>

<span data-ttu-id="465c4-110">Эта статья состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="465c4-110">This article contains the following sections.</span></span>

-   [<span data-ttu-id="465c4-111">Пример кода для потоковой передачи видео</span><span class="sxs-lookup"><span data-stu-id="465c4-111">Video Streaming Sample Code</span></span>](video-streaming-sample-code.md)
-   [<span data-ttu-id="465c4-112">Пример кода для потоковой передачи звука</span><span class="sxs-lookup"><span data-stu-id="465c4-112">Audio Streaming Sample Code</span></span>](audio-streaming-sample-code.md)

 

 



