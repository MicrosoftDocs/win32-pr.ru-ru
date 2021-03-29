---
title: Буферы потока
description: Буферы потока
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Мультимедиа Windows, буферы потоков
- мультимедиа, буферы потоков
- мультимедийные аудио, буферы потоков
- звук, буферы потоков
- Цифровой интерфейс музыкальных инструментов (MIDI), буферы потоков
- MIDI (цифровой интерфейс музыкального инструмента), буферы потоков
- буферы потоков, сведения
- Структура МИДИХДР
- Структура МИДИЕВЕНТ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790164"
---
# <a name="stream-buffers"></a><span data-ttu-id="00989-112">Буферы потока</span><span class="sxs-lookup"><span data-stu-id="00989-112">Stream Buffers</span></span>

<span data-ttu-id="00989-113">Приложения могут использовать буферы потоков для отправки потоков событий MIDI на устройство.</span><span class="sxs-lookup"><span data-stu-id="00989-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="00989-114">Каждый буфер потока — это блок памяти, на который указывает структура [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="00989-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="00989-115">Этот блок памяти содержит данные для одного или нескольких событий MIDI, каждое из которых определяется структурой [**мидиевент**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="00989-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="00989-116">Приложение управляет буфером путем вызова функций обработки потока, таких как [**мидистреамопен**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)и [**мидистреамклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="00989-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="00989-117">Формат буфера потока</span><span class="sxs-lookup"><span data-stu-id="00989-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="00989-118">Сведения о времени</span><span class="sxs-lookup"><span data-stu-id="00989-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="00989-119">Типы событий MIDI</span><span class="sxs-lookup"><span data-stu-id="00989-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="00989-120">Потоки MIDI</span><span class="sxs-lookup"><span data-stu-id="00989-120">MIDI Streams</span></span>](midi-streams.md)

 

 