---
description: В Microsoft Digest требуются учетные данные пользователя. как клиент, так и сервер должны представлять действительные учетные данные, прежде чем они смогут установить контекст безопасности для обмена сообщениями. Для получения и представления учетных данных используются дескрипторы учетных данных.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Получение учетных данных дайджест-поставщика Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497286"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="2c26a-104">Получение учетных данных дайджест-поставщика Microsoft</span><span class="sxs-lookup"><span data-stu-id="2c26a-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="2c26a-105">В Microsoft Digest требуются [*учетные данные*](../secgloss/c-gly.md) пользователя. как клиент, так и сервер должны представлять действительные учетные данные, прежде чем они смогут установить [*контекст безопасности*](../secgloss/s-gly.md) для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2c26a-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="2c26a-106">Для получения и представления учетных данных используются дескрипторы учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2c26a-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="2c26a-107">Так как для хранения сведений о конфигурации используется обработчик учетных данных, один и тот же обработчик не может использоваться как для операций на стороне клиента, так и для серверной операции.</span><span class="sxs-lookup"><span data-stu-id="2c26a-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="2c26a-108">Это означает, что приложения, поддерживающие как клиентские, так и серверные соединения, должны получить как минимум два дескриптора учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2c26a-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="2c26a-109">Чтобы получить маркер учетных данных, необходимых для Microsoft Digest, вызовите функцию [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="2c26a-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="2c26a-110">В следующих примерах языка C демонстрируется получение учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2c26a-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="2c26a-111">Получение учетных данных дайджеста по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c26a-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="2c26a-112">Получение учетных данных альтернативной дайджеста</span><span class="sxs-lookup"><span data-stu-id="2c26a-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
