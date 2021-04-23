---
description: Microsoft Digest выполняет начальную проверку подлинности при получении сервером первого ответа на запрос от клиента.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Дайджест-проверка подлинности Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647539"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="b5172-103">Дайджест-проверка подлинности Microsoft</span><span class="sxs-lookup"><span data-stu-id="b5172-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="b5172-104">Microsoft Digest выполняет начальную проверку подлинности при получении сервером первого ответа на запрос от клиента.</span><span class="sxs-lookup"><span data-stu-id="b5172-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="b5172-105">Сервер проверяет, что клиент не прошел проверку подлинности, а затем выполняет начальную проверку подлинности, обращаясь к службам контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="b5172-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="b5172-106">Подробное описание этой процедуры см. в разделе [Начальная проверка подлинности с помощью Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="b5172-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="b5172-107">Когда начальная проверка подлинности прошла успешно, сервер получает [*ключ сеанса*](../secgloss/s-gly.md)дайджеста.</span><span class="sxs-lookup"><span data-stu-id="b5172-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b5172-108">Сервер кэширует этот ключ и использует его для проверки подлинности последующих запросов ресурсов от клиента.</span><span class="sxs-lookup"><span data-stu-id="b5172-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="b5172-109">Это локальная проверка подлинности, т. е. не требуется доступ к контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="b5172-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="b5172-110">Подробное описание этой процедуры см. в [статье Проверка подлинности последующих запросов с помощью Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="b5172-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="b5172-111">При использовании протокола HTTP соединение между клиентом и сервером не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5172-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="b5172-112">Чтобы уменьшить трафик контроллера домена и повысить производительность, Microsoft Digest кэширует сведения, полученные после успешной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b5172-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="b5172-113">Сведения об этом процессе см. [в разделе поддержание контекста безопасности между соединениями](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="b5172-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
