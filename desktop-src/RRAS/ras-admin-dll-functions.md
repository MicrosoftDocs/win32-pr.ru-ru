---
title: Функции DLL администрирования RAS
description: Библиотека DLL администрирования RAS должна реализовывать и экспортировать все следующие функции.
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a02c8dc9212f3cfd173c9a236f81fcf766658424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792973"
---
# <a name="ras-administration-dll-functions"></a><span data-ttu-id="5e3fb-103">Функции DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="5e3fb-103">RAS administration DLL functions</span></span>

<span data-ttu-id="5e3fb-104">Библиотека DLL администрирования RAS должна реализовывать и экспортировать все следующие функции:</span><span class="sxs-lookup"><span data-stu-id="5e3fb-104">A RAS administration DLL must implement and export all of the following functions:</span></span>

-   [<span data-ttu-id="5e3fb-105">**мпрадминакцептневлинк**</span><span class="sxs-lookup"><span data-stu-id="5e3fb-105">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   <span data-ttu-id="5e3fb-106">[**Мпрадминакцептреаусентикатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) или [ **мпрадминакцептреаусентикатионекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) or [**MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span></span>
-   <span data-ttu-id="5e3fb-107">[**Мпрадмининитиализедлл**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) или [ **мпрадмининитиализедллекс**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) or [**MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span></span>
-   [<span data-ttu-id="5e3fb-108">**мпрадминлинкхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="5e3fb-108">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [<span data-ttu-id="5e3fb-109">**мпрадминтерминатедлл**</span><span class="sxs-lookup"><span data-stu-id="5e3fb-109">**MprAdminTerminateDll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

<span data-ttu-id="5e3fb-110">**Windows 2000/NT:** Библиотека DLL администрирования RAS должна также реализовывать и экспортировать следующую пару функций: [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) и [**мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) .</span><span class="sxs-lookup"><span data-stu-id="5e3fb-110">**Windows 2000/NT:** The RAS administration DLL must also implement and export the following pair of functions: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>

<span data-ttu-id="5e3fb-111">Кроме того, Библиотека DLL администрирования RAS должна реализовать и экспортировать одну из следующих пар функций:</span><span class="sxs-lookup"><span data-stu-id="5e3fb-111">In addition, the RAS administration DLL must implement and export one of the following pairs of functions:</span></span>

-   <span data-ttu-id="5e3fb-112">[**Мпрадминакцептневконнектион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) и [ **мпрадминконнектионхангупнотификатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) and [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span></span>
-   <span data-ttu-id="5e3fb-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) и [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) and [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span></span>
-   <span data-ttu-id="5e3fb-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) и [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) and [**MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span></span>
-   <span data-ttu-id="5e3fb-115">[**Мпрадминакцептневконнектионекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) и [ **мпрадминконнектионхангупнотификатионекс**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) and [**MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span></span>

<span data-ttu-id="5e3fb-116">Если одна из требуемых функций не реализована, служба удаленного доступа не запускается.</span><span class="sxs-lookup"><span data-stu-id="5e3fb-116">If one of the required functions is not implemented, the remote access service fails to start.</span></span>

<span data-ttu-id="5e3fb-117">Библиотека DLL администрирования не требуется для реализации следующих пар функций:</span><span class="sxs-lookup"><span data-stu-id="5e3fb-117">An administration DLL is not required to implement the following pairs of functions:</span></span>

-   <span data-ttu-id="5e3fb-118">[**Мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) и [ **мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>
-   <span data-ttu-id="5e3fb-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) и [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span><span class="sxs-lookup"><span data-stu-id="5e3fb-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) and [*MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span></span>

<span data-ttu-id="5e3fb-120">Однако если библиотека DLL реализует одну функцию в приведенной выше паре, она должна также реализовать другую функцию в паре.</span><span class="sxs-lookup"><span data-stu-id="5e3fb-120">However, if the DLL implements one function in a pair listed above, it must implement the other function in the pair as well.</span></span>

<span data-ttu-id="5e3fb-121">Дополнительные сведения о библиотеках DLL администрирования службы удаленного доступа см. в разделе Обзор, [Библиотека DLL администрирования RAS](ras-administration-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5e3fb-121">For more information on RAS Administration DLLs, see the overview topic, [RAS Administration DLL](ras-administration-dll.md).</span></span>

 

 