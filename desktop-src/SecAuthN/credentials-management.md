---
description: Разработчики, которые пишут для Windows, могут использовать API управления учетными данными, включая функции пользовательского интерфейса управления учетными данными, для получения и управления учетными данными, такими как имена пользователей и пароли.
ms.assetid: 0c44a360-d9c3-448c-a0d5-e33f3c27c58c
title: Управление учетными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5ffa7fb493fdfbf64945b202d2e2678fb329f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265015"
---
# <a name="credentials-management"></a><span data-ttu-id="e3c8f-103">Управление учетными данными</span><span class="sxs-lookup"><span data-stu-id="e3c8f-103">Credentials Management</span></span>

<span data-ttu-id="e3c8f-104">Разработчики, которые пишут для Windows, могут использовать API управления учетными данными, включая функции пользовательского интерфейса управления учетными данными, для получения и управления учетными данными, такими как имена пользователей и пароли.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-104">Developers who write for Windows can use the Credentials Management API including Credentials Management User Interface (UI) functions to obtain and manage credential information such as user names and passwords.</span></span> <span data-ttu-id="e3c8f-105">Эти функции запрашивают сведения об учетной записи Windows для использования вместо учетных данных, установленных при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-105">These functions request Windows account information to be used instead of the credentials established while logging on.</span></span> <span data-ttu-id="e3c8f-106">Такие запросы обычно возникают, когда учетные данные для входа не имеют разрешений, необходимых приложению.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-106">Such requests typically occur when the logon credentials do not have permissions that are required by the application.</span></span>

<span data-ttu-id="e3c8f-107">Функции пользовательского интерфейса управления учетными данными предоставляют интерфейсы с внешним видом пользовательского интерфейса Windows.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-107">The Credentials Management UI functions provide interfaces with the appearance of the Windows user interface.</span></span> <span data-ttu-id="e3c8f-108">Эти функции включают настраиваемые параметры, которые добавляют сведения о пользователе в хранилище учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-108">These functions include customizable options that add user's information to the user's credentials store.</span></span>

<span data-ttu-id="e3c8f-109">В следующих разделах содержатся дополнительные сведения об API управления учетными данными.</span><span class="sxs-lookup"><span data-stu-id="e3c8f-109">The following topics provide more information about the Credentials Management API:</span></span>

-   [<span data-ttu-id="e3c8f-110">Виды учетных данных</span><span class="sxs-lookup"><span data-stu-id="e3c8f-110">Kinds of Credentials</span></span>](kinds-of-credentials.md)
-   [<span data-ttu-id="e3c8f-111">Форматы имен пользователей</span><span class="sxs-lookup"><span data-stu-id="e3c8f-111">User Name Formats</span></span>](user-name-formats.md)

<span data-ttu-id="e3c8f-112">Сведения о функциях API управления учетными данными см. в разделе [Справочник по проверке подлинности](authentication-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e3c8f-112">For information about functions in the Credential Management API, see [Authentication Reference](authentication-reference.md).</span></span>

 

 



