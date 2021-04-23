---
title: Методы Win32_TSGatewayServerSettings
description: Класс Win32 \_ тсгатевайсерверсеттингс предоставляет следующие методы.
ms.assetid: BD5A5D8E-2EAE-4806-8DE8-B6B02D9D0402
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388712e8d9244e8d628c72c1fff80e5fc468a466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777744"
---
# <a name="win32_tsgatewayserversettings-methods"></a><span data-ttu-id="c13f8-103">\_Методы тсгатевайсерверсеттингс Win32</span><span class="sxs-lookup"><span data-stu-id="c13f8-103">Win32\_TSGatewayServerSettings Methods</span></span>

<span data-ttu-id="c13f8-104">Класс [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c13f8-104">The [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c13f8-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c13f8-105">In this section</span></span>

-   [<span data-ttu-id="c13f8-106">**Метод Configure**</span><span class="sxs-lookup"><span data-stu-id="c13f8-106">**Configure method**</span></span>](configure-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-107">**Метод Енаблецентралкап**</span><span class="sxs-lookup"><span data-stu-id="c13f8-107">**EnableCentralCAP method**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-108">**Метод Енаблеложевент**</span><span class="sxs-lookup"><span data-stu-id="c13f8-108">**EnableLogEvent method**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-109">**Метод Енаблеонликонсенткапаблеклиентс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-109">**EnableOnlyConsentCapableClients method**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-110">**Метод Енаблетранспорт**</span><span class="sxs-lookup"><span data-stu-id="c13f8-110">**EnableTransport method**</span></span>](enabletransport-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-111">**Метод Енаблерекуестсох**</span><span class="sxs-lookup"><span data-stu-id="c13f8-111">**EnableRequestSOH method**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)
-   [<span data-ttu-id="c13f8-112">**Метод Енумаусентикатионплугинс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-112">**EnumAuthenticationPlugins method**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-113">**Метод Енумаусоризатионплугинс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-113">**EnumAuthorizationPlugins method**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-114">**Метод Жетипандпорт**</span><span class="sxs-lookup"><span data-stu-id="c13f8-114">**GetIPAndPort method**</span></span>](getipandport-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-115">**Метод Жетложевентнаме**</span><span class="sxs-lookup"><span data-stu-id="c13f8-115">**GetLogEventName method**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-116">**Метод Жетпротоколнаме**</span><span class="sxs-lookup"><span data-stu-id="c13f8-116">**GetProtocolName method**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-117">**Метод Исложевентенаблед**</span><span class="sxs-lookup"><span data-stu-id="c13f8-117">**IsLogEventEnabled method**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-118">**Метод Истранспортенаблед**</span><span class="sxs-lookup"><span data-stu-id="c13f8-118">**IsTransportEnabled method**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-119">**Метод Куерицертконтекст**</span><span class="sxs-lookup"><span data-stu-id="c13f8-119">**QueryCertContext method**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)
-   [<span data-ttu-id="c13f8-120">**Метод Рециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-120">**RecycleRpcApplicationPools method**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-121">**Метод Рефрешцертконтекст**</span><span class="sxs-lookup"><span data-stu-id="c13f8-121">**RefreshCertContext method**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)
-   [<span data-ttu-id="c13f8-122">**Метод Сетаусентикатионплугин**</span><span class="sxs-lookup"><span data-stu-id="c13f8-122">**SetAuthenticationPlugin method**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-123">**Метод Сетаусентикатионплугинандрециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-123">**SetAuthenticationPluginAndRecycleRpcApplicationPools method**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-124">**Метод Сетаусоризатионплугин**</span><span class="sxs-lookup"><span data-stu-id="c13f8-124">**SetAuthorizationPlugin method**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-125">**Метод Сетдефаултплугинсандрециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-125">**SetDefaultPluginsAndRecycleRpcApplicationPools method**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-126">**Метод Сетцертификате**</span><span class="sxs-lookup"><span data-stu-id="c13f8-126">**SetCertificate method**</span></span>](setcertificate-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-127">**Метод Сетцертификатеакл**</span><span class="sxs-lookup"><span data-stu-id="c13f8-127">**SetCertificateACL method**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-128">**Метод Сетенфорцечаннелбиндинг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-128">**SetEnforceChannelBinding method**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-129">**Метод Сетипандпорт**</span><span class="sxs-lookup"><span data-stu-id="c13f8-129">**SetIPAndPort method**</span></span>](setipandport-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-130">**Метод Сетсслбридгинг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-130">**SetSslBridging method**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-131">**Метод Сетмаксконнектионс**</span><span class="sxs-lookup"><span data-stu-id="c13f8-131">**SetMaxConnections method**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-132">**Метод Тсгремовеадминмсг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-132">**TSGRemoveAdminMsg method**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-133">**Метод Тсгремовеконсентмсг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-133">**TSGRemoveConsentMsg method**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-134">**Метод Тсгстореадминмсг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-134">**TSGStoreAdminMsg method**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)
-   [<span data-ttu-id="c13f8-135">**Метод Тсгстореконсентмсг**</span><span class="sxs-lookup"><span data-stu-id="c13f8-135">**TSGStoreConsentMsg method**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)

 

 




