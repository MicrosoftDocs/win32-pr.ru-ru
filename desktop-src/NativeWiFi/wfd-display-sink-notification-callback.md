---
description: Определяет функцию обратного вызова&\# 8212;, которая реализуется в приложении&\# 8212;, которое было указано в функции вфдстартдисплайсинк.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: Функция обратного вызова WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663037"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="87892-103">\_ \_ \_ Функция обратного вызова для уведомлений о приемнике для дисплея WFD \_</span><span class="sxs-lookup"><span data-stu-id="87892-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="87892-104">Функция **\_ \_ \_ \_ обратного вызова уведомления о приемнике WFD дисплея** определяет функцию обратного вызова, которая реализуется в приложении, которая была указана для функции [**вфдстартдисплайсинк**](wfdstartdisplaysink.md) .</span><span class="sxs-lookup"><span data-stu-id="87892-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="87892-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87892-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="87892-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87892-107">*пвконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="87892-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87892-108">Необязательный указатель контекста, передаваемый функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="87892-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="87892-109">*пнотификатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87892-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87892-110">Указатель на структуру, содержащую данные уведомления о приемнике экрана.</span><span class="sxs-lookup"><span data-stu-id="87892-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="87892-111">*пнотификатионресулт* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="87892-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87892-112">Указатель на структуру, содержащую данные, которые могут быть заданы приложением для указания результата обработки уведомления о приемнике отображения.</span><span class="sxs-lookup"><span data-stu-id="87892-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87892-113">Требования</span><span class="sxs-lookup"><span data-stu-id="87892-113">Requirements</span></span>



| <span data-ttu-id="87892-114">Требование</span><span class="sxs-lookup"><span data-stu-id="87892-114">Requirement</span></span> | <span data-ttu-id="87892-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87892-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87892-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87892-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87892-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87892-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="87892-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87892-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87892-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="87892-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87892-120">Header</span><span class="sxs-lookup"><span data-stu-id="87892-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="87892-121"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="87892-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




