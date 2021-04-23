---
title: Функции диспетчера таблиц маршрутизации версии 2
description: Для взаимодействия с диспетчером таблиц маршрутизации используются следующие функции.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации, версия 2, функции
- Диспетчер таблиц маршрутизации, службы RRAS версии 2, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f59e4a1ad2bf091d8a74672f1f473589c5fa1d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411089"
---
# <a name="routing-table-manager-version-2-functions"></a><span data-ttu-id="d7179-105">Функции диспетчера таблиц маршрутизации версии 2</span><span class="sxs-lookup"><span data-stu-id="d7179-105">Routing Table Manager Version 2 Functions</span></span>

<span data-ttu-id="d7179-106">Для взаимодействия с диспетчером таблиц маршрутизации используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="d7179-106">The following functions are used to interact with the routing table manager.</span></span>

## <a name="registration-functions"></a><span data-ttu-id="d7179-107">Функции регистрации</span><span class="sxs-lookup"><span data-stu-id="d7179-107">Registration Functions</span></span>

[<span data-ttu-id="d7179-108">**ртмрегистерентити**</span><span class="sxs-lookup"><span data-stu-id="d7179-108">**RtmRegisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[<span data-ttu-id="d7179-109">**ртмдерегистерентити**</span><span class="sxs-lookup"><span data-stu-id="d7179-109">**RtmDeregisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[<span data-ttu-id="d7179-110">**ртмжетрегистередентитиес**</span><span class="sxs-lookup"><span data-stu-id="d7179-110">**RtmGetRegisteredEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[<span data-ttu-id="d7179-111">**ртмрелеасинтитиес**</span><span class="sxs-lookup"><span data-stu-id="d7179-111">**RtmReleaseEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a><span data-ttu-id="d7179-112">Функции непрозрачных указателей</span><span class="sxs-lookup"><span data-stu-id="d7179-112">Opaque Pointer Functions</span></span>

[<span data-ttu-id="d7179-113">**ртмлоккдестинатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-113">**RtmLockDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[<span data-ttu-id="d7179-114">**ртмжетопакуеинформатионпоинтер**</span><span class="sxs-lookup"><span data-stu-id="d7179-114">**RtmGetOpaqueInformationPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a><span data-ttu-id="d7179-115">Функции метода Export</span><span class="sxs-lookup"><span data-stu-id="d7179-115">Export Method Functions</span></span>

[<span data-ttu-id="d7179-116">**ртмжетентитимесодс**</span><span class="sxs-lookup"><span data-stu-id="d7179-116">**RtmGetEntityMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[<span data-ttu-id="d7179-117">**ртминвокемесод**</span><span class="sxs-lookup"><span data-stu-id="d7179-117">**RtmInvokeMethod**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[<span data-ttu-id="d7179-118">**ртмблоккмесодс**</span><span class="sxs-lookup"><span data-stu-id="d7179-118">**RtmBlockMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a><span data-ttu-id="d7179-119">Обработчик для функций структуры информации</span><span class="sxs-lookup"><span data-stu-id="d7179-119">Handle to Information Structure Functions</span></span>

[<span data-ttu-id="d7179-120">**ртмжетентитинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-120">**RtmGetEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[<span data-ttu-id="d7179-121">**ртмжетдестинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-121">**RtmGetDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[<span data-ttu-id="d7179-122">**ртмжетраутеинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-122">**RtmGetRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[<span data-ttu-id="d7179-123">**ртмжетнекссопинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-123">**RtmGetNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[<span data-ttu-id="d7179-124">**ртмрелеасинтитинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-124">**RtmReleaseEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[<span data-ttu-id="d7179-125">**ртмрелеаседестинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-125">**RtmReleaseDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[<span data-ttu-id="d7179-126">**ртмрелеасераутеинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-126">**RtmReleaseRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[<span data-ttu-id="d7179-127">**ртмрелеасенекссопинфо**</span><span class="sxs-lookup"><span data-stu-id="d7179-127">**RtmReleaseNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a><span data-ttu-id="d7179-128">Функции вставки и удаления таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d7179-128">Routing Table Insertion and Deletion Functions</span></span>

[<span data-ttu-id="d7179-129">**ртмаддраутетодест**</span><span class="sxs-lookup"><span data-stu-id="d7179-129">**RtmAddRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[<span data-ttu-id="d7179-130">**ртмделетераутетодест**</span><span class="sxs-lookup"><span data-stu-id="d7179-130">**RtmDeleteRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[<span data-ttu-id="d7179-131">**ртмхолддестинатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-131">**RtmHoldDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[<span data-ttu-id="d7179-132">**ртмжетраутепоинтер**</span><span class="sxs-lookup"><span data-stu-id="d7179-132">**RtmGetRoutePointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[<span data-ttu-id="d7179-133">**ртмлоккрауте**</span><span class="sxs-lookup"><span data-stu-id="d7179-133">**RtmLockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[<span data-ttu-id="d7179-134">**ртмупдатеандунлоккрауте**</span><span class="sxs-lookup"><span data-stu-id="d7179-134">**RtmUpdateAndUnlockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a><span data-ttu-id="d7179-135">Функции запроса таблицы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d7179-135">Routing Table Query Functions</span></span>

[<span data-ttu-id="d7179-136">**ртмжетексактматчдестинатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-136">**RtmGetExactMatchDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[<span data-ttu-id="d7179-137">**ртмжетмостспеЦификдестинатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-137">**RtmGetMostSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[<span data-ttu-id="d7179-138">**ртмжетлессспеЦификдестинатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-138">**RtmGetLessSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[<span data-ttu-id="d7179-139">**ртмжетексактматчрауте**</span><span class="sxs-lookup"><span data-stu-id="d7179-139">**RtmGetExactMatchRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[<span data-ttu-id="d7179-140">**ртмисбестрауте**</span><span class="sxs-lookup"><span data-stu-id="d7179-140">**RtmIsBestRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a><span data-ttu-id="d7179-141">Функции вставки и удаления следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="d7179-141">Next-Hop Insertion and Deletion Functions</span></span>

[<span data-ttu-id="d7179-142">**ртмадднекссоп**</span><span class="sxs-lookup"><span data-stu-id="d7179-142">**RtmAddNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[<span data-ttu-id="d7179-143">**ртмфинднекссоп**</span><span class="sxs-lookup"><span data-stu-id="d7179-143">**RtmFindNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[<span data-ttu-id="d7179-144">**ртмделетенекссоп**</span><span class="sxs-lookup"><span data-stu-id="d7179-144">**RtmDeleteNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[<span data-ttu-id="d7179-145">**ртмжетнекссоппоинтер**</span><span class="sxs-lookup"><span data-stu-id="d7179-145">**RtmGetNextHopPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[<span data-ttu-id="d7179-146">**ртмлоккнекссоп**</span><span class="sxs-lookup"><span data-stu-id="d7179-146">**RtmLockNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a><span data-ttu-id="d7179-147">Функции перечисления таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d7179-147">Routing Table Enumeration Functions</span></span>

[<span data-ttu-id="d7179-148">**ртмкреатедестенум**</span><span class="sxs-lookup"><span data-stu-id="d7179-148">**RtmCreateDestEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[<span data-ttu-id="d7179-149">**ртмжетенумдестс**</span><span class="sxs-lookup"><span data-stu-id="d7179-149">**RtmGetEnumDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[<span data-ttu-id="d7179-150">**ртмрелеаседестс**</span><span class="sxs-lookup"><span data-stu-id="d7179-150">**RtmReleaseDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[<span data-ttu-id="d7179-151">**ртмкреатераутинум**</span><span class="sxs-lookup"><span data-stu-id="d7179-151">**RtmCreateRouteEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[<span data-ttu-id="d7179-152">**ртмжетенумраутес**</span><span class="sxs-lookup"><span data-stu-id="d7179-152">**RtmGetEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[<span data-ttu-id="d7179-153">**ртмрелеасераутес**</span><span class="sxs-lookup"><span data-stu-id="d7179-153">**RtmReleaseRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[<span data-ttu-id="d7179-154">**ртмкреатенекссопенум**</span><span class="sxs-lookup"><span data-stu-id="d7179-154">**RtmCreateNextHopEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[<span data-ttu-id="d7179-155">**ртмжетенумнекссопс**</span><span class="sxs-lookup"><span data-stu-id="d7179-155">**RtmGetEnumNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[<span data-ttu-id="d7179-156">**ртмрелеасенекссопс**</span><span class="sxs-lookup"><span data-stu-id="d7179-156">**RtmReleaseNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[<span data-ttu-id="d7179-157">**ртмделетинумхандле**</span><span class="sxs-lookup"><span data-stu-id="d7179-157">**RtmDeleteEnumHandle**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a><span data-ttu-id="d7179-158">Функции уведомлений об изменениях</span><span class="sxs-lookup"><span data-stu-id="d7179-158">Change Notification Functions</span></span>

[<span data-ttu-id="d7179-159">**ртмрегистерфорчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-159">**RtmRegisterForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[<span data-ttu-id="d7179-160">**ртмжетчанжеддестс**</span><span class="sxs-lookup"><span data-stu-id="d7179-160">**RtmGetChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[<span data-ttu-id="d7179-161">**ртмрелеасечанжеддестс**</span><span class="sxs-lookup"><span data-stu-id="d7179-161">**RtmReleaseChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[<span data-ttu-id="d7179-162">**ртмигноречанжеддестс**</span><span class="sxs-lookup"><span data-stu-id="d7179-162">**RtmIgnoreChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[<span data-ttu-id="d7179-163">**ртмжетчанжестатус**</span><span class="sxs-lookup"><span data-stu-id="d7179-163">**RtmGetChangeStatus**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[<span data-ttu-id="d7179-164">**ртммаркдестфорчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-164">**RtmMarkDestForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[<span data-ttu-id="d7179-165">**ртмисмаркедфорчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-165">**RtmIsMarkedForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[<span data-ttu-id="d7179-166">**ртмдерегистерфромчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="d7179-166">**RtmDeregisterFromChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a><span data-ttu-id="d7179-167">Функция списка маршрутов</span><span class="sxs-lookup"><span data-stu-id="d7179-167">Route List Function</span></span>

[<span data-ttu-id="d7179-168">**ртмкреатераутелист**</span><span class="sxs-lookup"><span data-stu-id="d7179-168">**RtmCreateRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[<span data-ttu-id="d7179-169">**ртминсертинраутелист**</span><span class="sxs-lookup"><span data-stu-id="d7179-169">**RtmInsertInRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[<span data-ttu-id="d7179-170">**ртмкреатераутелистенум**</span><span class="sxs-lookup"><span data-stu-id="d7179-170">**RtmCreateRouteListEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[<span data-ttu-id="d7179-171">**ртмжетлистенумраутес**</span><span class="sxs-lookup"><span data-stu-id="d7179-171">**RtmGetListEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[<span data-ttu-id="d7179-172">**ртмделетераутелист**</span><span class="sxs-lookup"><span data-stu-id="d7179-172">**RtmDeleteRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a><span data-ttu-id="d7179-173">Функции управления обработчиками</span><span class="sxs-lookup"><span data-stu-id="d7179-173">Handle Management Functions</span></span>

[<span data-ttu-id="d7179-174">**ртмреференцехандлес**</span><span class="sxs-lookup"><span data-stu-id="d7179-174">**RtmReferenceHandles**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




