---
description: Как клиенты, так и серверы должны получить учетные данные, прежде чем они смогут установить контекст безопасности для обмена сообщениями.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Получение учетных данных дайджеста по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786592"
---
# <a name="obtaining-default-digest-credentials"></a>Получение учетных данных дайджеста по умолчанию

Как клиенты, так и серверы должны получить [*учетные данные*](../secgloss/c-gly.md) , прежде чем они смогут установить [*контекст безопасности*](../secgloss/s-gly.md) для обмена сообщениями. Поведение функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) по умолчанию заключается в предоставлении учетных данных для субъекта безопасности, связанного с текущим [*сеансом*](../secgloss/s-gly.md)входа.

В следующем примере демонстрируется вызов на стороне сервера для получения учетных данных по умолчанию.


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



Вызов на стороне клиента для учетных данных по умолчанию идентичен, за исключением того, что третий параметр должен указывать SECPKG \_ cred \_ OUTBOUND, чтобы указать, что клиент будет использовать маркер учетных данных, возвращаемый функцией.

Пример, демонстрирующий получение учетных данных для субъекта безопасности, отличного от пользователя, выполнившего вход, см. в разделе [получение альтернативных учетных данных](obtaining-alternate-digest-credentials.md).

 

 
