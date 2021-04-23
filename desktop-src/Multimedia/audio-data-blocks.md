---
title: Звуковые блоки данных
description: Звуковые блоки данных
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- мультимедийные аудио, блоки данных
- звук, блоки данных
- звуковая волна, блоки данных
- блоки звуковых данных, сведения
- Структура ВАВЕХДР
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987396"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="0c663-108">Звуковые блоки данных</span><span class="sxs-lookup"><span data-stu-id="0c663-108">Audio Data Blocks</span></span>

<span data-ttu-id="0c663-109">Функции [**вавеинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) и [**вавеаутврите**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) нуждаются в том, чтобы приложения выделили блоки данных для передачи в драйверы устройств для записи или воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0c663-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="0c663-110">Обе эти функции используют структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) для описания своего блока данных.</span><span class="sxs-lookup"><span data-stu-id="0c663-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="0c663-111">Перед использованием одной из этих функций для передачи блока данных в драйвер устройства необходимо выделить память для блока данных и структуру заголовка, описывающую блок данных.</span><span class="sxs-lookup"><span data-stu-id="0c663-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="0c663-112">Заголовки можно подготавливать и подготавливать с помощью следующих функций.</span><span class="sxs-lookup"><span data-stu-id="0c663-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="0c663-113">Функция</span><span class="sxs-lookup"><span data-stu-id="0c663-113">Function</span></span>                                                 | <span data-ttu-id="0c663-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0c663-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0c663-115">**вавеинпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="0c663-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="0c663-116">Подготавливает блок входных данных звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="0c663-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="0c663-117">**вавеинунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="0c663-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="0c663-118">Очищает подготовку к блоку входных данных звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="0c663-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="0c663-119">**вавеаутпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="0c663-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="0c663-120">Подготавливает блок выходных данных волны-Audio.</span><span class="sxs-lookup"><span data-stu-id="0c663-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="0c663-121">**вавеаутунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="0c663-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="0c663-122">Очищает подготовку к выходному блоку выходных данных звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="0c663-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="0c663-123">Перед передачей блока звуковых данных в драйвер устройства необходимо подготовить блок данных, передав его в [**вавеинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) или [**вавеаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span><span class="sxs-lookup"><span data-stu-id="0c663-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="0c663-124">Когда драйвер устройства завершает работу с блоком данных и возвращает его, необходимо очистить эту подготовку, передав блок данных в [**вавеинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) или [**вавеаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) , прежде чем можно будет освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="0c663-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="0c663-125">Если входные и выходные данные аудио-сигнала недостаточны для появления в одном блоке данных, приложения должны постоянно предоставлять драйверы устройств блоками данных до завершения воспроизведения или записи.</span><span class="sxs-lookup"><span data-stu-id="0c663-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="0c663-126">Даже если используется один блок данных, приложение должно иметь возможность определить, завершена ли работа драйвера устройства с блоком данных, чтобы приложение могло освободить память, связанную с блоком данных и структурой заголовков.</span><span class="sxs-lookup"><span data-stu-id="0c663-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="0c663-127">Существует несколько способов определения завершения работы драйвера устройства с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="0c663-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="0c663-128">Указание функции обратного вызова для получения сообщения, отправленного драйвером после завершения работы с блоком данных</span><span class="sxs-lookup"><span data-stu-id="0c663-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="0c663-129">С помощью обратного вызова события</span><span class="sxs-lookup"><span data-stu-id="0c663-129">By using an event callback</span></span>
-   <span data-ttu-id="0c663-130">Указание окна или потока для получения сообщения, отправленного драйвером после завершения работы с блоком данных</span><span class="sxs-lookup"><span data-stu-id="0c663-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="0c663-131">Путем опроса бита ВХДР \_ done в члене **DwFlags** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , отправленной с каждым блоком данных</span><span class="sxs-lookup"><span data-stu-id="0c663-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="0c663-132">Если приложение не получает блок данных к драйверу устройства при необходимости, может воздержаться звуковой зазор при воспроизведении или потери входящей записанной информации.</span><span class="sxs-lookup"><span data-stu-id="0c663-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="0c663-133">Для этого требуется по крайней мере один блок данных с двойной буферизацией, в котором впереди драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="0c663-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="0c663-134">В следующих разделах описаны способы определения завершения работы драйвера устройства с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="0c663-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="0c663-135">Использование функции обратного вызова для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="0c663-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="0c663-136">Использование функции обратного вызова для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="0c663-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="0c663-137">Использование обратного вызова события для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="0c663-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="0c663-138">Использование окна или потока для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="0c663-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="0c663-139">Управление блоками данных путем опроса</span><span class="sxs-lookup"><span data-stu-id="0c663-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 