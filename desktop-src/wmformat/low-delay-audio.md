---
title: Low-Delay звук
description: Low-Delay звук
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, аудио с низкой задержкой
- Windows Media Format SDK, поддержка аудио
- кодеки, низкие задержки
- кодеки, поддержка аудио
- низкое задержку звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691370"
---
# <a name="low-delay-audio"></a><span data-ttu-id="e8091-108">Low-Delay звук</span><span class="sxs-lookup"><span data-stu-id="e8091-108">Low-Delay Audio</span></span>

<span data-ttu-id="e8091-109">Низкое задержка — это режим кодирования, который создает сжатый звук с меньшим значением параметра буферного окна, чем другие режимы.</span><span class="sxs-lookup"><span data-stu-id="e8091-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="e8091-110">Это полезно для потоков, которые необходимо быстро переключать во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e8091-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="e8091-111">Типичный сценарий для этой функции — это потоковая презентация, которая включает возможность произвольного переключения содержимого, например изменение канала телевизора.</span><span class="sxs-lookup"><span data-stu-id="e8091-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="e8091-112">При использовании аудио формата с низкой задержкой задержка для переключения содержимого значительно уменьшилась по сравнению с другими звуковыми форматами.</span><span class="sxs-lookup"><span data-stu-id="e8091-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="e8091-113">Задержка также сокращается для вещания в реальном времени при использовании форматов с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="e8091-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="e8091-114">Эта функция поддерживается кодеками Windows Media Audio 9,1 и Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="e8091-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="e8091-115">Форматы с низкой задержкой доступны только для кодирования с постоянной скоростью потока (один и два прохода).</span><span class="sxs-lookup"><span data-stu-id="e8091-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8091-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e8091-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8091-117">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="e8091-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




