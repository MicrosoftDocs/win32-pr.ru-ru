---
title: О EAP
description: Протокол расширенной проверки подлинности (EAP), Стандартный поддерживаемый многими сетевыми компонентами Майкрософт.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Описание расширяемого протокола проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413968"
---
# <a name="about-eap"></a><span data-ttu-id="48560-104">О EAP</span><span class="sxs-lookup"><span data-stu-id="48560-104">About EAP</span></span>

<span data-ttu-id="48560-105">В этом разделе описывается протокол расширенной проверки подлинности (EAP), Стандартный поддерживаемый многими сетевыми компонентами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="48560-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="48560-106">Компоненты EAP</span><span class="sxs-lookup"><span data-stu-id="48560-106">EAP Components</span></span>

<span data-ttu-id="48560-107">EAP очень важен для защиты беспроводных сетей (802.1 X), проводных локальных сетей, коммутируемых сетей и виртуальных частных подключений (VPN).</span><span class="sxs-lookup"><span data-stu-id="48560-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="48560-108">Следующие компоненты поддерживают протокол EAP.</span><span class="sxs-lookup"><span data-stu-id="48560-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="48560-109">Клиенты и серверы удаленного доступа Microsoft для коммутируемого подключения и VPN (PPTP и L2TP/IPSec) реализуют EAP как расширение для PPP.</span><span class="sxs-lookup"><span data-stu-id="48560-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="48560-110">Дополнительные сведения см. в [документе RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="48560-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="48560-111">Клиенты беспроводной локальной сети и проводной ЛС, совместимые с Microsoft IEEE 802.1 X, реализуют EAP, как определено в стандарте IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="48560-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="48560-112">Сервер Microsoft RADIUS, называемый службой проверки подлинности в Интернете (IAS), реализует EAP, как определено в [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span><span class="sxs-lookup"><span data-stu-id="48560-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="48560-113">Все перечисленные выше компоненты поддерживают эту расширяемую архитектуру с помощью пакета средств разработки программного обеспечения Microsoft Windows (SDK), что позволяет интегрировать сторонние модули проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="48560-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="48560-114">Этот расширяемый механизм можно использовать для поддержки протоколов Token Card, Kerberos, открытого ключа и протокола проверки подлинности S/Key.</span><span class="sxs-lookup"><span data-stu-id="48560-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="48560-115">Защищенный протокол расширенной проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="48560-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="48560-116">Помимо протокола EAP, реализация беспроводного (802.1 X) и RADIUS-сервера также поддерживает новые стандартные протоколы, называемые Protected EAP (PEAP).</span><span class="sxs-lookup"><span data-stu-id="48560-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="48560-117">PEAP предоставляет несколько ключевых служб для других протоколов проверки подлинности EAP, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="48560-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="48560-118">Протокол PEAP шифрует пакеты EAP других протоколов проверки подлинности EAP с помощью протокола TLS, технологии на основе протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="48560-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="48560-119">Дополнительные сведения см. в [документе RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="48560-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="48560-120">PEAP выполняет проверку подлинности на стороне сервера с использованием сертификата сервера с сервером RADIUS.</span><span class="sxs-lookup"><span data-stu-id="48560-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="48560-121">Протокол PEAP обеспечивает возможность быстрой повторной проверки подлинности, которая поддерживает эффективное перемещение между беспроводными устройствами.</span><span class="sxs-lookup"><span data-stu-id="48560-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="48560-122">PEAP управляет фрагментацией и повторной сборкой пакетов EAP.</span><span class="sxs-lookup"><span data-stu-id="48560-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="48560-123">Протокол PEAP создает ключи, используемые для шифрования беспроводного трафика.</span><span class="sxs-lookup"><span data-stu-id="48560-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="48560-124">Протокол PEAP значительно упрощает написание протокола EAP, поскольку программист больше не должен решать эти проблемы.</span><span class="sxs-lookup"><span data-stu-id="48560-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48560-125">См. также</span><span class="sxs-lookup"><span data-stu-id="48560-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48560-126">О протоколах EAP и EAPHost</span><span class="sxs-lookup"><span data-stu-id="48560-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




