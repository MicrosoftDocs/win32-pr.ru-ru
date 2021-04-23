---
title: Функции диспетчера групп многоадресной рассылки
description: Для регистрации в диспетчере групп многоадресной рассылки используются следующие функции.
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332123"
---
# <a name="multicast-group-manager-functions"></a><span data-ttu-id="3f178-103">Функции диспетчера групп многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="3f178-103">Multicast Group Manager Functions</span></span>

<span data-ttu-id="3f178-104">Для регистрации в диспетчере групп многоадресной рассылки используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="3f178-104">The following functions are used to register with the multicast group manager:</span></span>

[<span data-ttu-id="3f178-105">**мгмрегистермпротокол**</span><span class="sxs-lookup"><span data-stu-id="3f178-105">**MgmRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[<span data-ttu-id="3f178-106">**мгмдерегистермпротокол**</span><span class="sxs-lookup"><span data-stu-id="3f178-106">**MgmDeRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

<span data-ttu-id="3f178-107">Для управления владением интерфейсом используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="3f178-107">The following functions are used to manage interface ownership:</span></span>

[<span data-ttu-id="3f178-108">**мгмжетпротоколонинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="3f178-108">**MgmGetProtocolOnInterface**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[<span data-ttu-id="3f178-109">**мгмтакеинтерфацеовнершип**</span><span class="sxs-lookup"><span data-stu-id="3f178-109">**MgmTakeInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[<span data-ttu-id="3f178-110">**мгмрелеасеинтерфацеовнершип**</span><span class="sxs-lookup"><span data-stu-id="3f178-110">**MgmReleaseInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

<span data-ttu-id="3f178-111">Для управления членством в группах используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="3f178-111">The following functions are used to manage group membership:</span></span>

[<span data-ttu-id="3f178-112">**мгмаддграупмембершипентри**</span><span class="sxs-lookup"><span data-stu-id="3f178-112">**MgmAddGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[<span data-ttu-id="3f178-113">**мгмделетеграупмембершипентри**</span><span class="sxs-lookup"><span data-stu-id="3f178-113">**MgmDeleteGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

<span data-ttu-id="3f178-114">Для получения записей многоадресной пересылки (мфес) и статистики МФЕ используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="3f178-114">The following functions are used to obtain multicast forwarding entries (MFEs) and MFE statistics:</span></span>

[<span data-ttu-id="3f178-115">**мгмжетфирстмфе**</span><span class="sxs-lookup"><span data-stu-id="3f178-115">**MgmGetFirstMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[<span data-ttu-id="3f178-116">**мгмжетнекстмфе**</span><span class="sxs-lookup"><span data-stu-id="3f178-116">**MgmGetNextMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[<span data-ttu-id="3f178-117">**мгмжетмфе**</span><span class="sxs-lookup"><span data-stu-id="3f178-117">**MgmGetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[<span data-ttu-id="3f178-118">**мгмжетфирстмфестатс**</span><span class="sxs-lookup"><span data-stu-id="3f178-118">**MgmGetFirstMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[<span data-ttu-id="3f178-119">**мгмжетнекстмфестатс**</span><span class="sxs-lookup"><span data-stu-id="3f178-119">**MgmGetNextMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[<span data-ttu-id="3f178-120">**мгмжетмфестатс**</span><span class="sxs-lookup"><span data-stu-id="3f178-120">**MgmGetMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

<span data-ttu-id="3f178-121">Для изменения мфес используется следующая функция:</span><span class="sxs-lookup"><span data-stu-id="3f178-121">The following function is used to modify MFEs:</span></span>

[<span data-ttu-id="3f178-122">**мгмсетмфе**</span><span class="sxs-lookup"><span data-stu-id="3f178-122">**MgmSetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

<span data-ttu-id="3f178-123">Следующие функции используются для получения списка Объединенных групп.</span><span class="sxs-lookup"><span data-stu-id="3f178-123">The following functions are used obtain a list of groups that have been joined:</span></span>

[<span data-ttu-id="3f178-124">**мгмграупенумератионстарт**</span><span class="sxs-lookup"><span data-stu-id="3f178-124">**MgmGroupEnumerationStart**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[<span data-ttu-id="3f178-125">**мгмграупенумератионжетнекст**</span><span class="sxs-lookup"><span data-stu-id="3f178-125">**MgmGroupEnumerationGetNext**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[<span data-ttu-id="3f178-126">**мгмграупенумератионенд**</span><span class="sxs-lookup"><span data-stu-id="3f178-126">**MgmGroupEnumerationEnd**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




