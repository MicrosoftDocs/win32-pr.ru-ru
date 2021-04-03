---
title: Звуковые буферы
description: Звуковые буферы
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774714"
---
# <a name="audio-buffers"></a><span data-ttu-id="4eb34-107">Звуковые буферы</span><span class="sxs-lookup"><span data-stu-id="4eb34-107">Audio Buffers</span></span>

<span data-ttu-id="4eb34-108">Управлять звуковой частью операции записи можно тремя способами:</span><span class="sxs-lookup"><span data-stu-id="4eb34-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="4eb34-109">Включение или исключение звука из операции записи.</span><span class="sxs-lookup"><span data-stu-id="4eb34-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="4eb34-110">Запросите определенное количество звуковых буферов.</span><span class="sxs-lookup"><span data-stu-id="4eb34-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="4eb34-111">Запрос на то, что буферы аудио имеют конкретный размер.</span><span class="sxs-lookup"><span data-stu-id="4eb34-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="4eb34-112">Параметры для буферов аудио можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке для получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4eb34-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="4eb34-113">Элемент **фкаптуреаудио** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) указывает, включено ли аудио или исключено из операции записи.</span><span class="sxs-lookup"><span data-stu-id="4eb34-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="4eb34-114">Текущее запрошенное количество звуковых буферов хранится в элементе **внумаудиорекуестед** , а текущий размер буфера аудио хранится в элементе **дваудиобуфферсизе** .</span><span class="sxs-lookup"><span data-stu-id="4eb34-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="4eb34-115">Можно указать, следует ли включать запись звука, указать размер и количество звуковых буферов, обновив эти элементы, и отправить обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4eb34-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="4eb34-116">По умолчанию звук включается в операцию записи, и выделяется четыре буфера аудио.</span><span class="sxs-lookup"><span data-stu-id="4eb34-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="4eb34-117">Значение **фкаптуреаудио** по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="4eb34-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="4eb34-118">Размер буфера по умолчанию (значение **дваудиобуфферсизе**) может содержать 0,5 секунд для звуковых данных или 10000, в зависимости от того, что больше.</span><span class="sxs-lookup"><span data-stu-id="4eb34-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




