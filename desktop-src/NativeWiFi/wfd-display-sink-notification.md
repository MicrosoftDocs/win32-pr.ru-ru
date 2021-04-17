---
description: Описывает уведомление, передаваемое \_ \_ \_ функции обратного вызова уведомлений для приемника WFD \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Структура WFD_DISPLAY_SINK_NOTIFICATION (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663036"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="db474-103">\_ \_ Структура уведомлений о приемнике для экрана WFD \_</span><span class="sxs-lookup"><span data-stu-id="db474-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="db474-104">В **структуре \_ \_ \_ уведомлений о приемнике для представления WFD** описывается уведомление, передаваемое функции [**\_ \_ \_ \_ обратного вызова уведомлений о приемнике для монитора WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="db474-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="db474-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db474-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="db474-106">Члены</span><span class="sxs-lookup"><span data-stu-id="db474-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="db474-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="db474-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="db474-108">[**\_ \_ \_ \_ Заголовок объекта для приемника WFD**](wfd-display-sink-object-header.md) , описывающий данные, содержащиеся в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="db474-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="db474-109">**type**</span><span class="sxs-lookup"><span data-stu-id="db474-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="db474-110">Значение [**\_ \_ \_ \_ типа уведомления о приемнике для представления WFD**](wfd-display-sink-notification-type.md) , которое указывает тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="db474-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="db474-111">Этот параметр также определяет, какие сведения следует использовать в приведенном ниже объединении.</span><span class="sxs-lookup"><span data-stu-id="db474-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="db474-112">**стрремотедевиценаме**</span><span class="sxs-lookup"><span data-stu-id="db474-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="db474-113">Содержит строку, завершающуюся НУЛЕМ, которая содержит имя удаленного устройства.</span><span class="sxs-lookup"><span data-stu-id="db474-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="db474-114">\_ \_ Максимальная \_ Длина имени устройства в приемнике WFD \_ \_ определяется как значение (32).</span><span class="sxs-lookup"><span data-stu-id="db474-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="db474-115">**ремотедевицеаддресс**</span><span class="sxs-lookup"><span data-stu-id="db474-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="db474-116">[**\_ Mac- \_ адрес DOT11**](dot11-mac-address-type.md) , содержащий BSSID удаленного устройства.</span><span class="sxs-lookup"><span data-stu-id="db474-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="db474-117">**провисионингрекуестинфо**</span><span class="sxs-lookup"><span data-stu-id="db474-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="db474-118">Сведения о запросе на подготовку.</span><span class="sxs-lookup"><span data-stu-id="db474-118">Info about a provisioning request.</span></span> <span data-ttu-id="db474-119">Используйте этот параметр, если *тип* имеет значение **провисионингрекуестнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="db474-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="db474-120">**хсессионхандле**</span><span class="sxs-lookup"><span data-stu-id="db474-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="db474-121">Обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="db474-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="db474-122">**поссиблеконфигмесодс**</span><span class="sxs-lookup"><span data-stu-id="db474-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="db474-123">Возможные методы для отображения пользовательского интерфейса для интерактивного принятия.</span><span class="sxs-lookup"><span data-stu-id="db474-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db474-124">**реконнектрекуестинфо**</span><span class="sxs-lookup"><span data-stu-id="db474-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="db474-125">Сведения о запросе на повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="db474-125">Info about a reconnect request.</span></span> <span data-ttu-id="db474-126">Используйте этот параметр, если *тип* имеет значение **реконнектрекуестнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="db474-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="db474-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="db474-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="db474-128">Идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="db474-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db474-129">**коннектединфо**</span><span class="sxs-lookup"><span data-stu-id="db474-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="db474-130">Сведения о подключенном уведомлении.</span><span class="sxs-lookup"><span data-stu-id="db474-130">Info about a connected notification.</span></span> <span data-ttu-id="db474-131">Используйте этот параметр, если *тип* имеет значение **коннектеднотификатион**.</span><span class="sxs-lookup"><span data-stu-id="db474-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="db474-132">**хсессионхандле**</span><span class="sxs-lookup"><span data-stu-id="db474-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="db474-133">Обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="db474-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="db474-134">**гуидсессионинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="db474-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="db474-135">Идентификатор GUID, указывающий интерфейс сеанса.</span><span class="sxs-lookup"><span data-stu-id="db474-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="db474-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="db474-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="db474-137">Идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="db474-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="db474-138">**стрпрофиле**</span><span class="sxs-lookup"><span data-stu-id="db474-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="db474-139">Указатель на строку, завершающуюся нулем, описывающую профиль.</span><span class="sxs-lookup"><span data-stu-id="db474-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="db474-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="db474-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="db474-141">Локальный адрес.</span><span class="sxs-lookup"><span data-stu-id="db474-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="db474-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="db474-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="db474-143">Удаленный адрес.</span><span class="sxs-lookup"><span data-stu-id="db474-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="db474-144">**уртсппорт**</span><span class="sxs-lookup"><span data-stu-id="db474-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="db474-145">Порт RTSP.</span><span class="sxs-lookup"><span data-stu-id="db474-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db474-146">Требования</span><span class="sxs-lookup"><span data-stu-id="db474-146">Requirements</span></span>



| <span data-ttu-id="db474-147">Требование</span><span class="sxs-lookup"><span data-stu-id="db474-147">Requirement</span></span> | <span data-ttu-id="db474-148">Значение</span><span class="sxs-lookup"><span data-stu-id="db474-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="db474-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db474-149">Minimum supported client</span></span><br/> | <span data-ttu-id="db474-150">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db474-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db474-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db474-151">Minimum supported server</span></span><br/> | <span data-ttu-id="db474-152">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="db474-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db474-153">Header</span><span class="sxs-lookup"><span data-stu-id="db474-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="db474-154"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="db474-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




