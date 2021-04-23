---
title: Ограничение времени
description: Ограничение времени
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Структура КАПТУРЕПАРМС
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Структура КАПТУРЕПАРМС
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779976"
---
# <a name="time-limit"></a><span data-ttu-id="0210b-109">Ограничение времени</span><span class="sxs-lookup"><span data-stu-id="0210b-109">Time Limit</span></span>

<span data-ttu-id="0210b-110">Длительность операции записи можно ограничить с помощью членов **флимитенаблед** и **втимелимит** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="0210b-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="0210b-111">Элемент **флимитенаблед** указывает, следует ли выполнять операцию записи, в то время как **втимелимит** указывает максимальную продолжительность операции записи.</span><span class="sxs-lookup"><span data-stu-id="0210b-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="0210b-112">Вы можете получить значения для **флимитенаблед** и **втимелимит** с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="0210b-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="0210b-113">Вы можете включить таймер для операции записи, указав значение **true** в качестве значения параметра **флимитенаблед**, или можно задать длительность операции записи, указав в параметрах **втимелимит** время.</span><span class="sxs-lookup"><span data-stu-id="0210b-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="0210b-114">После установки этих членов отправьте обновленную структуру [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="0210b-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="0210b-115">По умолчанию **флимитенаблед** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="0210b-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




