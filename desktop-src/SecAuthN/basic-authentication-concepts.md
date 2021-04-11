---
description: В модели клиентских и серверных приложений клиенты — это программы, действующие от имени пользователей, которым требуется что-то делать.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Основные понятия проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155275"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="0482f-103">Основные понятия проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="0482f-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="0482f-104">В модели клиентских и серверных приложений клиенты — это программы, действующие от имени пользователей, которым требуется что-то делать.</span><span class="sxs-lookup"><span data-stu-id="0482f-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="0482f-105">Это может быть открытие и использование файла, доступ к почтовому ящику, запрос к базе данных или печать документа.</span><span class="sxs-lookup"><span data-stu-id="0482f-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="0482f-106">Серверы представляют собой программы, предоставляющие службы клиентам, таким как хранение файлов, обработка почты, обработка запросов и буферизация печати.</span><span class="sxs-lookup"><span data-stu-id="0482f-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="0482f-107">Клиенты инициируют действие, серверы отвечают.</span><span class="sxs-lookup"><span data-stu-id="0482f-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="0482f-108">Как правило, сервер прослушивает порт связи, ожидающий подключения клиентов, и запрашивает службу.</span><span class="sxs-lookup"><span data-stu-id="0482f-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="0482f-109">В модели протокола Kerberos каждое соединение клиент-сервер начинается с проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0482f-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="0482f-110">Клиент и сервер, по очереди, выполняют последовательность действий, созданных для проверки каждым участником соединения того, что участник на другом конце подлинный.</span><span class="sxs-lookup"><span data-stu-id="0482f-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="0482f-111">Если проверка подлинности завершена успешно, сеанс установки соединения завершается и устанавливается безопасный сеанс клиент-сервер.</span><span class="sxs-lookup"><span data-stu-id="0482f-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="0482f-112">Протокол Kerberos использует следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="0482f-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="0482f-113">Проверка подлинности ключа</span><span class="sxs-lookup"><span data-stu-id="0482f-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="0482f-114">Сообщения средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="0482f-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="0482f-115">Распределение ключей</span><span class="sxs-lookup"><span data-stu-id="0482f-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="0482f-116">Билеты сеансов</span><span class="sxs-lookup"><span data-stu-id="0482f-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="0482f-117">Билеты предоставления билетов</span><span class="sxs-lookup"><span data-stu-id="0482f-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



