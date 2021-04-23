---
title: Размер индексов
description: Размер индексов
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777120"
---
# <a name="index-size"></a><span data-ttu-id="af21f-107">Размер индексов</span><span class="sxs-lookup"><span data-stu-id="af21f-107">Index Size</span></span>

<span data-ttu-id="af21f-108">Каждый AVI-файл использует индекс указанного размера для нахождение фрагментов видео и звуковых данных в файле.</span><span class="sxs-lookup"><span data-stu-id="af21f-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="af21f-109">Запись в индексе находит один видеокадр или звуковой буфер аудио.</span><span class="sxs-lookup"><span data-stu-id="af21f-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="af21f-110">Следовательно, значение размера индекса косвенно задает верхний предел числа кадров, которые могут быть захвачены в файле.</span><span class="sxs-lookup"><span data-stu-id="af21f-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="af21f-111">Текущий размер индекса можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="af21f-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="af21f-112">Текущий размер индекса хранится в элементе **двиндекссизе** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="af21f-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="af21f-113">Можно указать новый размер индекса в качестве значения параметра **двиндекссизе** , а затем отправить обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="af21f-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="af21f-114">По умолчанию размер индекса составляет 34 952 записей (что позволяет использовать 32 000 кадров и пропорциональное количество звуковых буферов).</span><span class="sxs-lookup"><span data-stu-id="af21f-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




