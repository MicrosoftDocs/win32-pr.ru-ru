---
description: Schannel поддерживает версии 1,0, 1,1 и 1,2 протокола TLS.
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Протокол TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664031"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="a4ec8-103">Протокол TLS</span><span class="sxs-lookup"><span data-stu-id="a4ec8-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="a4ec8-104">Schannel поддерживает версии 1,0, 1,1 и 1,2 [*протокола TLS*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a4ec8-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="a4ec8-105">Этот протокол является отраслевым стандартом, предназначенным для защиты конфиденциальности данных, передаваемых через Интернет.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="a4ec8-106">TLS предполагает, что используется транспорт, ориентированный на соединение, обычно TCP.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="a4ec8-107">Протокол TLS позволяет клиентским и серверным приложениям обнаруживать следующие угрозы безопасности:</span><span class="sxs-lookup"><span data-stu-id="a4ec8-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="a4ec8-108">Вмешательство в сообщение</span><span class="sxs-lookup"><span data-stu-id="a4ec8-108">Message tampering</span></span>
-   <span data-ttu-id="a4ec8-109">Перехват сообщений</span><span class="sxs-lookup"><span data-stu-id="a4ec8-109">Message interception</span></span>
-   <span data-ttu-id="a4ec8-110">Подделка сообщений</span><span class="sxs-lookup"><span data-stu-id="a4ec8-110">Message forgery</span></span>

<span data-ttu-id="a4ec8-111">Полная спецификация протокола TLS доступна на веб-сайте IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="a4ec8-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="a4ec8-112">Организация TLS</span><span class="sxs-lookup"><span data-stu-id="a4ec8-112">Organization of TLS</span></span>

<span data-ttu-id="a4ec8-113">Следующие шаги используются при использовании TLS для обмена данными между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="a4ec8-114">**Использование TLS для обмена данными между клиентом и сервером**</span><span class="sxs-lookup"><span data-stu-id="a4ec8-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="a4ec8-115">Согласование с набором подтверждения и набора шифров</span><span class="sxs-lookup"><span data-stu-id="a4ec8-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="a4ec8-116">Проверка подлинности сторон</span><span class="sxs-lookup"><span data-stu-id="a4ec8-116">Authentication of parties</span></span>
3.  <span data-ttu-id="a4ec8-117">Обмен информацией, относящейся к ключам</span><span class="sxs-lookup"><span data-stu-id="a4ec8-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="a4ec8-118">Обмен данными приложений</span><span class="sxs-lookup"><span data-stu-id="a4ec8-118">Application data exchange</span></span>

<span data-ttu-id="a4ec8-119">Действия, которые составляют протокол TLS, делятся на два протокола, которые вместе обеспечивают безопасность подключения:</span><span class="sxs-lookup"><span data-stu-id="a4ec8-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="a4ec8-120">[Протокол подтверждения TLS](tls-handshake-protocol.md)— (шаги 1 – 3)</span><span class="sxs-lookup"><span data-stu-id="a4ec8-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="a4ec8-121">[Протокол TLS](tls-record-protocol.md)— (шаг 4)</span><span class="sxs-lookup"><span data-stu-id="a4ec8-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="a4ec8-122">SSPI с реализациями TLS</span><span class="sxs-lookup"><span data-stu-id="a4ec8-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="a4ec8-123">Поскольку TLS не имеет спецификации GSSAPI, средства реализации TLS не могут быть знакомы с функциями SSPI.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="a4ec8-124">Приложения вызывают функции SSPI для перечисления доступных пакетов, создания и работы с дескрипторами учетных данных, создания контекстов безопасности и обеспечения конфиденциальности целостности сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="a4ec8-125">Для поддержки функций SSPI, используемых приложениями пользовательского режима, функции, перечисленные в [функциях, реализованных с помощью SSP или ТД пользовательского режима](/windows/desktop/SecAuthN/authentication-functions) , должны поддерживаться реализациями TLS, такими как schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="a4ec8-126">Дополнительные сведения о функциях SSPI и службах SSP см. в разделе [функции проверки подлинности](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a4ec8-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4ec8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a4ec8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4ec8-128">Комплекты шифров TLS</span><span class="sxs-lookup"><span data-stu-id="a4ec8-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="a4ec8-129">TLS и SSL</span><span class="sxs-lookup"><span data-stu-id="a4ec8-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
