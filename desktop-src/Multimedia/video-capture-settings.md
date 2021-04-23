---
title: Параметры видеозаписи
description: Параметры видеозаписи
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Структура КАПТУРЕПАРМС
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661519"
---
# <a name="video-capture-settings"></a><span data-ttu-id="5c40f-108">Параметры видеозаписи</span><span class="sxs-lookup"><span data-stu-id="5c40f-108">Video Capture Settings</span></span>

<span data-ttu-id="5c40f-109">Структура [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) содержит параметры элемента управления для потоковой записи видео.</span><span class="sxs-lookup"><span data-stu-id="5c40f-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="5c40f-110">Эта структура управляет несколькими аспектами процесса отслеживания и позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="5c40f-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="5c40f-111">Укажите частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="5c40f-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="5c40f-112">Укажите число выделенных буферов видео.</span><span class="sxs-lookup"><span data-stu-id="5c40f-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="5c40f-113">Отключите и включите запись звука.</span><span class="sxs-lookup"><span data-stu-id="5c40f-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="5c40f-114">Укажите интервал времени для записи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="5c40f-115">Укажите, используется ли устройство MCI (ВИДЕОМАГНИТОФОН или видеодиск) во время записи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="5c40f-116">Укажите клавиатуру или элемент управления мышью для завершения потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="5c40f-117">Укажите тип усреднения видео, применяемый во время записи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="5c40f-118">Вы можете получить текущие параметры записи в структуре [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) , отправив сообщение о [**\_ \_ \_ \_ настройке установки последовательностей WM Cap**](wm-cap-get-sequence-setup.md) (или макрос [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="5c40f-119">Вы можете задать один или несколько текущих параметров записи, обновив соответствующие члены структуры **каптурепармс** , а затем отправив сообщение о [**\_ \_ \_ \_ настройке установки последовательностей WM Cap**](wm-cap-set-sequence-setup.md) (или макрос [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) и **каптурепармс** в окно записи.</span><span class="sxs-lookup"><span data-stu-id="5c40f-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




