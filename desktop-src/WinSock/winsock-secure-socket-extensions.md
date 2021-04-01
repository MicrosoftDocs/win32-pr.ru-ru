---
description: Расширения защищенных сокетов для Winsock позволяют приложению сокета управлять безопасностью трафика по сети.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Расширения безопасных сокетов Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072736"
---
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="31799-103">Расширения безопасных сокетов Winsock</span><span class="sxs-lookup"><span data-stu-id="31799-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="31799-104">Расширения защищенных сокетов для Winsock позволяют приложению сокета управлять безопасностью трафика по сети.</span><span class="sxs-lookup"><span data-stu-id="31799-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="31799-105">Эти расширения позволяют приложению предоставлять политику безопасности и требования к сетевому трафику, а также запрашивать примененные параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="31799-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="31799-106">Например, приложение может использовать эти расширения для запроса маркера безопасности однорангового узла, который можно использовать для проверки доступа на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="31799-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="31799-107">Расширения SSL предназначены для интеграции служб, предоставляемых протоколом IPsec и другими протоколами безопасности, с платформой Winsock Framework.</span><span class="sxs-lookup"><span data-stu-id="31799-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="31799-108">До Windows Vista, в Windows Server 2003 и Windows XP, IPsec был настроен администратором с помощью локальных политик и политики домена.</span><span class="sxs-lookup"><span data-stu-id="31799-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="31799-109">В Windows Vista расширения безопасных сокетов позволяют приложениям полностью или частично настраивать и контролировать безопасность своего сетевого трафика на уровне сокета.</span><span class="sxs-lookup"><span data-stu-id="31799-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="31799-110">Приложения могут уже защищать сетевой трафик с помощью общедоступных API, таких как Управление IPsec, платформа фильтрации Windows и интерфейс поставщика поддержки безопасности (SSPI).</span><span class="sxs-lookup"><span data-stu-id="31799-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="31799-111">Однако использование этих API может усложнить разработку приложения и может усложнить настройку и развертывание.</span><span class="sxs-lookup"><span data-stu-id="31799-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="31799-112">Расширения для безопасного сокета WinSock предназначены для упрощения разработки сетевых приложений, требующих безопасного сетевого трафика путем предоставления Winsock большей части сложности.</span><span class="sxs-lookup"><span data-stu-id="31799-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="31799-113">Эти расширения SSL доступны в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="31799-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="31799-114">Функции защищенного сокета</span><span class="sxs-lookup"><span data-stu-id="31799-114">Secure Socket Functions</span></span>

<span data-ttu-id="31799-115">Существуют следующие функции расширения SSL.</span><span class="sxs-lookup"><span data-stu-id="31799-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="31799-116">**всаделетесоккетпиртаржетнаме**</span><span class="sxs-lookup"><span data-stu-id="31799-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="31799-117">**всаимперсонатесоккетпир**</span><span class="sxs-lookup"><span data-stu-id="31799-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="31799-118">**всакуерисоккетсекурити**</span><span class="sxs-lookup"><span data-stu-id="31799-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="31799-119">**всаревертимперсонатион**</span><span class="sxs-lookup"><span data-stu-id="31799-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="31799-120">**всасетсоккетпиртаржетнаме**</span><span class="sxs-lookup"><span data-stu-id="31799-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="31799-121">**всасетсоккетсекурити**</span><span class="sxs-lookup"><span data-stu-id="31799-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="31799-122">Функции защищенного сокета в настоящее время поддерживают только протокол IPsec и доступны в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="31799-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="31799-123">Ниже приведены структуры и перечисления, используемые функциями безопасного сокета.</span><span class="sxs-lookup"><span data-stu-id="31799-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="31799-124">**\_ \_ имя целевого объекта на уровне сокета \_**</span><span class="sxs-lookup"><span data-stu-id="31799-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="31799-125">**\_протокол безопасности сокета \_**</span><span class="sxs-lookup"><span data-stu-id="31799-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="31799-126">**\_ \_ сведения о запросе безопасности сокета \_**</span><span class="sxs-lookup"><span data-stu-id="31799-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="31799-127">**\_ \_ шаблон запроса безопасности сокета \_**</span><span class="sxs-lookup"><span data-stu-id="31799-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="31799-128">**\_Параметры безопасности сокета \_**</span><span class="sxs-lookup"><span data-stu-id="31799-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="31799-129">**\_Параметры безопасности сокета \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="31799-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="31799-130">Функции безопасного сокета просты в использовании для обычных приложений и достаточно гибкие для приложений, которым требуется высокий уровень контроля над безопасностью.</span><span class="sxs-lookup"><span data-stu-id="31799-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="31799-131">Эти функции позволяют обеспечить скрытие базового механизма безопасности от приложения.</span><span class="sxs-lookup"><span data-stu-id="31799-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="31799-132">Приложение может указать общие требования к безопасности и позволить администратору управлять протоколом безопасности, который используется для поддержки требований.</span><span class="sxs-lookup"><span data-stu-id="31799-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="31799-133">Хотя эти функции можно расширить для добавления других протоколов безопасности, в настоящее время только IPsec интегрируется с функциями безопасных сокетов.</span><span class="sxs-lookup"><span data-stu-id="31799-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="31799-134">Функция [**всасетсоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) позволяет приложению включить безопасность и применить параметры безопасности до установки соединения.</span><span class="sxs-lookup"><span data-stu-id="31799-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="31799-135">Функция [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) позволяет приложению указать целевое имя, соответствующее одноранговой сущности.</span><span class="sxs-lookup"><span data-stu-id="31799-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="31799-136">Выбранный протокол безопасности будет использовать эти сведения при проверке подлинности однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="31799-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="31799-137">Эта функция решает проблемы доверенных атак "злоумышленник в середине".</span><span class="sxs-lookup"><span data-stu-id="31799-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="31799-138">Функция [**всаделетесоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) используется для удаления ранее указанного однорангового имени для сокета.</span><span class="sxs-lookup"><span data-stu-id="31799-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="31799-139">После установления соединения функция [**всакуерисоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) позволяет приложению запрашивать свойства безопасности подключения, которые могут включать одноранговый доступ или маркер доступа к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="31799-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="31799-140">После установления соединения функция [**всаимперсонатесоккетпир**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) позволяет приложению олицетворять субъект безопасности, соответствующий узлу сокета, для выполнения авторизации на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="31799-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="31799-141">[**Всаревертимперсонатион**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) позволяет приложению завершить олицетворение однорангового узла сокета.</span><span class="sxs-lookup"><span data-stu-id="31799-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="31799-142">Архитектура защищенного сокета</span><span class="sxs-lookup"><span data-stu-id="31799-142">Secure Socket Architecture</span></span>

![Базовая архитектура расширений безопасного сокета WinSock](images/ss-arch.png)

-   <span data-ttu-id="31799-144">Приложение вызывает функции безопасного сокета для установки или запроса параметров безопасности для сокета.</span><span class="sxs-lookup"><span data-stu-id="31799-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="31799-145">Функции безопасного сокета — это набор строго типизированных функций расширения, которые заключают вызовы функции [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) , используя только что определенные значения параметра *двиоконтролкоде* , доступного в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="31799-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="31799-146">Эти запросы IOCTL обрабатываются сетевым стеком.</span><span class="sxs-lookup"><span data-stu-id="31799-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="31799-147">Сетевой стек будет направлять вызов [принудительного применения уровня приложения (ALE)](../fwp/application-layer-enforcement--ale-.md) вместе с маркером конечной точки.</span><span class="sxs-lookup"><span data-stu-id="31799-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="31799-148">Для функций [**всаделетесоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)и [**всасетсоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , ALE будет настраивать параметры приложения в локальной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="31799-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="31799-149">Для функции [**ВСАКУЕРИСОККЕТСЕКУРИТИ**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) Ale будет считывать запрошенные сведения из соответствующих локальных и удаленных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="31799-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="31799-150">На основе событий сокета принудительное применение прикладного уровня (ALE) обеспечивает применение политик для безопасной архитектуры сокетов с помощью платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="31799-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="31799-151">Дополнительные сведения см. в разделе [сведения о платформе фильтрации Windows](../fwp/about-windows-filtering-platform.md) и [применении уровня приложения (ALE)](../fwp/application-layer-enforcement--ale-.md).</span><span class="sxs-lookup"><span data-stu-id="31799-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31799-152">См. также</span><span class="sxs-lookup"><span data-stu-id="31799-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31799-153">О платформе фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="31799-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="31799-154">Расширенные примеры Winsock с использованием расширений SSL</span><span class="sxs-lookup"><span data-stu-id="31799-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="31799-155">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="31799-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="31799-156">Конфигурация IPsec</span><span class="sxs-lookup"><span data-stu-id="31799-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="31799-157">Функции IPsec</span><span class="sxs-lookup"><span data-stu-id="31799-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="31799-158">Безопасное программирование Winsock</span><span class="sxs-lookup"><span data-stu-id="31799-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="31799-159">интерфейс поставщика поддержки безопасности (SSPI)</span><span class="sxs-lookup"><span data-stu-id="31799-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="31799-160">Использование расширений SSL</span><span class="sxs-lookup"><span data-stu-id="31799-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="31799-161">Платформа фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="31799-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="31799-162">Функции API платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="31799-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 
