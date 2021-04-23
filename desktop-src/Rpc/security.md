---
title: Безопасность (RPC)
description: Благодаря увеличению использования распределенных приложений потребность в безопасной связи между клиентскими и серверными частями приложений имеет первостепенное значение.
ms.assetid: 0eceefed-644c-4e4b-a873-8005137c00ef
keywords:
- Удаленный вызов процедур RPC, описание, безопасность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a257b67fad90fe568615eb5731fc60dc9706d5ae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134910"
---
# <a name="security-rpc"></a><span data-ttu-id="8150d-104">Безопасность (RPC)</span><span class="sxs-lookup"><span data-stu-id="8150d-104">Security (RPC)</span></span>

<span data-ttu-id="8150d-105">Благодаря увеличению использования распределенных приложений потребность в безопасной связи между клиентскими и серверными частями приложений имеет первостепенное значение.</span><span class="sxs-lookup"><span data-stu-id="8150d-105">With the increased use of distributed applications, the need for secure communications between the client and server portions of applications is paramount.</span></span> <span data-ttu-id="8150d-106">Библиотека времени выполнения удаленного вызова процедур (RPC) предоставляет стандартизированный интерфейс для служб проверки подлинности как для клиентов, так и для серверов.</span><span class="sxs-lookup"><span data-stu-id="8150d-106">The Remote Procedure Call (RPC) run-time library provides a standardized interface to authentication services for both clients and servers.</span></span> <span data-ttu-id="8150d-107">Службы проверки подлинности в системе узла сервера обеспечивают проверку подлинности RPC.</span><span class="sxs-lookup"><span data-stu-id="8150d-107">The authentication services on the server host system provide RPC authentication.</span></span> <span data-ttu-id="8150d-108">Приложения используют удаленные вызовы процедур, прошедшие проверку подлинности, чтобы гарантировать, что все вызовы поступают от авторизованных клиентов.</span><span class="sxs-lookup"><span data-stu-id="8150d-108">Applications use authenticated remote procedure calls to ensure that all calls come from authorized clients.</span></span> <span data-ttu-id="8150d-109">Они также могут гарантировать, что все ответы сервера поступают с серверов, прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8150d-109">They can also help ensure that all server replies come from authenticated servers.</span></span>

<span data-ttu-id="8150d-110">В этом разделе представлен обзор проверки подлинности RPC в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="8150d-110">This section presents an overview of authenticated RPC in the following sections:</span></span>

-   [<span data-ttu-id="8150d-111">Основы безопасности RPC</span><span class="sxs-lookup"><span data-stu-id="8150d-111">RPC Security Essentials</span></span>](rpc-security-essentials.md)
-   [<span data-ttu-id="8150d-112">Методы безопасности</span><span class="sxs-lookup"><span data-stu-id="8150d-112">Security Methods</span></span>](security-methods.md)

 

 




