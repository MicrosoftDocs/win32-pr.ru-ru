---
description: Проверьте права доступа, которые предоставляет дескриптор безопасности для клиента.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Проверка клиентского доступа с помощью списков ACL в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda629338d731d6e93f316fc15a6338c99bc1609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910875"
---
# <a name="verifying-client-access-with-acls-in-c"></a><span data-ttu-id="9b986-103">Проверка клиентского доступа с помощью списков ACL в C++</span><span class="sxs-lookup"><span data-stu-id="9b986-103">Verifying Client Access with ACLs in C++</span></span>

<span data-ttu-id="9b986-104">В следующем примере показано, как сервер может проверить права доступа, разрешенные [*дескриптором безопасности*](/windows/desktop/SecGloss/s-gly) для клиента.</span><span class="sxs-lookup"><span data-stu-id="9b986-104">The following example shows how a server could check the access rights that a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows for a client.</span></span> <span data-ttu-id="9b986-105">В примере используется функция [**имперсонатенамедпипеклиент**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) . Однако он будет работать так же, как и любые другие функции олицетворения.</span><span class="sxs-lookup"><span data-stu-id="9b986-105">The example uses the [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) function; however, it would work the same using any of the other impersonation functions.</span></span> <span data-ttu-id="9b986-106">После олицетворения клиента в примере вызывается функция [**опенсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) для получения [*маркера олицетворения*](/windows/desktop/SecGloss/i-gly).</span><span class="sxs-lookup"><span data-stu-id="9b986-106">After impersonating the client, the example calls the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function to get the [*impersonation token*](/windows/desktop/SecGloss/i-gly).</span></span> <span data-ttu-id="9b986-107">Затем он вызывает функцию [**мапженерикмаск**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) для преобразования любых универсальных прав доступа к соответствующим определенным и стандартным правам в соответствии с сопоставлением, указанным в структуре [**универсального \_ сопоставления**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .</span><span class="sxs-lookup"><span data-stu-id="9b986-107">Then, it calls the [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) function to convert any generic access rights to the corresponding specific and standard rights according to the mapping specified in the [**GENERIC\_MAPPING**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) structure.</span></span>

<span data-ttu-id="9b986-108">Функция [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) проверяет запрошенные права доступа на соответствие правам, разрешенному клиенту, в списке DACL дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9b986-108">The [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function checks the requested access rights against the rights allowed for the client in the DACL of the security descriptor.</span></span> <span data-ttu-id="9b986-109">Чтобы проверить доступ и создать запись в журнале событий безопасности, используйте функцию [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) .</span><span class="sxs-lookup"><span data-stu-id="9b986-109">To check access and generate an entry in the security event log, use the [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) function.</span></span>


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



 

 
