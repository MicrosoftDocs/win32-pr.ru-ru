---
title: Использование учетной записи локального пользователя в качестве учетной записи входа службы
description: Локальная учетная запись пользователя (формат имени \ 0034;. \\ Имя пользователя \ 0034;) Существует только в базе данных SAM главного компьютера; в службе домен Active Directory Services отсутствует объект User.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132826"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="f8aab-103">Использование учетной записи локального пользователя в качестве учетной записи входа службы</span><span class="sxs-lookup"><span data-stu-id="f8aab-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="f8aab-104">Локальная учетная запись пользователя (формат имени: ". \\ *Username*") существует только в базе данных SAM главного компьютера; в службе домен Active Directory Services отсутствует объект User.</span><span class="sxs-lookup"><span data-stu-id="f8aab-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="f8aab-105">Это означает, что домен не может пройти проверку подлинности локальной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f8aab-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="f8aab-106">Следовательно, служба, которая работает в контексте безопасности локальной учетной записи пользователя, не имеет доступа к сетевым ресурсам (за исключением анонимного пользователя) и не может поддерживать взаимную проверку подлинности Kerberos, в которой служба проходит проверку подлинности по своим клиентам.</span><span class="sxs-lookup"><span data-stu-id="f8aab-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="f8aab-107">По этим причинам локальные учетные записи пользователей обычно не подходят для служб, поддерживающих каталог.</span><span class="sxs-lookup"><span data-stu-id="f8aab-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="f8aab-108">На стороне плюс ошибки в службе не могут повредить систему.</span><span class="sxs-lookup"><span data-stu-id="f8aab-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="f8aab-109">Если служба может работать с этими ограничениями, она должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="f8aab-109">If your service can run under those limitations, it should.</span></span>

 

 




