---
title: Типы перечисления API службы удаленных рабочих столов
description: Перечисляет типы перечислений, которые используются с API службы удаленных рабочих столов.
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330608"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="a9459-103">Типы перечисления API службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="a9459-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="a9459-104">С службы удаленных рабочих столов API используются следующие типы перечислений.</span><span class="sxs-lookup"><span data-stu-id="a9459-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9459-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="a9459-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a9459-106">**\_класс конфигурации \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="a9459-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="a9459-107">Содержит значения, указывающие тип пользовательской конфигурации, которую необходимо задать или получить в вызове функций [**втскуерюсерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) и [**втссетусерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="a9459-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-108">**\_источник конфигурации \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="a9459-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="a9459-109">Задает источник сведений о конфигурации, возвращаемых функцией [**втскуерюсерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="a9459-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-110">**\_класс ВТС коннектстате \_**</span><span class="sxs-lookup"><span data-stu-id="a9459-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="a9459-111">Указывает состояние соединения службы удаленных рабочих столов сеанса.</span><span class="sxs-lookup"><span data-stu-id="a9459-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-112">**\_класс сведений \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="a9459-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="a9459-113">Содержит значения, указывающие тип сведений сеанса, которые необходимо получить при вызове функции [**втскуерисессионинформатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="a9459-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-114">**\_класс типа \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="a9459-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="a9459-115">Указывает тип структуры, возвращаемой функцией службы удаленных рабочих столов в буфере.</span><span class="sxs-lookup"><span data-stu-id="a9459-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-116">**\_виртуальный \_ класс ВТС**</span><span class="sxs-lookup"><span data-stu-id="a9459-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="a9459-117">Содержит значения, указывающие тип извлекаемых данных виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="a9459-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-118">**\_семейство адресов \_ втссбкс**</span><span class="sxs-lookup"><span data-stu-id="a9459-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="a9459-119">Содержит значения, указывающие семейство адресов сетевого адреса, используемого для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="a9459-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-120">**ВТССБКС \_ машинный \_ сток**</span><span class="sxs-lookup"><span data-stu-id="a9459-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="a9459-121">Содержит значения, указывающие состояние стока сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="a9459-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-122">**\_ \_ режим сеанса втссбкс \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="a9459-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="a9459-123">Содержит значения, указывающие режим сеанса для сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a9459-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-124">**\_состояние компьютера \_ втссбкс**</span><span class="sxs-lookup"><span data-stu-id="a9459-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="a9459-125">Содержит значения, указывающие текущее состояние сервера.</span><span class="sxs-lookup"><span data-stu-id="a9459-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-126">**\_тип уведомления \_ втссбкс**</span><span class="sxs-lookup"><span data-stu-id="a9459-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="a9459-127">Содержит значения, указывающие тип изменения состояния, возникшего на сервере узла сеансов удаленных рабочих столов или в сеансе пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9459-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="a9459-128">**\_состояние сеанса \_ втссбкс**</span><span class="sxs-lookup"><span data-stu-id="a9459-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="a9459-129">Содержит значения, указывающие состояние соединения пользовательского сеанса.</span><span class="sxs-lookup"><span data-stu-id="a9459-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




