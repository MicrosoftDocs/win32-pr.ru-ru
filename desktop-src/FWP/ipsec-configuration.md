---
title: Конфигурация IPsec
description: Платформа фильтрации Windows (WFP) — это базовая платформа для брандмауэра Windows в повышенной безопасности.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987452"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="95a6a-103">Конфигурация IPsec</span><span class="sxs-lookup"><span data-stu-id="95a6a-103">IPsec Configuration</span></span>

<span data-ttu-id="95a6a-104">Платформа фильтрации Windows (WFP) — это базовая платформа для брандмауэра Windows в повышенной безопасности.</span><span class="sxs-lookup"><span data-stu-id="95a6a-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="95a6a-105">WFP используется для настройки правил фильтрации сети, в том числе правил, регулирующих защиту сетевого трафика с помощью IPsec.</span><span class="sxs-lookup"><span data-stu-id="95a6a-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="95a6a-106">Разработчики приложений могут настроить IPsec напрямую с помощью API WFP, чтобы использовать более детализированную модель фильтрации сетевого трафика, чем модель, доступную через оснастку консоли управления (MMC) для брандмауэра Windows в режиме повышенной безопасности.</span><span class="sxs-lookup"><span data-stu-id="95a6a-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="95a6a-107">Что такое IPsec</span><span class="sxs-lookup"><span data-stu-id="95a6a-107">What is IPsec</span></span>

<span data-ttu-id="95a6a-108">Internet Protocol Security (IPsec) — это набор протоколов безопасности, используемых для обеспечения конфиденциальности IP-пакетов по Интернету.</span><span class="sxs-lookup"><span data-stu-id="95a6a-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="95a6a-109">Протокол IPsec обязателен для всех реализаций IPv6 и необязателен для IPv4.</span><span class="sxs-lookup"><span data-stu-id="95a6a-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="95a6a-110">В защищенном IP-трафике есть два дополнительных заголовка IPsec, которые указывают типы криптографической защиты, применяемые к пакету IP, и включают сведения для декодирования защищенного пакета.</span><span class="sxs-lookup"><span data-stu-id="95a6a-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="95a6a-111">Заголовок ESP используется для обеспечения конфиденциальности и защиты от вредоносных изменений путем выполнения проверки подлинности и дополнительного шифрования.</span><span class="sxs-lookup"><span data-stu-id="95a6a-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="95a6a-112">Его можно использовать для трафика, который проходит через маршрутизаторы преобразования сетевых адресов (NAT).</span><span class="sxs-lookup"><span data-stu-id="95a6a-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="95a6a-113">Заголовок Authentication (AH) используется только для защиты от вредоносных изменений путем выполнения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="95a6a-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="95a6a-114">Его нельзя использовать для трафика, который проходит через маршрутизаторы NAT.</span><span class="sxs-lookup"><span data-stu-id="95a6a-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="95a6a-115">Дополнительные сведения о протоколе IPsec см. в разделе также:</span><span class="sxs-lookup"><span data-stu-id="95a6a-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="95a6a-116">[Технический справочник по IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="95a6a-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="95a6a-117">Что такое IKE</span><span class="sxs-lookup"><span data-stu-id="95a6a-117">What is IKE</span></span>

<span data-ttu-id="95a6a-118">Протокол IKE (IKE) — это протокол обмена ключами, который является частью набора протоколов IPsec.</span><span class="sxs-lookup"><span data-stu-id="95a6a-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="95a6a-119">IKE используется при настройке безопасного подключения и выполнении безопасного обмена секретными ключами и другими параметрами, связанными с защитой, без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="95a6a-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="95a6a-120">Дополнительные сведения о IKE см. также в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="95a6a-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="95a6a-121">[протокол IKE](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="95a6a-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="95a6a-122">Что такое AuthIP</span><span class="sxs-lookup"><span data-stu-id="95a6a-122">What is AuthIP</span></span>

<span data-ttu-id="95a6a-123">Протокол AuthIP — это новый протокол обмена ключами, который расширяет IKE следующим образом.</span><span class="sxs-lookup"><span data-stu-id="95a6a-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="95a6a-124">Хотя IKE поддерживает только учетные данные проверки подлинности компьютера, AuthIP также поддерживает:</span><span class="sxs-lookup"><span data-stu-id="95a6a-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="95a6a-125">Учетные данные пользователя: NTLM, Kerberos, сертификаты.</span><span class="sxs-lookup"><span data-stu-id="95a6a-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="95a6a-126">Сертификаты работоспособности защиты доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="95a6a-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="95a6a-127">Анонимные учетные данные, используемые для дополнительной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="95a6a-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="95a6a-128">Сочетание учетных данных; Например, сочетание учетных данных компьютера и пользователя Kerberos.</span><span class="sxs-lookup"><span data-stu-id="95a6a-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="95a6a-129">AuthIP использует механизм повторной проверки подлинности, который проверяет все настроенные методы проверки подлинности до сбоя подключения.</span><span class="sxs-lookup"><span data-stu-id="95a6a-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="95a6a-130">AuthIP можно использовать с защищенными сокетами для реализации защищенного трафика IPsec на основе приложений.</span><span class="sxs-lookup"><span data-stu-id="95a6a-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="95a6a-131">Консоль предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="95a6a-131">It provides:</span></span>

-   <span data-ttu-id="95a6a-132">Проверка подлинности и шифрование для каждого сокета.</span><span class="sxs-lookup"><span data-stu-id="95a6a-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="95a6a-133">Дополнительные сведения см. в разделе [**всасетсоккетсекурити**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .</span><span class="sxs-lookup"><span data-stu-id="95a6a-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="95a6a-134">Олицетворение клиента.</span><span class="sxs-lookup"><span data-stu-id="95a6a-134">Client impersonation.</span></span> <span data-ttu-id="95a6a-135">(IPsec олицетворяет контекст безопасности, в котором создан сокет.)</span><span class="sxs-lookup"><span data-stu-id="95a6a-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="95a6a-136">Проверка имени входящей и исходящей одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="95a6a-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="95a6a-137">Дополнительные сведения см. в разделе [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .</span><span class="sxs-lookup"><span data-stu-id="95a6a-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="95a6a-138">Дополнительные сведения об AuthIP см. также в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="95a6a-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="95a6a-139">AuthIP в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95a6a-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="95a6a-140">Что такое политика IPsec</span><span class="sxs-lookup"><span data-stu-id="95a6a-140">What is an IPsec Policy</span></span>

<span data-ttu-id="95a6a-141">Политика IPsec — это набор правил, определяющих, какой тип IP-трафика должен быть защищен с помощью IPsec, и как защитить этот трафик.</span><span class="sxs-lookup"><span data-stu-id="95a6a-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="95a6a-142">Только одна политика IPsec активна на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="95a6a-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="95a6a-143">Чтобы узнать больше о реализации политик IPsec, откройте оснастку MMC "Локальная политика безопасности" (secpol. msc), нажмите клавишу F1, чтобы открыть справку, а затем выберите Создание и использование политик IPsec в содержании.</span><span class="sxs-lookup"><span data-stu-id="95a6a-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="95a6a-144">Дополнительные сведения о политиках IPsec см. также в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="95a6a-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="95a6a-145">[Обзор основных понятий политики IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="95a6a-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="95a6a-146">[Описание политики IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="95a6a-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="95a6a-147">Использование WFP для настройки политик IPsec</span><span class="sxs-lookup"><span data-stu-id="95a6a-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="95a6a-148">Реализация IPsec в корпорации Майкрософт использует платформу фильтрации Windows для настройки политик IPsec.</span><span class="sxs-lookup"><span data-stu-id="95a6a-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="95a6a-149">Политики IPsec реализуются путем добавления фильтров на различных уровнях WFP следующим образом.</span><span class="sxs-lookup"><span data-stu-id="95a6a-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="95a6a-150">На слоях ФВПМ в версии \_ \_ \_ {4 \| 6} слоев добавляются фильтры, задающих политики согласования, используемые модулями ключей (IKE/AuthIP) во время обмена данными в основном режиме (mm).</span><span class="sxs-lookup"><span data-stu-id="95a6a-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="95a6a-151">Методы проверки подлинности и криптографические алгоритмы указаны на этих уровнях.</span><span class="sxs-lookup"><span data-stu-id="95a6a-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="95a6a-152">На слоях ФВПМ \_ Layer \_ IPSec \_ V {4 \| 6} добавьте фильтры, задающих политики согласования, используемые модулями ключей во время обмена быстрым режимом (QM) и расширенного режима (EM).</span><span class="sxs-lookup"><span data-stu-id="95a6a-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="95a6a-153">Заголовки IPsec (AH/ESP) и алгоритмы шифрования указаны на этих уровнях.</span><span class="sxs-lookup"><span data-stu-id="95a6a-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="95a6a-154">Политика согласования указывается в качестве контекста поставщика политики, связанного с фильтром.</span><span class="sxs-lookup"><span data-stu-id="95a6a-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="95a6a-155">Модуль ключа перечисляет контексты поставщика политики на основе характеристик трафика и получает политику, используемую для согласования безопасности.</span><span class="sxs-lookup"><span data-stu-id="95a6a-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="95a6a-156">API WFP можно использовать для непосредственного указания сопоставлений безопасности (SAs) и, следовательно, для игнорирования политики согласования модуля создания ключей.</span><span class="sxs-lookup"><span data-stu-id="95a6a-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="95a6a-157">На слоях \_ фвпм \_ входящего \_ транспорта \_ v {4 \| 6} и фвпм \_ уровня " \_ исходящий \_ транспорт \_ v {4 \| 6}" добавьте фильтры, которые вызывают выноски, и определите, какой поток трафика следует защищать.</span><span class="sxs-lookup"><span data-stu-id="95a6a-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="95a6a-158">На уровне ФВПМ \_ \_ \_ проверки подлинности \_ recv \_ Accept \_ V {4 \| 6} слои добавляют фильтры, реализующие фильтрацию удостоверений и политику для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="95a6a-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="95a6a-159">На следующей схеме показано взаимодействие различных компонентов платформы WFP по отношению к операциям IPsec.</span><span class="sxs-lookup"><span data-stu-id="95a6a-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![конфигурация IPSec с использованием платформы фильтрации Windows](images/ipsec-configuration.jpg)

<span data-ttu-id="95a6a-161">После настройки IPsec она интегрируется с WFP и расширяет возможности фильтрации WFP, предоставляя сведения для использования в качестве условий фильтрации на уровнях авторизации уровня приложения (ALE).</span><span class="sxs-lookup"><span data-stu-id="95a6a-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="95a6a-162">Например, IPsec предоставляет удаленный пользователь и удостоверение удаленного компьютера, что WFP предоставляет уровни авторизации ALE Connect и Accept.</span><span class="sxs-lookup"><span data-stu-id="95a6a-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="95a6a-163">Эти сведения можно использовать для детальной авторизации удаленных удостоверений с помощью реализации брандмауэра на основе WFP.</span><span class="sxs-lookup"><span data-stu-id="95a6a-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="95a6a-164">Ниже приведен пример политики изоляции, которую можно реализовать с помощью IPsec:</span><span class="sxs-lookup"><span data-stu-id="95a6a-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="95a6a-165">ФВПМ \_ слоя \_ " \_ {4 \| 6} уровни" — Проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="95a6a-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="95a6a-166">\_Уровни фвпм \_ IPSec \_ V {4 \| 6} слои — AH/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="95a6a-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="95a6a-167">\_Уровень фвпм \_ входящего \_ транспорта \_ v {4 \| 6} и фвпм \_ уровня \_ исходящего \_ транспорта \_ v {4 \| 6} — Обнаружение согласований для всего сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="95a6a-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="95a6a-168">ФВПМ \_ уровня \_ \_ проверки подлинности \_ recv \_ Accept \_ V {4 \| 6} уровней: IPSec требуется для всего сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="95a6a-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95a6a-169">См. также</span><span class="sxs-lookup"><span data-stu-id="95a6a-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95a6a-170">**Уровни WFP**</span><span class="sxs-lookup"><span data-stu-id="95a6a-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="95a6a-171">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="95a6a-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="95a6a-172">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="95a6a-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="95a6a-173">**Сценарии политики IPsec, реализованные с помощью API WFP:**</span><span class="sxs-lookup"><span data-stu-id="95a6a-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="95a6a-174">транспортный режим</span><span class="sxs-lookup"><span data-stu-id="95a6a-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="95a6a-175">Транспортный режим обнаружения согласований</span><span class="sxs-lookup"><span data-stu-id="95a6a-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="95a6a-176">Транспортный режим обнаружения согласований в режиме границ</span><span class="sxs-lookup"><span data-stu-id="95a6a-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="95a6a-177">Туннельный режим</span><span class="sxs-lookup"><span data-stu-id="95a6a-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="95a6a-178">Гарантированное шифрование</span><span class="sxs-lookup"><span data-stu-id="95a6a-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="95a6a-179">Удаленная авторизация идентификации</span><span class="sxs-lookup"><span data-stu-id="95a6a-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="95a6a-180">SAs вручную IPsec</span><span class="sxs-lookup"><span data-stu-id="95a6a-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="95a6a-181">Исключения IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="95a6a-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="95a6a-182">**Решения IPsec:**</span><span class="sxs-lookup"><span data-stu-id="95a6a-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="95a6a-183">[Изоляция серверов и доменов](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="95a6a-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 