---
description: Описывает результат, который при необходимости можно задать после обработки уведомления приемника \_ \_ \_ уведомлений в \_ функции обратного вызова уведомления приемника WFD.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Структура WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Вфдсинк. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664485"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="74ce5-103">\_ \_ \_ Структура результата уведомления приемника для дисплея WFD \_</span><span class="sxs-lookup"><span data-stu-id="74ce5-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="74ce5-104">В **структуре \_ \_ \_ \_ результатов уведомлений о приемнике WFD отображаются сведения о** результатах, которые можно задать после обработки уведомления приемника уведомлений в функции [**\_ \_ \_ \_ обратного вызова уведомления приемника WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="74ce5-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ce5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74ce5-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="74ce5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="74ce5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="74ce5-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="74ce5-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-108">[**\_ \_ \_ \_ Заголовок объекта для приемника WFD**](wfd-display-sink-object-header.md) , описывающий данные, включаемые в результат уведомления.</span><span class="sxs-lookup"><span data-stu-id="74ce5-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="74ce5-109">**type**</span><span class="sxs-lookup"><span data-stu-id="74ce5-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-110">Значение [**\_ \_ \_ \_ типа уведомления о приемнике представления WFD**](wfd-display-sink-notification-type.md) , которое указывает тип результата уведомления.</span><span class="sxs-lookup"><span data-stu-id="74ce5-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="74ce5-111">Этот параметр также определяет, какие сведения следует использовать в приведенном ниже объединении.</span><span class="sxs-lookup"><span data-stu-id="74ce5-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="74ce5-112">**провисионингдата**</span><span class="sxs-lookup"><span data-stu-id="74ce5-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-113">Сведения о результате запроса на подготовку.</span><span class="sxs-lookup"><span data-stu-id="74ce5-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="74ce5-114">Используйте этот параметр, если *тип* имеет значение **провисионингрекуестнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="74ce5-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="74ce5-115">**конфигмесод**</span><span class="sxs-lookup"><span data-stu-id="74ce5-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-116">Метод отображения пользовательского интерфейса для интерактивного принятия.</span><span class="sxs-lookup"><span data-stu-id="74ce5-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="74ce5-117">**упасскэйленгс**</span><span class="sxs-lookup"><span data-stu-id="74ce5-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-118">Число расширенных символов в *ключе доступа*, при котором не учитываются признаки конца строки null.</span><span class="sxs-lookup"><span data-stu-id="74ce5-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="74ce5-119">**Наличия**</span><span class="sxs-lookup"><span data-stu-id="74ce5-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-120">Содержит ключ Pass в виде массива расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="74ce5-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="74ce5-121">\_ \_ Сведения о WPS приемника WFD \_ \_ Максимальная \_ \_ Длина ключа доступа определяется как значение (8).</span><span class="sxs-lookup"><span data-stu-id="74ce5-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="74ce5-122">**реконнектдата**</span><span class="sxs-lookup"><span data-stu-id="74ce5-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-123">Сведения о результате запроса на повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="74ce5-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="74ce5-124">Используйте этот параметр, если *тип* имеет значение **реконнектрекуестнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="74ce5-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="74ce5-125">**стрпрофиле**</span><span class="sxs-lookup"><span data-stu-id="74ce5-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="74ce5-126">Указатель на строку, завершающуюся нулем, описывающую профиль.</span><span class="sxs-lookup"><span data-stu-id="74ce5-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74ce5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="74ce5-127">Requirements</span></span>



| <span data-ttu-id="74ce5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="74ce5-128">Requirement</span></span> | <span data-ttu-id="74ce5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74ce5-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="74ce5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74ce5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74ce5-131">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74ce5-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74ce5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74ce5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74ce5-133">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="74ce5-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74ce5-134">Header</span><span class="sxs-lookup"><span data-stu-id="74ce5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ce5-135"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ce5-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




