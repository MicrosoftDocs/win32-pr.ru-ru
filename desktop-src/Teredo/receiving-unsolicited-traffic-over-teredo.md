---
title: Получение незапрошенного трафика через Teredo
description: Teredo обеспечивает глобальную связь с помощью возможностей обхода IPv6 и NAT.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792931"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="fc53d-103">Получение незапрошенного трафика через Teredo</span><span class="sxs-lookup"><span data-stu-id="fc53d-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="fc53d-104">[Teredo](about-teredo.md) обеспечивает глобальную связь с помощью возможностей обхода IPv6 и NAT.</span><span class="sxs-lookup"><span data-stu-id="fc53d-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="fc53d-105">Однако многие приложения, в том числе одноранговые, должны потребовать, чтобы Teredo получал незапрошенный трафик из Интернета.</span><span class="sxs-lookup"><span data-stu-id="fc53d-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="fc53d-106">Приложение можно программировать для получения трафика через один интерфейс IPv6 или все интерфейсы, поддерживающие IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc53d-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="fc53d-107">В этой документации описаны требования для приложений, использующих интерфейс Teredo для получения незапрошенного трафика IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc53d-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="fc53d-108">Приложение будет принимать незапрошенный трафик через интерфейс Teredo только в том случае, если приложение зарегистрировано в [брандмауэре Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span><span class="sxs-lookup"><span data-stu-id="fc53d-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="fc53d-109">Для получения незапрошенного трафика необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="fc53d-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="fc53d-110">Пользователям необходимо дать указание использовать консоль управления (MMC), чтобы включить параметр "обход узлов" для приложения.</span><span class="sxs-lookup"><span data-stu-id="fc53d-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="fc53d-111">Этот параметр доступен в разделе Брандмауэр Windows Snap-In--> <application name> --> вкладке "Дополнительно". Параметр "обход ребра" должен быть включен отдельно для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="fc53d-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="fc53d-112">Параметр "обход ребра" включен приложением.</span><span class="sxs-lookup"><span data-stu-id="fc53d-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="fc53d-113">Приложения могут получать незапрошенный трафик в брандмауэре Windows для "обхода узлов" и получать незапрошенный трафик через интерфейс Teredo.</span><span class="sxs-lookup"><span data-stu-id="fc53d-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="fc53d-114">Для этого приложение должно вызвать API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) с параметром "обход ребра", установленным в значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="fc53d-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="fc53d-115">Для этого вызова API требуется согласие пользователя, прежде чем приложению будет разрешено прослушивать трафик.</span><span class="sxs-lookup"><span data-stu-id="fc53d-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="fc53d-116">Приложение устанавливает параметр сокета [ \_ \_ уровня защиты Winsock IPv6](/windows/desktop/WinSock/ipv6-protection-level) на **уровень защиты \_ без \_ ограничений** через [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="fc53d-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="fc53d-117">Это позволит приложению получить трафик обхода по периметру.</span><span class="sxs-lookup"><span data-stu-id="fc53d-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc53d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fc53d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc53d-119">Получение запрошенного трафика через Teredo</span><span class="sxs-lookup"><span data-stu-id="fc53d-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 