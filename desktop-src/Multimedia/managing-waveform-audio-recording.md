---
title: Управление записью Waveform-Audio
description: Управление записью Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- волна аудио, запись
- волна — аудио-интерфейс, запись
- запись аудио звукового сигнала, сведения
- Структура ВАВЕХДР
- Функция Вавеинаддбуффер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336993"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="212da-108">Управление записью Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="212da-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="212da-109">После открытия устройства ввода аудио-звука можно начать запись данных аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="212da-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="212da-110">Аудио-данные записываются в предоставляемые приложением буферы, заданные структурой [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) .</span><span class="sxs-lookup"><span data-stu-id="212da-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="212da-111">Эти блоки данных должны быть подготовлены до их использования; Дополнительные сведения см. в разделе [Звуковые блоки данных](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="212da-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="212da-112">Windows предоставляет следующие функции для управления записью аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="212da-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="212da-113">Функция</span><span class="sxs-lookup"><span data-stu-id="212da-113">Function</span></span>                                   | <span data-ttu-id="212da-114">Описание</span><span class="sxs-lookup"><span data-stu-id="212da-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="212da-115">**вавеинаддбуффер**</span><span class="sxs-lookup"><span data-stu-id="212da-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="212da-116">Отправляет буфер драйверу устройства, чтобы его можно было заполнить записанными данными аудио-данных.</span><span class="sxs-lookup"><span data-stu-id="212da-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="212da-117">**вавеинресет**</span><span class="sxs-lookup"><span data-stu-id="212da-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="212da-118">Останавливает запись аудио-звука и помечает все ожидающие буфер как выполненные.</span><span class="sxs-lookup"><span data-stu-id="212da-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="212da-119">**вавеинстарт**</span><span class="sxs-lookup"><span data-stu-id="212da-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="212da-120">Запускает запись аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="212da-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="212da-121">**вавеинстоп**</span><span class="sxs-lookup"><span data-stu-id="212da-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="212da-122">Останавливает запись аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="212da-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="212da-123">Используйте функцию [**вавеинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) для отправки буферов в драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="212da-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="212da-124">Так как буферы заполнены записанными аудио-данными, приложение получает уведомление о окне, сообщение обратного вызова, сообщение потока или событие, в зависимости от флага, указанного при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="212da-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="212da-125">Прежде чем начать запись с помощью [**вавеинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), необходимо отправить драйверу по крайней мере один буфер, иначе входящие данные могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="212da-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="212da-126">Перед закрытием устройства с помощью [**вавеинклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)вызовите [**вавеинресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) , чтобы пометить все ожидающие блоки данных как выполненные.</span><span class="sxs-lookup"><span data-stu-id="212da-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="212da-127">См. также</span><span class="sxs-lookup"><span data-stu-id="212da-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212da-128">Запись звука звукозаписи</span><span class="sxs-lookup"><span data-stu-id="212da-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 