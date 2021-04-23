---
title: Методы Ивтспротоколконнектион
description: Интерфейс Ивтспротоколконнектион предоставляет следующие методы.
ms.assetid: DBB96D6B-F5A5-4CAF-974F-44D76B9CBFB6
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89f63aea6b1904eb4319dcce541aeb4d15d34f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411440"
---
# <a name="iwtsprotocolconnection-methods"></a><span data-ttu-id="54b9f-103">Методы Ивтспротоколконнектион</span><span class="sxs-lookup"><span data-stu-id="54b9f-103">IWTSProtocolConnection Methods</span></span>

<span data-ttu-id="54b9f-104">\[Ивтспротоколконнектион больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="54b9f-104">\[IWTSProtocolConnection is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="54b9f-105">Интерфейс [**ивтспротоколконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="54b9f-105">The [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54b9f-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="54b9f-106">In this section</span></span>

-   [<span data-ttu-id="54b9f-107">**Метод Акцептконнектион**</span><span class="sxs-lookup"><span data-stu-id="54b9f-107">**AcceptConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection)
-   [<span data-ttu-id="54b9f-108">**Метод Аусентикатеклиенттосессион**</span><span class="sxs-lookup"><span data-stu-id="54b9f-108">**AuthenticateClientToSession method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession)
-   [<span data-ttu-id="54b9f-109">**Метод Close**</span><span class="sxs-lookup"><span data-stu-id="54b9f-109">**Close method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close)
-   [<span data-ttu-id="54b9f-110">**Метод Коннектнотифи**</span><span class="sxs-lookup"><span data-stu-id="54b9f-110">**ConnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify)
-   [<span data-ttu-id="54b9f-111">**Метод Креатевиртуалчаннел**</span><span class="sxs-lookup"><span data-stu-id="54b9f-111">**CreateVirtualChannel method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel)
-   [<span data-ttu-id="54b9f-112">**Метод Дисконнектнотифи**</span><span class="sxs-lookup"><span data-stu-id="54b9f-112">**DisconnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify)
-   [<span data-ttu-id="54b9f-113">**Метод Жетклиентдата**</span><span class="sxs-lookup"><span data-stu-id="54b9f-113">**GetClientData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata)
-   [<span data-ttu-id="54b9f-114">**Метод Жетластинпуттиме**</span><span class="sxs-lookup"><span data-stu-id="54b9f-114">**GetLastInputTime method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime)
-   [<span data-ttu-id="54b9f-115">**Метод Жетлиценсеконнектион**</span><span class="sxs-lookup"><span data-stu-id="54b9f-115">**GetLicenseConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection)
-   [<span data-ttu-id="54b9f-116">**Метод Жетлогонеррорредиректор**</span><span class="sxs-lookup"><span data-stu-id="54b9f-116">**GetLogonErrorRedirector method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector)
-   [<span data-ttu-id="54b9f-117">**Метод Жетпротоколхандлес**</span><span class="sxs-lookup"><span data-stu-id="54b9f-117">**GetProtocolHandles method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles)
-   [<span data-ttu-id="54b9f-118">**Метод Жетпротоколстатус**</span><span class="sxs-lookup"><span data-stu-id="54b9f-118">**GetProtocolStatus method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus)
-   [<span data-ttu-id="54b9f-119">**Метод Жетшадовконнектион**</span><span class="sxs-lookup"><span data-stu-id="54b9f-119">**GetShadowConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection)
-   [<span data-ttu-id="54b9f-120">**Метод Жетусеркредентиалс**</span><span class="sxs-lookup"><span data-stu-id="54b9f-120">**GetUserCredentials method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials)
-   [<span data-ttu-id="54b9f-121">**Метод UserData**</span><span class="sxs-lookup"><span data-stu-id="54b9f-121">**GetUserData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata)
-   [<span data-ttu-id="54b9f-122">**Метод Исусералловедтологон**</span><span class="sxs-lookup"><span data-stu-id="54b9f-122">**IsUserAllowedToLogon method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon)
-   [<span data-ttu-id="54b9f-123">**Метод Логоннотифи**</span><span class="sxs-lookup"><span data-stu-id="54b9f-123">**LogonNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify)
-   [<span data-ttu-id="54b9f-124">**Метод Нотифисессионид**</span><span class="sxs-lookup"><span data-stu-id="54b9f-124">**NotifySessionId method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid)
-   [<span data-ttu-id="54b9f-125">**Метод Куерипроперти**</span><span class="sxs-lookup"><span data-stu-id="54b9f-125">**QueryProperty method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)
-   [<span data-ttu-id="54b9f-126">**Метод Сендбип**</span><span class="sxs-lookup"><span data-stu-id="54b9f-126">**SendBeep method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep)
-   [<span data-ttu-id="54b9f-127">**Метод Сендполицидата**</span><span class="sxs-lookup"><span data-stu-id="54b9f-127">**SendPolicyData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata)
-   [<span data-ttu-id="54b9f-128">**Метод Сессионарбитратионенумератион**</span><span class="sxs-lookup"><span data-stu-id="54b9f-128">**SessionArbitrationEnumeration method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration)
-   [<span data-ttu-id="54b9f-129">**SetErrorInfo - метод**</span><span class="sxs-lookup"><span data-stu-id="54b9f-129">**SetErrorInfo method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo)

 

 




