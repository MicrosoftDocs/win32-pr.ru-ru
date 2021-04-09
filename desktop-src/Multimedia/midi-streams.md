---
title: Потоки MIDI
description: Потоки MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Цифровой интерфейс MIDI, потоки
- MIDI (цифровой интерфейс музыкального инструмента), потоки
- буферы потоков, потоки MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133830"
---
# <a name="midi-streams"></a><span data-ttu-id="db69d-106">Потоки MIDI</span><span class="sxs-lookup"><span data-stu-id="db69d-106">MIDI Streams</span></span>

<span data-ttu-id="db69d-107">События MIDI возникают в контексте потока данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="db69d-108">Хотя приложение может использовать несколько потоков для определения музыкальных данных, средство сопоставления MIDI не распознает несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="db69d-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="db69d-109">Большинство приложений, использующих потоки, используют один поток MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="db69d-110">Следующие функции работают с потоками.</span><span class="sxs-lookup"><span data-stu-id="db69d-110">The following functions work with streams.</span></span>



| <span data-ttu-id="db69d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="db69d-111">Value</span></span>                                            | <span data-ttu-id="db69d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="db69d-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="db69d-113">**мидистреамклосе**</span><span class="sxs-lookup"><span data-stu-id="db69d-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="db69d-114">Закрывает поток MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="db69d-115">**мидистреамопен**</span><span class="sxs-lookup"><span data-stu-id="db69d-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="db69d-116">Открывает поток MIDI и получает маркер.</span><span class="sxs-lookup"><span data-stu-id="db69d-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="db69d-117">**мидистреамаут**</span><span class="sxs-lookup"><span data-stu-id="db69d-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="db69d-118">Воспроизводит поток (буфер) данных MIDI на устройстве вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="db69d-119">**мидистреампаусе**</span><span class="sxs-lookup"><span data-stu-id="db69d-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="db69d-120">Приостанавливает воспроизведение указанного потока MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="db69d-121">**мидистреампоситион**</span><span class="sxs-lookup"><span data-stu-id="db69d-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="db69d-122">Возвращает текущую точку в потоке MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="db69d-123">**мидистреампроперти**</span><span class="sxs-lookup"><span data-stu-id="db69d-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="db69d-124">Задает и получает свойства потока.</span><span class="sxs-lookup"><span data-stu-id="db69d-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="db69d-125">**мидистреамрестарт**</span><span class="sxs-lookup"><span data-stu-id="db69d-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="db69d-126">Перезапускает воспроизведение приостановленного потока MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="db69d-127">**мидистреамстоп**</span><span class="sxs-lookup"><span data-stu-id="db69d-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="db69d-128">Отключает все заметки на всех каналах MIDI для указанного потока MIDI.</span><span class="sxs-lookup"><span data-stu-id="db69d-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 