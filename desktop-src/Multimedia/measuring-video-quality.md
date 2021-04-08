---
title: Измерение качества видео
description: Измерение качества видео
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067900"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="7e0a4-107">Измерение качества видео</span><span class="sxs-lookup"><span data-stu-id="7e0a4-107">Measuring Video Quality</span></span>

<span data-ttu-id="7e0a4-108">Одним из способов измерения качества видео является ограничение числа записанных кадров, отброшенных во время операции записи.</span><span class="sxs-lookup"><span data-stu-id="7e0a4-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="7e0a4-109">Когда потоковая передача завершена, значение качества сравнивается с отношением удаленных кадров к общему количеству кадров.</span><span class="sxs-lookup"><span data-stu-id="7e0a4-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="7e0a4-110">Если процент удаленных кадров больше значения элемента **вперцентдропфореррор** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) , авикап отправляет сообщение об ошибке функции обратного вызова ошибки, если она установлена.</span><span class="sxs-lookup"><span data-stu-id="7e0a4-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="7e0a4-111">Вы можете получить текущее предельное число пропущенных кадров (выраженное в процентах) с помощью сообщения о [**\_ \_ \_ \_ настройке установки последовательностей WM Cap**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="7e0a4-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="7e0a4-112">Можно задать новое ограничение, указав процентную долю в качестве значения элемента **вперцентдропфореррор** структуры **каптурепармс** , а затем отправив обновленную структуру в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="7e0a4-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="7e0a4-113">Значение по умолчанию **вперцентдропфореррор** — 10 процентов.</span><span class="sxs-lookup"><span data-stu-id="7e0a4-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




