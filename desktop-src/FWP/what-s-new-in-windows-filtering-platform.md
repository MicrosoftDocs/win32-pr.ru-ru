---
title: Новые возможности платформы фильтрации Windows
description: Windows 8 и Windows Server 2012 представляют новые элементы программирования платформы фильтрации Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339875"
---
# <a name="whats-new-in-windows-filtering-platform"></a><span data-ttu-id="40983-103">Новые возможности платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="40983-103">What's New in Windows Filtering Platform</span></span>

<span data-ttu-id="40983-104">Windows 8 и Windows Server 2012 представляют новые элементы программирования платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="40983-104">Windows 8 and Windows Server 2012 introduce new Windows Filtering Platform programming elements.</span></span> <span data-ttu-id="40983-105">Новые функции включают следующие:</span><span class="sxs-lookup"><span data-stu-id="40983-105">New functionality includes the following:</span></span>

-   <span data-ttu-id="40983-106">*Фильтрация уровня 2*: обеспечивает доступ к уровню L2 (Mac), позволяя фильтровать трафик на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="40983-106">*Layer 2 filtering*: Provides access to the L2 (MAC) layer, allowing filtering of traffic at that layer.</span></span>
-   <span data-ttu-id="40983-107">*Фильтрация vSwitch*: позволяет проверять и изменять пакеты vSwitch.</span><span class="sxs-lookup"><span data-stu-id="40983-107">*vSwitch filtering*: Allows packets traversing a vSwitch to be inspected and/or modified.</span></span> <span data-ttu-id="40983-108">Фильтры и выноски WFP можно использовать во входных и выходных данных vSwitch.</span><span class="sxs-lookup"><span data-stu-id="40983-108">WFP filters or callouts can be used at the vSwitch ingress and egress.</span></span>
-   <span data-ttu-id="40983-109">*Управление контейнерами приложений*: разрешает доступ к сведениям о контейнерах приложений и проблемах с подключением к сетевой изоляции.</span><span class="sxs-lookup"><span data-stu-id="40983-109">*App container management*: Allows access to information about app containers and network isolation connectivity issues.</span></span>
-   <span data-ttu-id="40983-110">*Обновления IPSec*: расширенные функции IPSec, включая мониторинг состояния подключения, выбор сертификатов и управление ключами.</span><span class="sxs-lookup"><span data-stu-id="40983-110">*IPsec updates*: Extended IPsec functionality including connection state monitoring, certificate selection, and key management.</span></span>

<span data-ttu-id="40983-111">В комплект драйверов для Windows также входит информация об [изменениях в WFP для Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span><span class="sxs-lookup"><span data-stu-id="40983-111">The Windows Driver Kit also includes information on [WFP Changes for Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span></span>

## <a name="windows-8-api-updates"></a><span data-ttu-id="40983-112">Обновления API Windows 8</span><span class="sxs-lookup"><span data-stu-id="40983-112">Windows 8 API updates</span></span>

<span data-ttu-id="40983-113">Для Windows 8 и Windows Server 2012 были добавлены многие новые API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="40983-113">Many new APIs have been added for Windows 8 and Windows Server 2012.</span></span>

## <a name="new-functions"></a><span data-ttu-id="40983-114">Новые функции</span><span class="sxs-lookup"><span data-stu-id="40983-114">New functions</span></span>

-   [<span data-ttu-id="40983-115">**ФВПМ \_ net \_ event \_ CALLBACK1**</span><span class="sxs-lookup"><span data-stu-id="40983-115">**FWPM\_NET\_EVENT\_CALLBACK1**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="40983-116">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="40983-116">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="40983-117">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="40983-117">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="40983-118">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="40983-118">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="40983-119">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="40983-119">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="40983-120">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="40983-120">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="40983-121">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="40983-121">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="40983-122">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-122">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="40983-123">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="40983-123">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="40983-124">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-124">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [<span data-ttu-id="40983-125">**FwpmIPsecTunnelAdd2**</span><span class="sxs-lookup"><span data-stu-id="40983-125">**FwpmIPsecTunnelAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [<span data-ttu-id="40983-126">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="40983-126">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="40983-127">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="40983-127">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="40983-128">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="40983-128">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="40983-129">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="40983-129">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="40983-130">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="40983-130">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="40983-131">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="40983-131">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="40983-132">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="40983-132">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="40983-133">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="40983-133">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="40983-134">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-134">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="40983-135">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-135">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [<span data-ttu-id="40983-136">**IkeextSaEnum2**</span><span class="sxs-lookup"><span data-stu-id="40983-136">**IkeextSaEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [<span data-ttu-id="40983-137">**IkeextSaGetById2**</span><span class="sxs-lookup"><span data-stu-id="40983-137">**IkeextSaGetById2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [<span data-ttu-id="40983-138">**\_ \_ \_ \_ CHECK0 диктофона ключей диспетчера ключей \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-138">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="40983-139">**\_Диспетчер ключей \_ IPSec \_ определяет \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="40983-139">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="40983-140">**\_ \_ \_ Уведомление \_ Key0 диспетчера ключей IPsec**</span><span class="sxs-lookup"><span data-stu-id="40983-140">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="40983-141">**\_ \_ CALLBACK0 контекста SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-141">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="40983-142">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="40983-142">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="40983-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="40983-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="40983-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="40983-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="40983-145">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="40983-145">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="40983-146">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="40983-146">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [<span data-ttu-id="40983-147">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-147">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="40983-148">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="40983-148">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="40983-149">**IPsecSaContextUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="40983-149">**IPsecSaContextUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [<span data-ttu-id="40983-150">**нетворкисолатиондиагносеконнектфаилуреанджетинфо**</span><span class="sxs-lookup"><span data-stu-id="40983-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [<span data-ttu-id="40983-151">**нетворкисолатионенумаппконтаинерс**</span><span class="sxs-lookup"><span data-stu-id="40983-151">**NetworkIsolationEnumAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [<span data-ttu-id="40983-152">**нетворкисолатионенумератеаппконтаинеррулес**</span><span class="sxs-lookup"><span data-stu-id="40983-152">**NetworkIsolationEnumerateAppContainerRules**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [<span data-ttu-id="40983-153">**нетворкисолатионфриаппконтаинерс**</span><span class="sxs-lookup"><span data-stu-id="40983-153">**NetworkIsolationFreeAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [<span data-ttu-id="40983-154">**нетворкисолатионжетаппконтаинерконфиг**</span><span class="sxs-lookup"><span data-stu-id="40983-154">**NetworkIsolationGetAppContainerConfig**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [<span data-ttu-id="40983-155">**нетворкисолатионрегистерфораппконтаинерчанжес**</span><span class="sxs-lookup"><span data-stu-id="40983-155">**NetworkIsolationRegisterForAppContainerChanges**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [<span data-ttu-id="40983-156">**нетворкисолатионсетаппконтаинерконфиг**</span><span class="sxs-lookup"><span data-stu-id="40983-156">**NetworkIsolationSetAppContainerConfig**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [<span data-ttu-id="40983-157">**нетворкисолатионсетупаппконтаинербинариес**</span><span class="sxs-lookup"><span data-stu-id="40983-157">**NetworkIsolationSetupAppContainerBinaries**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [<span data-ttu-id="40983-158">**\_ \_ обратный вызов изменений Pac \_ fn**</span><span class="sxs-lookup"><span data-stu-id="40983-158">**PAC\_CHANGES\_CALLBACK\_FN**</span></span>](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a><span data-ttu-id="40983-159">Новые структуры</span><span class="sxs-lookup"><span data-stu-id="40983-159">New structures</span></span>

-   [<span data-ttu-id="40983-160">**\_METHOD2 проверки подлинности IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="40983-160">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="40983-161">**\_EKUS0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="40983-161">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="40983-162">**\_NAME0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="40983-162">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="40983-163">**\_Добавьте сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="40983-163">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="40983-164">**\_CRITERIA0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="40983-164">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="40983-165">**\_POLICY2 EM для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="40983-165">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="40983-166">**IKEEXT \_ Kerberos \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="40983-166">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="40983-167">**\_POLICY2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="40983-167">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="40983-168">**\_MANAGER0 ключей \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-168">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="40983-169">**\_ \_ CALLBACKS0 ДИСПЕТЧЕРА ключей \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-169">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="40983-170">**\_POLICY1 ключей \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-170">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="40983-171">**\_ \_ CHANGE0 контекста SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-171">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="40983-172">**\_ \_ SUBSCRIPTION0 контекста SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-172">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="40983-173">**\_POLICY2 транспорта \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-173">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="40983-174">**\_ENDPOINT0 туннеля \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-174">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="40983-175">**\_ENDPOINTS2 туннеля \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-175">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="40983-176">**\_POLICY2 туннеля \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-176">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="40983-177">**ФВПМ \_ CONNECTION0**</span><span class="sxs-lookup"><span data-stu-id="40983-177">**FWPM\_CONNECTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [<span data-ttu-id="40983-178">**\_ \_ Перечисление \_ TEMPLATE0 подключения фвпм**</span><span class="sxs-lookup"><span data-stu-id="40983-178">**FWPM\_CONNECTION\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [<span data-ttu-id="40983-179">**ФВПМ \_ подключение \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="40983-179">**FWPM\_CONNECTION\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [<span data-ttu-id="40983-180">**ФВПМ \_ net \_ EVENT2**</span><span class="sxs-lookup"><span data-stu-id="40983-180">**FWPM\_NET\_EVENT2**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [<span data-ttu-id="40983-181">**\_ALLOW0 фвпм NET, \_ возможности для событий \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40983-181">**FWPM\_NET\_EVENT\_CAPABILITY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [<span data-ttu-id="40983-182">**\_DROP0 фвпм NET, \_ возможности для событий \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40983-182">**FWPM\_NET\_EVENT\_CAPABILITY\_DROP0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [<span data-ttu-id="40983-183">**ФВПМ \_ net \_ event \_ классифицировать \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="40983-183">**FWPM\_NET\_EVENT\_CLASSIFY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [<span data-ttu-id="40983-184">**ФВПМ \_ net \_ event \_ классифицировать \_ DROP2**</span><span class="sxs-lookup"><span data-stu-id="40983-184">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [<span data-ttu-id="40983-185">**ФВПМ \_ net \_ event \_ классификация \_ DROP \_ MAC0**</span><span class="sxs-lookup"><span data-stu-id="40983-185">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP\_MAC0**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [<span data-ttu-id="40983-186">**ФВПМ \_ net \_ event \_ HEADER2**</span><span class="sxs-lookup"><span data-stu-id="40983-186">**FWPM\_NET\_EVENT\_HEADER2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [<span data-ttu-id="40983-187">**\_CONTEXT2 поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="40983-187">**FWPM\_PROVIDER\_CONTEXT2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [<span data-ttu-id="40983-188">**ФВПМ \_ VSWITCH \_ EVENT0**</span><span class="sxs-lookup"><span data-stu-id="40983-188">**FWPM\_VSWITCH\_EVENT0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [<span data-ttu-id="40983-189">**\_ \_ SUBSCRIPTION0 события фвпм \_ VSWITCH**</span><span class="sxs-lookup"><span data-stu-id="40983-189">**FWPM\_VSWITCH\_EVENT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a><span data-ttu-id="40983-190">Новые перечислимые типы</span><span class="sxs-lookup"><span data-stu-id="40983-190">New enumerated types</span></span>

-   [<span data-ttu-id="40983-191">**\_ \_ тип сети VSWITCH \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="40983-191">**FWP\_VSWITCH\_NETWORK\_TYPE**</span></span>](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [<span data-ttu-id="40983-192">**\_ \_ \_ Тип возможности сети фвпм \_ APPC**</span><span class="sxs-lookup"><span data-stu-id="40983-192">**FWPM\_APPC\_NETWORK\_CAPABILITY\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [<span data-ttu-id="40983-193">**\_ \_ Тип события подключения \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="40983-193">**FWPM\_CONNECTION\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [<span data-ttu-id="40983-194">**\_ \_ Тип события фвпм \_ VSWITCH**</span><span class="sxs-lookup"><span data-stu-id="40983-194">**FWPM\_VSWITCH\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [<span data-ttu-id="40983-195">**\_ \_ тип имени критерия сертификата IKEEXT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40983-195">**IKEEXT\_CERT\_CRITERIA\_NAME\_TYPE**</span></span>](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [<span data-ttu-id="40983-196">**\_ \_ \_ TYPE0 события контекста SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="40983-196">**IPSEC\_SA\_CONTEXT\_EVENT\_TYPE0**</span></span>](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a><span data-ttu-id="40983-197">Новые идентификаторы слоя фильтрации</span><span class="sxs-lookup"><span data-stu-id="40983-197">New filtering layer identifiers</span></span>

[<span data-ttu-id="40983-198">**Фильтрация идентификаторов слоя:**</span><span class="sxs-lookup"><span data-stu-id="40983-198">**Filtering Layer Identifiers:**</span></span>](management-filtering-layer-identifiers-.md)

-   <span data-ttu-id="40983-199">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="40983-199">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="40983-200">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-200">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="40983-201">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-201">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="40983-202">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-202">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="40983-203">уровень ФВПМ входящий трафик \_ \_ \_ VSWITCH \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="40983-203">FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="40983-204">исходящий слой ФВПМ для \_ \_ \_ vSwitch \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="40983-204">FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="40983-205">Уровень \_ фвпм \_ входящего трафика \_ VSWITCH \_ \_ v4/фвпм, входящий в \_ \_ \_ транспорт vSwitch \_ \_ версии 6</span><span class="sxs-lookup"><span data-stu-id="40983-205">FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>
-   <span data-ttu-id="40983-206">Исходящий уровень ФВПМ, \_ \_ \_ \_ транспорт vSwitch v4/фвпм, исходящий \_ \_ \_ \_ \_ транспорт vSwitch \_ версии 6</span><span class="sxs-lookup"><span data-stu-id="40983-206">FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>

## <a name="new-filtering-condition-identifiers"></a><span data-ttu-id="40983-207">Новые идентификаторы условий фильтрации</span><span class="sxs-lookup"><span data-stu-id="40983-207">New filtering condition identifiers</span></span>

[<span data-ttu-id="40983-208">**Фильтрация идентификаторов условий:**</span><span class="sxs-lookup"><span data-stu-id="40983-208">**Filtering Condition Identifiers:**</span></span>](filtering-condition-identifiers-.md)

-   <span data-ttu-id="40983-209">\_ \_ \_ MAC-адрес интерфейса условия фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-209">FWPM\_CONDITION\_INTERFACE\_MAC\_ADDRESS</span></span>
-   <span data-ttu-id="40983-210">\_ \_ \_ локальный \_ адрес Mac условия фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-210">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS</span></span>
-   <span data-ttu-id="40983-211">\_ \_ \_ Удаленный адрес фвпм условия \_ Mac</span><span class="sxs-lookup"><span data-stu-id="40983-211">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS</span></span>
-   <span data-ttu-id="40983-212">\_ \_ тип ETHER условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-212">FWPM\_CONDITION\_ETHER\_TYPE</span></span>
-   <span data-ttu-id="40983-213">\_ \_ ИД виртуальной ЛС для условия фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-213">FWPM\_CONDITION\_VLAN\_ID</span></span>
-   <span data-ttu-id="40983-214">\_ \_ порт NDIS условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-214">FWPM\_CONDITION\_NDIS\_PORT</span></span>
-   <span data-ttu-id="40983-215">\_ \_ \_ тип носителя NDIS условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-215">FWPM\_CONDITION\_NDIS\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="40983-216">\_ \_ \_ \_ тип физического носителя \_ для условия фвпм NDIS</span><span class="sxs-lookup"><span data-stu-id="40983-216">FWPM\_CONDITION\_NDIS\_PHYSICAL\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="40983-217">\_ \_ Флаги фвпм условия L2 \_</span><span class="sxs-lookup"><span data-stu-id="40983-217">FWPM\_CONDITION\_L2\_FLAGS</span></span>
-   <span data-ttu-id="40983-218">\_ \_ \_ \_ тип ЛОКАЛЬНОГО адреса Mac условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-218">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="40983-219">\_ \_ \_ \_ Тип удаленного адреса Mac условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-219">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="40983-220">\_ \_ \_ идентификатор пакета ALE фвпм \_ Condition</span><span class="sxs-lookup"><span data-stu-id="40983-220">FWPM\_CONDITION\_ALE\_PACKAGE\_ID</span></span>
-   <span data-ttu-id="40983-221">\_ \_ Исходный Mac- \_ \_ адрес условия фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-221">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS</span></span>
-   <span data-ttu-id="40983-222">ФВПМ \_ условие для \_ Mac- \_ \_ адреса назначения</span><span class="sxs-lookup"><span data-stu-id="40983-222">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS</span></span>
-   <span data-ttu-id="40983-223">\_ \_ \_ \_ тип ИСХОДНОГО адреса Mac условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="40983-223">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="40983-224">\_ \_ \_ \_ тип адреса назначения для фвпм условия Mac \_</span><span class="sxs-lookup"><span data-stu-id="40983-224">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="40983-225">\_ \_ Исходный IP-адрес условия \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-225">FWPM\_CONDITION\_IP\_SOURCE\_PORT</span></span>
-   <span data-ttu-id="40983-226">\_ \_ порт назначения IP-адреса фвпм Condition \_ \_</span><span class="sxs-lookup"><span data-stu-id="40983-226">FWPM\_CONDITION\_IP\_DESTINATION\_PORT</span></span>
-   <span data-ttu-id="40983-227">Идентификатор ФВПМ для \_ состояния \_ VSWITCH \_</span><span class="sxs-lookup"><span data-stu-id="40983-227">FWPM\_CONDITION\_VSWITCH\_ID</span></span>
-   <span data-ttu-id="40983-228">\_ \_ \_ тип сети VSWITCH фвпм \_ Condition</span><span class="sxs-lookup"><span data-stu-id="40983-228">FWPM\_CONDITION\_VSWITCH\_NETWORK\_TYPE</span></span>
-   <span data-ttu-id="40983-229">ФВПМ \_ условие \_ \_ идентификации исходного \_ интерфейса \_ VSWITCH</span><span class="sxs-lookup"><span data-stu-id="40983-229">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="40983-230">\_ \_ \_ \_ идентификатор конечного интерфейса VSWITCH \_ для фвпм условия</span><span class="sxs-lookup"><span data-stu-id="40983-230">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="40983-231">ФВПМ \_ условие \_ с \_ \_ идентификатором исходной виртуальной машины VSWITCH \_</span><span class="sxs-lookup"><span data-stu-id="40983-231">FWPM\_CONDITION\_VSWITCH\_SOURCE\_VM\_ID</span></span>
-   <span data-ttu-id="40983-232">ФВПМ \_ условие \_ , \_ \_ идентификатор целевой виртуальной машины VSWITCH \_</span><span class="sxs-lookup"><span data-stu-id="40983-232">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_VM\_ID</span></span>
-   <span data-ttu-id="40983-233">ФВПМ \_ условие \_ , \_ \_ Тип исходного интерфейса \_ VSWITCH</span><span class="sxs-lookup"><span data-stu-id="40983-233">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_TYPE</span></span>
-   <span data-ttu-id="40983-234">\_ \_ \_ \_ идентификатор сети клиента VSWITCH с условием фвпм \_</span><span class="sxs-lookup"><span data-stu-id="40983-234">FWPM\_CONDITION\_VSWITCH\_TENANT\_NETWORK\_ID</span></span>

## <a name="new-filtering-condition-flags"></a><span data-ttu-id="40983-235">Новые флаги условий фильтрации</span><span class="sxs-lookup"><span data-stu-id="40983-235">New filtering condition flags</span></span>

[<span data-ttu-id="40983-236">**Флаги условия фильтрации:**</span><span class="sxs-lookup"><span data-stu-id="40983-236">**Filtering Condition Flags:**</span></span>](filtering-condition-flags-.md)

-   <span data-ttu-id="40983-237">\_флаг условия \_ FWP \_ является \_ прокси- \_ соединением</span><span class="sxs-lookup"><span data-stu-id="40983-237">FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION</span></span>
-   <span data-ttu-id="40983-238">\_флаг условия \_ FWP \_ — \_ это \_ замыкание APPCONTAINER</span><span class="sxs-lookup"><span data-stu-id="40983-238">FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="40983-239">\_флаг условия \_ FWP \_ не \_ является \_ \_ замыканием APPCONTAINER</span><span class="sxs-lookup"><span data-stu-id="40983-239">FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="40983-240">\_флаг условия \_ FWP \_ \_ учитывает \_ политику \_ авторизации</span><span class="sxs-lookup"><span data-stu-id="40983-240">FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE</span></span>
-   <span data-ttu-id="40983-241">\_Условие FWP \_ L2 \_ — \_ собственная \_ сеть Ethernet</span><span class="sxs-lookup"><span data-stu-id="40983-241">FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET</span></span>
-   <span data-ttu-id="40983-242">\_Условие FWP \_ L2 \_ — \_ Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="40983-242">FWP\_CONDITION\_L2\_IS\_WIFI</span></span>
-   <span data-ttu-id="40983-243">\_Условие FWP \_ L2 \_ — \_ мобильное \_ широкополосное подключение</span><span class="sxs-lookup"><span data-stu-id="40983-243">FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND</span></span>
-   <span data-ttu-id="40983-244">\_Условие FWP \_ L2 \_ — \_ \_ прямые \_ данные WiFi</span><span class="sxs-lookup"><span data-stu-id="40983-244">FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA</span></span>
-   <span data-ttu-id="40983-245">\_Условие FWP \_ L2 \_ — \_ VM2VM</span><span class="sxs-lookup"><span data-stu-id="40983-245">FWP\_CONDITION\_L2\_IS\_VM2VM</span></span>
-   <span data-ttu-id="40983-246">\_Условие FWP \_ L2 \_ имеет \_ неправильный формат \_ пакета</span><span class="sxs-lookup"><span data-stu-id="40983-246">FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET</span></span>
-   <span data-ttu-id="40983-247">\_Условие FWP \_ L2 \_ — \_ \_ Группа фрагментов IP-адресов \_</span><span class="sxs-lookup"><span data-stu-id="40983-247">FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP</span></span>
-   <span data-ttu-id="40983-248">\_Условие FWP \_ L2 \_ , \_ Если \_ имеется соединитель</span><span class="sxs-lookup"><span data-stu-id="40983-248">FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT</span></span>

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a><span data-ttu-id="40983-249">Обновления Windows 7 для платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="40983-249">Windows 7 updates to the Windows Filtering Platform</span></span>

<span data-ttu-id="40983-250">В документе « [новые возможности платформы фильтрации Windows]() » подробно описаны многие обновления, внесенные в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40983-250">The document [What's New in Windows Filtering Platform]() details many of the updates made for Windows 7.</span></span> <span data-ttu-id="40983-251">Сведения также доступны в комплекте драйверов Windows на [изменениях WFP для Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span><span class="sxs-lookup"><span data-stu-id="40983-251">Information is also available in the Windows Driver Kit on [WFP Changes for Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span></span>

 

 