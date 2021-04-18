---
description: После установки билета предоставления билета (TGT) и ключа сеанса для клиента Клиент может запросить отдельный ключ сеанса и билет для службы.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Предоставление билета службой Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662732"
---
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="94dd8-103">Предоставление билета службой Exchange</span><span class="sxs-lookup"><span data-stu-id="94dd8-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="94dd8-104">После установки билета предоставления билета (TGT) и [*ключа сеанса*](../secgloss/s-gly.md) для клиента Клиент может запросить отдельный ключ сеанса и билет для службы.</span><span class="sxs-lookup"><span data-stu-id="94dd8-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="94dd8-105">**Запрос билета для другой службы**</span><span class="sxs-lookup"><span data-stu-id="94dd8-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="94dd8-106">Клиент Kerberos на рабочей станции пользователя запрашивает [*учетные данные*](../secgloss/c-gly.md) для службы, отправляя на [*центр распространения ключей*](../secgloss/k-gly.md) (KDC) сообщение типа КРБ \_ TGS \_ REQ (запрос на обслуживание Kerberos Ticket-Granting).</span><span class="sxs-lookup"><span data-stu-id="94dd8-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="94dd8-107">Это сообщение состоит из удостоверения службы, для которой клиент запрашивает учетные данные, сообщение средства проверки подлинности, зашифрованное с помощью нового [*ключа сеанса*](../secgloss/s-gly.md)входа пользователя, и TGT, полученный при [обмене данными службы проверки подлинности](authentication-service-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="94dd8-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="94dd8-108">Когда KDC получает КРБ \_ TGS \_ , KDC расшифровывает билет TGT с секретным ключом и извлекает ключ сеанса входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="94dd8-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="94dd8-109">KDC использует [*ключ сеанса*](../secgloss/s-gly.md) входа, чтобы расшифровать сообщение средства проверки подлинности пользователя и оценить его.</span><span class="sxs-lookup"><span data-stu-id="94dd8-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="94dd8-110">Если средство проверки подлинности проходит тест, KDC извлекает данные авторизации пользователя из TGT и передает ключ сеанса, чтобы предоставить пользователю общий доступ к запрашиваемому серверу.</span><span class="sxs-lookup"><span data-stu-id="94dd8-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="94dd8-111">KDC шифрует одну копию ключа сеанса службы с помощью ключа сеанса входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="94dd8-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="94dd8-112">KDC внедряет еще одну копию ключа сеанса службы в билет, а также данные авторизации пользователя и шифрует билет с помощью [*главного ключа*](../secgloss/m-gly.md)сервера.</span><span class="sxs-lookup"><span data-stu-id="94dd8-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="94dd8-113">KDC отправляет эти учетные данные обратно клиенту, отвечая на сообщение типа КРБ \_ TGS \_ (ответ службы Kerberos Ticket-Granting).</span><span class="sxs-lookup"><span data-stu-id="94dd8-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="94dd8-114">Когда клиент получает ответ, он расшифровывает ключ сеанса службы с помощью ключа сеанса входа пользователя и сохраняет ключ сеанса службы в кэше билетов.</span><span class="sxs-lookup"><span data-stu-id="94dd8-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="94dd8-115">Клиент извлекает билет на сервер и сохраняет его в кэше билетов.</span><span class="sxs-lookup"><span data-stu-id="94dd8-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 
