---
description: Определяет тип уведомления, передаваемого \_ \_ \_ \_ функции обратного вызова уведомления приемника WFD.
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Перечисление WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663035"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="f5934-103">\_ \_ \_ Перечисление типов уведомлений приемника для дисплея WFD \_</span><span class="sxs-lookup"><span data-stu-id="f5934-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="f5934-104">Тип **\_ \_ \_ уведомления \_ sink дисплея WFD** определяет тип уведомления, передаваемого функции [**\_ \_ \_ \_ обратного вызова уведомления приемника WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="f5934-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5934-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5934-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f5934-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f5934-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5934-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**провисионингрекуестнотификатион**</span><span class="sxs-lookup"><span data-stu-id="f5934-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="f5934-108">Уведомление — это запрос на подготовку.</span><span class="sxs-lookup"><span data-stu-id="f5934-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="f5934-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**реконнектрекуестнотификатион**</span><span class="sxs-lookup"><span data-stu-id="f5934-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="f5934-110">Уведомление является запросом на повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="f5934-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="f5934-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**коннектеднотификатион**</span><span class="sxs-lookup"><span data-stu-id="f5934-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="f5934-112">Уведомление является подключенным уведомлением.</span><span class="sxs-lookup"><span data-stu-id="f5934-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="f5934-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**дисконнектеднотификатион**</span><span class="sxs-lookup"><span data-stu-id="f5934-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="f5934-114">Уведомление является отключенным уведомлением.</span><span class="sxs-lookup"><span data-stu-id="f5934-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5934-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f5934-115">Requirements</span></span>



| <span data-ttu-id="f5934-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f5934-116">Requirement</span></span> | <span data-ttu-id="f5934-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f5934-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5934-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5934-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5934-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5934-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f5934-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5934-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5934-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5934-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5934-122">Header</span><span class="sxs-lookup"><span data-stu-id="f5934-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5934-123"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5934-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




