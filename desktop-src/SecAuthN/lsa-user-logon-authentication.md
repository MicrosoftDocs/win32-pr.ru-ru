---
description: Проверка подлинности входа пользователя LSA
ms.assetid: 62606687-05f1-4757-9fcd-c1932412dcc4
title: Проверка подлинности входа пользователя LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57371a1c9f4c3269822fa98475bc0b426b854a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265804"
---
# <a name="lsa-user-logon-authentication"></a><span data-ttu-id="b1ff9-103">Проверка подлинности входа пользователя LSA</span><span class="sxs-lookup"><span data-stu-id="b1ff9-103">LSA User Logon Authentication</span></span>

<span data-ttu-id="b1ff9-104">LSA обрабатывает вход пользователя и проверку подлинности на локальном компьютере, и если пакет проверки подлинности, обрабатывающий запрос на вход в систему, поддерживает сквозную аутентификацию, LSA также может регистрировать пользователей на других компьютерах в сети.</span><span class="sxs-lookup"><span data-stu-id="b1ff9-104">The LSA handles user logon and authentication on the local computer, and if the authentication package processing the logon request supports pass-through authentication, the LSA can also log users on to other computers on the network.</span></span> <span data-ttu-id="b1ff9-105">LSA предоставляет доступ к пакетам проверки подлинности для поставщиков поддержки безопасности (SSP).</span><span class="sxs-lookup"><span data-stu-id="b1ff9-105">The LSA provides access to authentication packages for Security Support Providers (SSPs).</span></span> <span data-ttu-id="b1ff9-106">Выполняется один из двух следующих типов проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="b1ff9-106">One of the two following types of authentication is performed:</span></span>

-   [<span data-ttu-id="b1ff9-107">Интерактивная аутентификация</span><span class="sxs-lookup"><span data-stu-id="b1ff9-107">Interactive Authentication</span></span>](interactive-authentication.md)
-   [<span data-ttu-id="b1ff9-108">Неинтерактивная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="b1ff9-108">Noninteractive Authentication</span></span>](noninteractive-authentication.md)

 

 



