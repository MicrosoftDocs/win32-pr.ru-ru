---
description: Ниже показаны константы безопасности WMI, используемые для событий. Они используются для задания записей контроля доступа (ACE) в дескрипторах безопасности, используемых для событий или приемников.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Константы безопасности событий (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156002"
---
# <a name="event-security-constants"></a><span data-ttu-id="f0d22-104">Константы безопасности событий</span><span class="sxs-lookup"><span data-stu-id="f0d22-104">Event Security Constants</span></span>

<span data-ttu-id="f0d22-105">Ниже показаны константы безопасности WMI, используемые для событий.</span><span class="sxs-lookup"><span data-stu-id="f0d22-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="f0d22-106">Они используются для задания записей контроля доступа (ACE) в дескрипторах безопасности, используемых для событий или приемников.</span><span class="sxs-lookup"><span data-stu-id="f0d22-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="f0d22-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_Публикация с правильной \_ ПУБЛИКАЦИей WBEM**</span><span class="sxs-lookup"><span data-stu-id="f0d22-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0d22-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="f0d22-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="f0d22-109">Указывает, что учетная запись может публиковать события в экземпляре [**\_ \_ EventFilter**](--eventfilter.md) , который определяет фильтр событий для постоянного потребителя.</span><span class="sxs-lookup"><span data-stu-id="f0d22-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="f0d22-110">Доступно в вбемкли. h.</span><span class="sxs-lookup"><span data-stu-id="f0d22-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0d22-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_Подписка WBEM right \_**</span><span class="sxs-lookup"><span data-stu-id="f0d22-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0d22-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="f0d22-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="f0d22-113">Указывает, что потребитель может подписываться на события, доставляемые в приемник.</span><span class="sxs-lookup"><span data-stu-id="f0d22-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="f0d22-114">Используется в [**ивбемевентсинк:: сетсинксекурити**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span><span class="sxs-lookup"><span data-stu-id="f0d22-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="f0d22-115">Доступно в вбемкли. h.</span><span class="sxs-lookup"><span data-stu-id="f0d22-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0d22-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ \_ \_ , подверженный \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="f0d22-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0d22-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="f0d22-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="f0d22-118">Поставщик событий указывает, что WMI проверяет свойство " **\_ дескриптор безопасности** " в каждом событии (наследуется от [**\_ \_ события**](--event.md)) и отправляет события только потребителям с соответствующими разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="f0d22-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="f0d22-119">Доступно в вбемпров. h.</span><span class="sxs-lookup"><span data-stu-id="f0d22-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0d22-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f0d22-120">Requirements</span></span>



| <span data-ttu-id="f0d22-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f0d22-121">Requirement</span></span> | <span data-ttu-id="f0d22-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d22-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d22-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0d22-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d22-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0d22-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="f0d22-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0d22-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d22-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0d22-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="f0d22-127">Header</span><span class="sxs-lookup"><span data-stu-id="f0d22-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d22-128"><dt>Вбемкли. h; </dt> <dt>Вбемпров. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d22-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d22-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0d22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d22-130">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="f0d22-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="f0d22-131">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="f0d22-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="f0d22-132">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="f0d22-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




