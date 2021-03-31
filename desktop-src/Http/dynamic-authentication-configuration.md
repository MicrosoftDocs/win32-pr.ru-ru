---
title: Настройка динамической проверки подлинности
description: Приложения могут изменять конфигурации проверки подлинности в группе URL-адресов или сеансах сервера в любое время.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328896"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="58917-103">Настройка динамической проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="58917-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="58917-104">По умолчанию API сервера HTTP не выполняет проверку подлинности, если только приложение не включает его.</span><span class="sxs-lookup"><span data-stu-id="58917-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="58917-105">Приложения могут изменять конфигурации проверки подлинности в группе URL-адресов или сеансах сервера в любое время.</span><span class="sxs-lookup"><span data-stu-id="58917-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="58917-106">Изменения конфигурации проверки подлинности не влияют на запросы, которые уже прошли проверку подлинности или отправлены в приложение.</span><span class="sxs-lookup"><span data-stu-id="58917-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="58917-107">Для схем проверки подлинности, где требуется несколько циклов подтверждения подлинности, API-интерфейс сервера HTTP удаляет подтверждение, если текущая схема больше не поддерживается из-за изменений конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="58917-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="58917-108">Например, если приложение включает Negotiate и отключает NTLM, а API-интерфейс HTTP-сервера находится в промежуточной проверке подлинности для NTLM, подтверждение для NTLM отбрасывается и запрос передается в приложение.</span><span class="sxs-lookup"><span data-stu-id="58917-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="58917-109">Приложение отправляет запрос на проверку подлинности 401 с новыми типами проверки подлинности, указанными в заголовке WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="58917-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




