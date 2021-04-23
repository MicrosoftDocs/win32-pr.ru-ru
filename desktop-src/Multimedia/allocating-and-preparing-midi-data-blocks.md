---
title: Выделение и подготовка блоков данных MIDI
description: Выделение и подготовка блоков данных MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), выделение блоков данных
- MIDI (цифровой интерфейс музыкального инструмента), выделение блоков данных
- Службы MIDI, выделение блоков данных
- Выделение блоков данных MIDI
- Цифровой интерфейс MIDI, подготовка блоков данных
- MIDI (цифровой интерфейс музыкального инструмента), подготовка блоков данных
- Службы MIDI, подготовка блоков данных
- подготовка блоков данных MIDI
- Цифровой интерфейс MIDI, блоки данных
- MIDI (цифровой интерфейс музыкального инструмента), блоки данных
- Службы MIDI, блоки данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672281"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="ac3a0-114">Выделение и подготовка блоков данных MIDI</span><span class="sxs-lookup"><span data-stu-id="ac3a0-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="ac3a0-115">Для функций [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**мидиинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)и [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) требуется, чтобы приложения выделили блоки данных для передачи в драйверы устройств для воспроизведения или записи.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="ac3a0-116">Каждая из этих функций использует структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) для описания своего блока данных.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="ac3a0-117">Прежде чем использовать одну из этих функций для передачи блока данных в драйвер устройства, необходимо выделить память для буфера и структуру заголовка, описывающую блок данных.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="ac3a0-118">Windows предоставляет следующие функции для подготовки и очистки блоков данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="ac3a0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ac3a0-119">Value</span></span>                                                    | <span data-ttu-id="ac3a0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ac3a0-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ac3a0-121">**мидиинпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="ac3a0-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="ac3a0-122">Подготавливает блок входных данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="ac3a0-123">**мидиинунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="ac3a0-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="ac3a0-124">Очищает подготовку блока входных данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="ac3a0-125">**мидиаутпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="ac3a0-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="ac3a0-126">Подготавливает блок выходных данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="ac3a0-127">**мидиаутунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="ac3a0-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="ac3a0-128">Очищает подготовку блока выходных данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="ac3a0-129">Перед передачей блока данных MIDI в драйвер устройства необходимо подготовить буфер, передав его в функцию [**мидиинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) или [**мидиаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) .</span><span class="sxs-lookup"><span data-stu-id="ac3a0-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="ac3a0-130">Когда драйвер устройства завершает работу с буфером и возвращает его, необходимо очистить эту подготовку, передав буфер в функцию [**мидиинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) или [**мидиаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) , прежде чем можно будет освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="ac3a0-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac3a0-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ac3a0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac3a0-132">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="ac3a0-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 