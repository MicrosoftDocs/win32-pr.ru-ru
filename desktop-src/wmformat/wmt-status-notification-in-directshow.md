---
title: WMT_STATUS уведомления о событии в DirectShow
description: '\_Уведомление о событии состояния ВМТ в DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Пакет SDK Windows Media Format, WMT_STATUS уведомления о событиях в DirectShow
- Windows Media Format SDK, уведомления о событиях
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный формат систем (ASF), WMT_STATUS уведомления о событиях в DirectShow
- ASF (Расширенный системный формат), WMT_STATUS уведомлений о событиях в DirectShow
- Расширенный формат систем (ASF), уведомления о событиях
- ASF (Расширенный системный формат), уведомления о событиях
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, уведомления о событиях
- DirectShow, WMT_STATUS уведомления о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260926"
---
# <a name="wmt_status-event-notification-in-directshow"></a><span data-ttu-id="1a511-114">\_Уведомление о событии состояния ВМТ в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a511-114">WMT\_STATUS Event Notification in DirectShow</span></span>

<span data-ttu-id="1a511-115">Обработчики ASF и модуля записи ASF пересылают [**события \_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) в приложения.</span><span class="sxs-lookup"><span data-stu-id="1a511-115">Both the ASF Reader and the ASF Writer forward [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) events to applications.</span></span> <span data-ttu-id="1a511-116">Модуль записи перенаправляет все такие события, а модуль чтения перенаправляет только те из них, которые относятся к приобретению лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="1a511-116">The writer forwards all such events, and the reader forwards only those that pertain to DRM license acquisition.</span></span> <span data-ttu-id="1a511-117">Чтобы получать эти уведомления о событиях в приложении, добавьте обращение к **\_ \_ событию EC ВМТ** в функции обработки событий.</span><span class="sxs-lookup"><span data-stu-id="1a511-117">To receive these event notifications in your application, add a case for the **EC\_WMT\_EVENT** in your event-handling function.</span></span> <span data-ttu-id="1a511-118">Параметр *lParam1* , связанный с событием, содержит **код \_ состояния ВМТ** (который может быть **ВМТ \_ Error**), а lParam2 содержит [**\_ \_ \_ данные о событии AM ВМТ**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) , включающие **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a511-118">The *lParam1* parameter associated with the event contains the **WMT\_STATUS** code (which can be **WMT\_ERROR**) and lParam2 contains an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) that includes the **HRESULT**.</span></span>

 

 