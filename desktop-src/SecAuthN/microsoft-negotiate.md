---
description: Microsoft Negotiate — это поставщик поддержки безопасности, который выступает в качестве уровня приложения между интерфейсом поставщика поддержки безопасности и другими SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991060"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="a74ac-103">Microsoft Negotiate</span><span class="sxs-lookup"><span data-stu-id="a74ac-103">Microsoft Negotiate</span></span>

<span data-ttu-id="a74ac-104">Microsoft Negotiate — это [*поставщик службы поддержки безопасности*](../secgloss/s-gly.md) (SSP), который выступает в качестве уровня приложения между [*интерфейсом*](../secgloss/s-gly.md) [SSPI](sspi.md)и другими SSP.</span><span class="sxs-lookup"><span data-stu-id="a74ac-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="a74ac-105">Когда приложение обращается к интерфейсу SSPI для выполнения входа в сеть, оно может указать SSP для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="a74ac-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="a74ac-106">Если в приложении указано Negotiate, то Negotiate анализирует запрос и выбирает лучший поставщик общих служб для выполнения запроса на основе политики безопасности, настроенной пользователем.</span><span class="sxs-lookup"><span data-stu-id="a74ac-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="a74ac-107">Сейчас пакет безопасности Negotiate выбирает между [Kerberos](microsoft-kerberos.md) и [NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="a74ac-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="a74ac-108">Согласование выбирает Kerberos, если не может использоваться одной из систем, участвующих в проверке подлинности, или вызывающее приложение не предоставляет достаточных сведений для использования Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a74ac-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="a74ac-109">Чтобы разрешить согласование выбора поставщика безопасности [Kerberos](microsoft-kerberos.md) , клиентское приложение должно предоставить [*имя субъекта-службы*](../secgloss/s-gly.md) (SPN), имя участника-пользователя (UPN) или имя учетной записи NetBIOS в качестве целевого имени.</span><span class="sxs-lookup"><span data-stu-id="a74ac-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="a74ac-110">В противном случае Negotiate всегда выбирает поставщика безопасности [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="a74ac-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="a74ac-111">Сервер, использующий пакет Negotiate, может отвечать на клиентские приложения, которые специально выбирают либо поставщик безопасности [Kerberos](microsoft-kerberos.md) , либо [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="a74ac-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="a74ac-112">Однако клиентское приложение должно быть уверенным в том, что сервер поддерживает пакет Negotiate для запроса проверки подлинности с помощью Negotiate.</span><span class="sxs-lookup"><span data-stu-id="a74ac-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="a74ac-113">Сервер, не поддерживающий Negotiate, не всегда может отвечать на запросы клиентов, которые задают Negotiate в качестве поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="a74ac-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="a74ac-114">Причины использования пакета Negotiate</span><span class="sxs-lookup"><span data-stu-id="a74ac-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="a74ac-115">Позволяет системе использовать самый надежный (самый безопасный) доступный протокол.</span><span class="sxs-lookup"><span data-stu-id="a74ac-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="a74ac-116">Обеспечивает прямую совместимость приложения.</span><span class="sxs-lookup"><span data-stu-id="a74ac-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="a74ac-117">Обеспечивает работу приложения в соответствии с политикой безопасности, заданной клиентом.</span><span class="sxs-lookup"><span data-stu-id="a74ac-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
