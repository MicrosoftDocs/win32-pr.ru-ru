---
title: Новые возможности управления сетью
description: Новые возможности управления сетью
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104414104"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="fbbc4-103">Новые возможности управления сетью</span><span class="sxs-lookup"><span data-stu-id="fbbc4-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="fbbc4-104">Windows 8 и Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbbc4-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="fbbc4-105">В Microsoft Windows 8 появились новые функции программирования управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="fbbc4-106">Эти новые элементы расширяют возможности управления сетью для создания пакетов подготовки для автономных операций приподключения к домену при подготовке компьютеров с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="fbbc4-107">Ниже перечислены новые функции управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="fbbc4-108">**неткреатепровисионингпаккаже**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="fbbc4-109">**нетрекуестпровисионингпаккажеинсталл**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="fbbc4-110">Ниже приведены новые структуры управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="fbbc4-111">**\_Параметры подготовки нетсетуп \_**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="fbbc4-112">**\_Сведения о пользователе \_ 24**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="fbbc4-113">Функция [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) была улучшена в Windows 8 для поддержки нового уровня информации и возвращения сведений [**\_ о пользователе \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) структура со сведениями об учетной записи пользователя для учетной записи, подключенной к удостоверению Интернета.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="fbbc4-114">Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbbc4-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="fbbc4-115">В Microsoft Windows 7 появились новые функции программирования управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="fbbc4-116">Эти элементы расширяют возможности управления сетью, чтобы разрешить автономные операции присоединение к домену при подготовке компьютеров с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="fbbc4-117">Ниже перечислены новые функции управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="fbbc4-118">**нетпровисионкомпутераккаунт**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="fbbc4-119">**нетрекуестоффлинедомаинжоин**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="fbbc4-120">Следующие существующие функции управления сетью были усовершенствованы для поддержки дополнительных параметров:</span><span class="sxs-lookup"><span data-stu-id="fbbc4-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="fbbc4-121">**нетжоиндомаин**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="fbbc4-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbbc4-122">Windows Server 2003</span></span>

<span data-ttu-id="fbbc4-123">В Microsoft Windows Server 2003 появились новые функции программирования управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="fbbc4-124">Эти элементы расширяют возможности операций управления сетью в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="fbbc4-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbbc4-125">Windows XP</span></span>

<span data-ttu-id="fbbc4-126">В Microsoft Windows XP появились новые функции программирования управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="fbbc4-127">Эти элементы расширяют возможности операций управления сетью в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="fbbc4-128">Ниже перечислены новые функции управления сетью.</span><span class="sxs-lookup"><span data-stu-id="fbbc4-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="fbbc4-129">**нетаддалтернатекомпутернаме**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="fbbc4-130">**нетенумератекомпутернамес**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="fbbc4-131">**нетремовеалтернатекомпутернаме**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="fbbc4-132">**нетсетпримарикомпутернаме**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="fbbc4-133">**сетнетсчедулеаккаунтинформатион**</span><span class="sxs-lookup"><span data-stu-id="fbbc4-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




