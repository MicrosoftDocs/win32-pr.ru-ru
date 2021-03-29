---
description: В следующем примере показано, как обычный клиент получает учетные данные SChannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Получение учетных данных SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345915"
---
# <a name="getting-schannel-credentials"></a>Получение учетных данных SChannel

В следующем примере показано, как обычный клиент получает учетные данные SChannel. В примере следует использовать системные значения по умолчанию для шифров и сильных шифров. Это позволяет пакету SChannel использовать наиболее надежные алгоритмы для защиты канала.


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



Основное различие между запросом на стороне клиента и сервером в отношении учетных данных заключается в том, что сервер должен предоставить сертификат с помощью структуры [**\_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) следующим образом:


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



Пример функции *жетсерверцертификате* — это функция-заполнитель для этого действия конкретного приложения. Пример реализации функции *жетсерверцертификате* см. [в разделе Получение сертификата](getting-a-certificate-for-schannel.md).

> [!Note]  
> При запросе учетных данных, которые будут использоваться сервером, измените третий параметр (*фкредентиалусе*) функции [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) с SECPKG \_ cred \_ OUTBOUND на SECPKG \_ cred \_ Inbound.

 

 

 
