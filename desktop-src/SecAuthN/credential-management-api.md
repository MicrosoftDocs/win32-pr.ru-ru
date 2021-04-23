---
description: API управления учетными данными
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API управления учетными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814744"
---
# <a name="credential-management-api"></a><span data-ttu-id="c5ebf-103">API управления учетными данными</span><span class="sxs-lookup"><span data-stu-id="c5ebf-103">Credential Management API</span></span>

<span data-ttu-id="c5ebf-104">Функции управления учетными данными составляют набор функций, которые должен реализовать Диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="c5ebf-105">А именно:</span><span class="sxs-lookup"><span data-stu-id="c5ebf-105">These are:</span></span>

-   <span data-ttu-id="c5ebf-106">[**Нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)— функция обработчика событий, которая вызывается многопротокольным маршрутизатором при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="c5ebf-107">[**Нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), функция обработчика событий, которая вызывается многопротокольной организацией при изменении пароля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="c5ebf-108">Функции управления учетными данными всегда вызываются в системном контексте (LocalSystem), а не в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="c5ebf-109">Дополнительные сведения о создании и регистрации приложения диспетчера учетных данных см. в разделе [Реализация диспетчера учетных данных](implementing-a-credential-manager.md) и [Регистрация поставщиков сетевых услуг и диспетчеров учетных данных](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="c5ebf-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 



