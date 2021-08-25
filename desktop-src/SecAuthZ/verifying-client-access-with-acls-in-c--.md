---
description: Проверьте права доступа, которые предоставляет дескриптор безопасности для клиента.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Проверка клиентского доступа с помощью списков ACL в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2160b48a3b88a617eaaea1e8fae63168db5a85e82cad62be5aef248ff51581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906694"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Проверка клиентского доступа с помощью списков ACL в C++

В следующем примере показано, как сервер может проверить права доступа, разрешенные [*дескриптором безопасности*](/windows/desktop/SecGloss/s-gly) для клиента. В примере используется функция [**имперсонатенамедпипеклиент**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) . Однако он будет работать так же, как и любые другие функции олицетворения. После олицетворения клиента в примере вызывается функция [**опенсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) для получения [*маркера олицетворения*](/windows/desktop/SecGloss/i-gly). Затем он вызывает функцию [**мапженерикмаск**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) для преобразования любых универсальных прав доступа к соответствующим определенным и стандартным правам в соответствии с сопоставлением, указанным в структуре [**универсального \_ сопоставления**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

Функция [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) проверяет запрошенные права доступа на соответствие правам, разрешенному клиенту, в списке DACL дескриптора безопасности. Чтобы проверить доступ и создать запись в журнале событий безопасности, используйте функцию [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) .


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
