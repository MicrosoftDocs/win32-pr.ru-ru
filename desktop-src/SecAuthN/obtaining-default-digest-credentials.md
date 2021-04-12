---
description: Как клиенты, так и серверы должны получить учетные данные, прежде чем они смогут установить контекст безопасности для обмена сообщениями.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Получение учетных данных дайджеста по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264364"
---
# <a name="obtaining-default-digest-credentials"></a><span data-ttu-id="478df-103">Получение учетных данных дайджеста по умолчанию</span><span class="sxs-lookup"><span data-stu-id="478df-103">Obtaining Default Digest Credentials</span></span>

<span data-ttu-id="478df-104">Как клиенты, так и серверы должны получить [*учетные данные*](../secgloss/c-gly.md) , прежде чем они смогут установить [*контекст безопасности*](../secgloss/s-gly.md) для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="478df-104">Both clients and servers must obtain [*credentials*](../secgloss/c-gly.md) before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="478df-105">Поведение функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) по умолчанию заключается в предоставлении учетных данных для субъекта безопасности, связанного с текущим [*сеансом*](../secgloss/s-gly.md)входа.</span><span class="sxs-lookup"><span data-stu-id="478df-105">The default behavior of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function is to provide credentials for the security principal associated with the current logon [*session*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="478df-106">В следующем примере демонстрируется вызов на стороне сервера для получения учетных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478df-106">The following example demonstrates a server-side call to obtain the default credentials.</span></span>


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



<span data-ttu-id="478df-107">Вызов на стороне клиента для учетных данных по умолчанию идентичен, за исключением того, что третий параметр должен указывать SECPKG \_ cred \_ OUTBOUND, чтобы указать, что клиент будет использовать маркер учетных данных, возвращаемый функцией.</span><span class="sxs-lookup"><span data-stu-id="478df-107">The client-side call for default credentials is identical, except the third parameter must specify SECPKG\_CRED\_OUTBOUND to indicate that the client will use the credentials handle returned by the function.</span></span>

<span data-ttu-id="478df-108">Пример, демонстрирующий получение учетных данных для субъекта безопасности, отличного от пользователя, выполнившего вход, см. в разделе [получение альтернативных учетных данных](obtaining-alternate-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="478df-108">For an example that demonstrates obtaining credentials for a security principal other than the logged on user, see [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).</span></span>

 

 
