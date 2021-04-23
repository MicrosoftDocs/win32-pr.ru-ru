---
description: В следующем примере предпринимается попытка изменить список DACL объекта File, выполнив владение этим объектом.
ms.assetid: 0b309ac9-177d-425f-8b78-71fe73e41979
title: Получение владения объектом в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae43c28cb55193d43a15ed08f5905defded3dc2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662557"
---
# <a name="taking-object-ownership-in-c"></a><span data-ttu-id="572cc-103">Получение владения объектом в C++</span><span class="sxs-lookup"><span data-stu-id="572cc-103">Taking Object Ownership in C++</span></span>

<span data-ttu-id="572cc-104">В следующем примере предпринимается попытка изменить список DACL объекта File, выполнив владение этим объектом.</span><span class="sxs-lookup"><span data-stu-id="572cc-104">The following example tries to change the DACL of a file object by taking ownership of that object.</span></span> <span data-ttu-id="572cc-105">Это будет успешно, только если вызывающий объект записывает \_ доступ DAC к объекту или является владельцем объекта.</span><span class="sxs-lookup"><span data-stu-id="572cc-105">This will succeed only if the caller has WRITE\_DAC access to the object or is the owner of the object.</span></span> <span data-ttu-id="572cc-106">Если начальная попытка изменить список DACL не удалась, администратор может стать владельцем объекта.</span><span class="sxs-lookup"><span data-stu-id="572cc-106">If the initial attempt to change the DACL fails, an administrator can take ownership of the object.</span></span> <span data-ttu-id="572cc-107">Чтобы предоставить права администратора, в примере включается привилегия SE \_ Take \_ Ownership \_ Name в [*маркере доступа*](/windows/desktop/SecGloss/a-gly)вызывающего объекта, после чего группа администраторов локальной системы делает ее владельцем.</span><span class="sxs-lookup"><span data-stu-id="572cc-107">To give the administrator ownership, the example enables the SE\_TAKE\_OWNERSHIP\_NAME privilege in the caller's [*access token*](/windows/desktop/SecGloss/a-gly), and makes the local system's Administrators group the owner of the object.</span></span> <span data-ttu-id="572cc-108">Если вызывающий участник является членом группы "Администраторы", код сможет изменить список DACL объекта.</span><span class="sxs-lookup"><span data-stu-id="572cc-108">If the caller is a member of the Administrators group, the code will then be able to change the object's DACL.</span></span>

<span data-ttu-id="572cc-109">Чтобы включить и отключить привилегии, в этом примере используется функция образца Сетпривилеже, описанная в разделе [Включение и отключение привилегий в C++](enabling-and-disabling-privileges-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="572cc-109">To enable and disable privileges, this example uses the SetPrivilege sample function described in [Enabling and Disabling Privileges in C++](enabling-and-disabling-privileges-in-c--.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <accctrl.h>
#include <aclapi.h>

//Forward declaration of SetPrivilege
BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) ;


BOOL TakeOwnership(LPTSTR lpszOwnFile) 
{

    BOOL bRetval = FALSE;

    HANDLE hToken = NULL; 
    PSID pSIDAdmin = NULL;
    PSID pSIDEveryone = NULL;
    PACL pACL = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    const int NUM_ACES  = 2;
    EXPLICIT_ACCESS ea[NUM_ACES];
    DWORD dwRes;

    // Specify the DACL to use.
    // Create a SID for the Everyone group.
    if (!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0,
                     0, 0, 0, 0, 0, 0,
                     &pSIDEveryone)) 
    {
        printf("AllocateAndInitializeSid (Everyone) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    // Create a SID for the BUILTIN\Administrators group.
    if (!AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSIDAdmin)) 
    {
        printf("AllocateAndInitializeSid (Admin) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    ZeroMemory(&ea, NUM_ACES * sizeof(EXPLICIT_ACCESS));

    // Set read access for Everyone.
    ea[0].grfAccessPermissions = GENERIC_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance = NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName = (LPTSTR) pSIDEveryone;

    // Set full control for Administrators.
    ea[1].grfAccessPermissions = GENERIC_ALL;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance = NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName = (LPTSTR) pSIDAdmin;

    if (ERROR_SUCCESS != SetEntriesInAcl(NUM_ACES,
                                         ea,
                                         NULL,
                                         &pACL))
    {
        printf("Failed SetEntriesInAcl\n");
        goto Cleanup;
    }

    // Try to modify the object's DACL.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (ERROR_SUCCESS == dwRes) 
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE;
        // No more processing needed.
        goto Cleanup;
    }
    if (dwRes != ERROR_ACCESS_DENIED)
    {
        printf("First SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
        goto Cleanup;
    }

    // If the preceding call failed because access was denied, 
    // enable the SE_TAKE_OWNERSHIP_NAME privilege, create a SID for 
    // the Administrators group, take ownership of the object, and 
    // disable the privilege. Then try again to set the object's DACL.

    // Open a handle to the access token for the calling process.
    if (!OpenProcessToken(GetCurrentProcess(), 
                          TOKEN_ADJUST_PRIVILEGES, 
                          &hToken)) 
       {
          printf("OpenProcessToken failed: %u\n", GetLastError()); 
          goto Cleanup; 
       } 

    // Enable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, TRUE)) 
    {
        printf("You must be logged on as Administrator.\n");
        goto Cleanup; 
    }

    // Set the owner in the object's security descriptor.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        OWNER_SECURITY_INFORMATION,  // change only the object's owner
        pSIDAdmin,                   // SID of Administrator group
        NULL,
        NULL,
        NULL); 

    if (dwRes != ERROR_SUCCESS) 
    {
        printf("Could not set owner. Error: %u\n", dwRes); 
        goto Cleanup;
    }
        
    // Disable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, FALSE)) 
    {
        printf("Failed SetPrivilege call unexpectedly.\n");
        goto Cleanup;
    }

    // Try again to modify the object's DACL,
    // now that we are the owner.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (dwRes == ERROR_SUCCESS)
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE; 
    }
    else
    {
        printf("Second SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
    }

Cleanup:

    if (pSIDAdmin)
        FreeSid(pSIDAdmin); 

    if (pSIDEveryone)
        FreeSid(pSIDEveryone); 

    if (pACL)
       LocalFree(pACL);

    if (hToken)
       CloseHandle(hToken);

    return bRetval;

}
```



 

 
