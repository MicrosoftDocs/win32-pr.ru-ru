---
title: Функции интерфейса протокола маршрутизации
description: Реализуйте следующие функции для библиотеки DLL протокола маршрутизации
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b696d516cf0fc0b13d66fdc53b384a28fac8696a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987841"
---
# <a name="routing-protocol-interface-functions"></a><span data-ttu-id="f1663-103">Функции интерфейса протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="f1663-103">Routing Protocol Interface Functions</span></span>

<span data-ttu-id="f1663-104">Реализуйте следующие функции для библиотеки DLL протокола маршрутизации:</span><span class="sxs-lookup"><span data-stu-id="f1663-104">Implement the following functions for a routing protocol DLL:</span></span>

[<span data-ttu-id="f1663-105">**аддинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="f1663-105">**AddInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[<span data-ttu-id="f1663-106">**коннектклиент**</span><span class="sxs-lookup"><span data-stu-id="f1663-106">**ConnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[<span data-ttu-id="f1663-107">**делетеинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="f1663-107">**DeleteInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[<span data-ttu-id="f1663-108">**дисконнектклиент**</span><span class="sxs-lookup"><span data-stu-id="f1663-108">**DisconnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[<span data-ttu-id="f1663-109">**даупдатераутес**</span><span class="sxs-lookup"><span data-stu-id="f1663-109">**DoUpdateRoutes**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

<span data-ttu-id="f1663-110">[*даупдатесервицес*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1663-110">[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

[<span data-ttu-id="f1663-111">**жетевентмессаже**</span><span class="sxs-lookup"><span data-stu-id="f1663-111">**GetEventMessage**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[<span data-ttu-id="f1663-112">**жетглобалинфо**</span><span class="sxs-lookup"><span data-stu-id="f1663-112">**GetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[<span data-ttu-id="f1663-113">**жетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="f1663-113">**GetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[<span data-ttu-id="f1663-114">**жетмфестатус**</span><span class="sxs-lookup"><span data-stu-id="f1663-114">**GetMfeStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[<span data-ttu-id="f1663-115">**Соседи**</span><span class="sxs-lookup"><span data-stu-id="f1663-115">**GetNeighbors**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[<span data-ttu-id="f1663-116">**интерфацестатус**</span><span class="sxs-lookup"><span data-stu-id="f1663-116">**InterfaceStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[<span data-ttu-id="f1663-117">**мибкреате**</span><span class="sxs-lookup"><span data-stu-id="f1663-117">**MibCreate**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[<span data-ttu-id="f1663-118">**мибделете**</span><span class="sxs-lookup"><span data-stu-id="f1663-118">**MibDelete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[<span data-ttu-id="f1663-119">**мибжет**</span><span class="sxs-lookup"><span data-stu-id="f1663-119">**MibGet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[<span data-ttu-id="f1663-120">**мибжетфирст**</span><span class="sxs-lookup"><span data-stu-id="f1663-120">**MibGetFirst**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[<span data-ttu-id="f1663-121">**мибжетнекст**</span><span class="sxs-lookup"><span data-stu-id="f1663-121">**MibGetNext**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[<span data-ttu-id="f1663-122">*мибжеттрапинфо*</span><span class="sxs-lookup"><span data-stu-id="f1663-122">*MibGetTrapInfo*</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[<span data-ttu-id="f1663-123">**мибсет**</span><span class="sxs-lookup"><span data-stu-id="f1663-123">**MibSet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[<span data-ttu-id="f1663-124">**мибсеттрапинфо**</span><span class="sxs-lookup"><span data-stu-id="f1663-124">**MibSetTrapInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[<span data-ttu-id="f1663-125">**куериповер**</span><span class="sxs-lookup"><span data-stu-id="f1663-125">**QueryPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[<span data-ttu-id="f1663-126">**регистерпротокол**</span><span class="sxs-lookup"><span data-stu-id="f1663-126">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[<span data-ttu-id="f1663-127">**сетглобалинфо**</span><span class="sxs-lookup"><span data-stu-id="f1663-127">**SetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[<span data-ttu-id="f1663-128">**сетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="f1663-128">**SetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[<span data-ttu-id="f1663-129">**сетповер**</span><span class="sxs-lookup"><span data-stu-id="f1663-129">**SetPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[<span data-ttu-id="f1663-130">**старткомплете**</span><span class="sxs-lookup"><span data-stu-id="f1663-130">**StartComplete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[<span data-ttu-id="f1663-131">**стартпротокол**</span><span class="sxs-lookup"><span data-stu-id="f1663-131">**StartProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[<span data-ttu-id="f1663-132">**стоппротокол**</span><span class="sxs-lookup"><span data-stu-id="f1663-132">**StopProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

<span data-ttu-id="f1663-133">[**унбиндинтерфаце**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1663-133">[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span></span>

<span data-ttu-id="f1663-134">Если протокол маршрутизации поддерживает обработку служб, реализуйте следующую функцию в дополнение к указанным выше.</span><span class="sxs-lookup"><span data-stu-id="f1663-134">If the routing protocol supports service handling, implement the following function in addition to those listed preceding:</span></span>

<span data-ttu-id="f1663-135">[**даупдатесервицес**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1663-135">[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

 

 