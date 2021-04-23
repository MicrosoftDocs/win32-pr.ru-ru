---
description: В следующем примере используются функции OpenProcessToken и GetTokenInformation для получения членства в группах в маркере доступа.
ms.assetid: f895dfef-75ad-419c-95d0-6480bdf9c769
title: Поиск идентификатора безопасности в маркере доступа в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713f69511f780898641e65f22503e595706307ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662566"
---
# <a name="searching-for-a-sid-in-an-access-token-in-c"></a><span data-ttu-id="4531e-103">Поиск идентификатора безопасности в маркере доступа в C++</span><span class="sxs-lookup"><span data-stu-id="4531e-103">Searching for a SID in an Access Token in C++</span></span>

<span data-ttu-id="4531e-104">В следующем примере используются функции [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) и [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) для получения членства в группах в [*маркере доступа*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="4531e-104">The following example uses the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) functions to get the group memberships in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="4531e-105">Затем используется функция [**аллокатеандинитиализесид**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) для создания идентификатора безопасности, определяющего известный идентификатор безопасности группы администраторов для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="4531e-105">Then it uses the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function to create a SID that identifies the well-known SID of the administrator group for the local computer.</span></span> <span data-ttu-id="4531e-106">Затем используется функция [**екуалсид**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) для сравнения ИЗВЕСТНОГО идентификатора безопасности с идентификаторами SID группы из маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="4531e-106">Next, it uses the [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) function to compare the well-known SID with the group SIDs from the access token.</span></span> <span data-ttu-id="4531e-107">Если идентификатор безопасности имеется в токене, функция проверяет атрибуты SID, чтобы определить, включена ли она.</span><span class="sxs-lookup"><span data-stu-id="4531e-107">If the SID is present in the token, the function checks the attributes of the SID to determine whether it is enabled.</span></span>

<span data-ttu-id="4531e-108">Функция [**чекктокенмембершип**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) должна использоваться для определения наличия и включения указанного идентификатора безопасности в маркере доступа.</span><span class="sxs-lookup"><span data-stu-id="4531e-108">The [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) function should be used to determine whether a specified SID is present and enabled in an access token.</span></span> <span data-ttu-id="4531e-109">Эта функция устраняет потенциальные некорректности интерпретации членства в активной группе.</span><span class="sxs-lookup"><span data-stu-id="4531e-109">This function eliminates potential misinterpretations of the active group membership.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "advapi32.lib")

#define MAX_NAME 256

BOOL SearchTokenGroupsForSID (VOID) 
{
    DWORD i, dwSize = 0, dwResult = 0;
    HANDLE hToken;
    PTOKEN_GROUPS pGroupInfo;
    SID_NAME_USE SidType;
    char lpName[MAX_NAME];
    char lpDomain[MAX_NAME];
    PSID pSID = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuth = SECURITY_NT_AUTHORITY;
       
    // Open a handle to the access token for the calling process.

    if (!OpenProcessToken( GetCurrentProcess(), TOKEN_QUERY, &hToken )) 
    {
        printf( "OpenProcessToken Error %u\n", GetLastError() );
        return FALSE;
    }

    // Call GetTokenInformation to get the buffer size.

    if(!GetTokenInformation(hToken, TokenGroups, NULL, dwSize, &dwSize)) 
    {
        dwResult = GetLastError();
        if( dwResult != ERROR_INSUFFICIENT_BUFFER ) {
            printf( "GetTokenInformation Error %u\n", dwResult );
            return FALSE;
        }
    }

    // Allocate the buffer.

    pGroupInfo = (PTOKEN_GROUPS) GlobalAlloc( GPTR, dwSize );

    // Call GetTokenInformation again to get the group information.

    if(! GetTokenInformation(hToken, TokenGroups, pGroupInfo, 
                            dwSize, &dwSize ) ) 
    {
        printf( "GetTokenInformation Error %u\n", GetLastError() );
        return FALSE;
    }

    // Create a SID for the BUILTIN\Administrators group.

    if(! AllocateAndInitializeSid( &SIDAuth, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSID) ) 
    {
        printf( "AllocateAndInitializeSid Error %u\n", GetLastError() );
        return FALSE;
    }

    // Loop through the group SIDs looking for the administrator SID.

    for(i=0; i<pGroupInfo->GroupCount; i++) 
    {
        if ( EqualSid(pSID, pGroupInfo->Groups[i].Sid) ) 
        {

            // Lookup the account name and print it.

            dwSize = MAX_NAME;
            if( !LookupAccountSid( NULL, pGroupInfo->Groups[i].Sid,
                                  lpName, &dwSize, lpDomain, 
                                  &dwSize, &SidType ) ) 
            {
                dwResult = GetLastError();
                if( dwResult == ERROR_NONE_MAPPED )
                   strcpy_s (lpName, dwSize, "NONE_MAPPED" );
                else 
                {
                    printf("LookupAccountSid Error %u\n", GetLastError());
                    return FALSE;
                }
            }
            printf( "Current user is a member of the %s\\%s group\n", 
                    lpDomain, lpName );

            // Find out whether the SID is enabled in the token.
            if (pGroupInfo->Groups[i].Attributes & SE_GROUP_ENABLED)
                printf("The group SID is enabled.\n");
            else if (pGroupInfo->Groups[i].Attributes & 
                              SE_GROUP_USE_FOR_DENY_ONLY)
                printf("The group SID is a deny-only SID.\n");
            else 
                printf("The group SID is not enabled.\n");
        }
    }

    if (pSID)
        FreeSid(pSID);
    if ( pGroupInfo )
        GlobalFree( pGroupInfo );
    return TRUE;
}
```



 

 
