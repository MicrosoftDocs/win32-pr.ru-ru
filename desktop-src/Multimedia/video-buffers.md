---
title: Буферы видео
description: Буферы видео
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778119"
---
# <a name="video-buffers"></a><span data-ttu-id="4eb85-107">Буферы видео</span><span class="sxs-lookup"><span data-stu-id="4eb85-107">Video Buffers</span></span>

<span data-ttu-id="4eb85-108">Буферы, используемые для записи видео, находятся в куче памяти.</span><span class="sxs-lookup"><span data-stu-id="4eb85-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="4eb85-109">Количество буферов, используемых в операции записи, может зависеть от значения элемента **внумвидеорекуестед** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) и доступной системной памяти.</span><span class="sxs-lookup"><span data-stu-id="4eb85-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="4eb85-110">Текущее значение запрошенных буферов видео можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4eb85-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="4eb85-111">Текущее запрошенное число буферов видео хранится в элементе **внумвидеорекуестед** структуры **каптурепармс** .</span><span class="sxs-lookup"><span data-stu-id="4eb85-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="4eb85-112">Вы можете запросить размещение и количество буферов, обновив этот элемент, а затем отправив обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4eb85-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




