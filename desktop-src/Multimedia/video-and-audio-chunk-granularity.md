---
title: Гранулярность фрагментов видео и звука
description: Гранулярность фрагментов видео и звука
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Файлы AVI, гранулярность фрагмента
- Класс Авикап, фрагменты заполнителя
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986591"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="499cd-109">Гранулярность фрагментов видео и звука</span><span class="sxs-lookup"><span data-stu-id="499cd-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="499cd-110">Гранулярность фрагмента — это размер логического блока для AVI-файла, который используется для записи и извлечения фрагментов аудио-и видеоданных.</span><span class="sxs-lookup"><span data-stu-id="499cd-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="499cd-111">При записи фрагментов аудио и видео на диск Авикап добавляет фрагменты заполнителя (нежелательные фрагменты Metallica) по мере необходимости для заполнения каждого логического блока данных.</span><span class="sxs-lookup"><span data-stu-id="499cd-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="499cd-112">Вы можете получить текущий параметр детализации фрагмента с помощью сообщения [**о \_ \_ \_ \_ настройке для получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="499cd-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="499cd-113">Текущая степень детализации фрагментов хранится в элементе **вчункгрануларити** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="499cd-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="499cd-114">Можно указать новую степень гранулярности фрагмента в качестве значения параметра **вчункгрануларити** , а затем отправить обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления \_ WM \_ Set \_ Sequence**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="499cd-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="499cd-115">Можно также указать ноль для этого элемента, чтобы задать гранулярность фрагмента на размер сектора диска.</span><span class="sxs-lookup"><span data-stu-id="499cd-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 




