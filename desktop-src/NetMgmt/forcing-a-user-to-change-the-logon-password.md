---
title: Принудительное изменение пароля для входа пользователем
description: В этом примере кода показано, как заставить пользователя изменить пароль для входа при следующем входе с помощью функций Нетусержетинфо и Нетусерсетинфо и \_ структуры User info \_ 3.
ms.assetid: 828f5d72-3e19-4b65-a1db-ac702fd4cfde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3d0910f77c2553a55a53f1393aae5c9535982
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888555"
---
# <a name="forcing-a-user-to-change-the-logon-password"></a><span data-ttu-id="058f7-103">Принудительное изменение пароля для входа пользователем</span><span class="sxs-lookup"><span data-stu-id="058f7-103">Forcing a User to Change the Logon Password</span></span>

<span data-ttu-id="058f7-104">В этом примере кода показано, как заставить пользователя изменить пароль для входа при следующем входе с помощью функций [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) и [**Нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) и структуры [**user \_ info \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="058f7-104">This code sample demonstrates how to force a user to change the logon password on the next logon using the [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions and the [**USER\_INFO\_3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) structure.</span></span> <span data-ttu-id="058f7-105">Обратите внимание, что начиная с Windows XP вместо этого рекомендуется использовать структуру [**user \_ info \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) .</span><span class="sxs-lookup"><span data-stu-id="058f7-105">Note that starting with Windows XP, it is recommended that you use the [**USER\_INFO\_4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) structure instead.</span></span>

<span data-ttu-id="058f7-106">Задайте ненулевое значение для члена **usri3 \_ Password с \_ истекшим сроком действия** структуры **пользователя \_ \_ 3** , используя следующий фрагмент кода:</span><span class="sxs-lookup"><span data-stu-id="058f7-106">Set the **usri3\_password\_expired** member of the **USER\_INFO\_3** structure to a nonzero value using the following code fragment:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

#define USERNAME L"your_user_name"
#define SERVER L"\\\\server"

void main( void )
{
    PUSER_INFO_3 pUsr = NULL;
    NET_API_STATUS netRet = 0;
    DWORD dwParmError = 0;
 //
 // First, retrieve the user information at level 3. This is 
 // necessary to prevent resetting other user information when 
 // the NetUserSetInfo call is made.
 //
   netRet = NetUserGetInfo( SERVER, USERNAME, 3, (LPBYTE *)&pUsr);

   if( netRet == NERR_Success )
   {
     //
     // The function was successful; set the usri3_password_expired value to 
     // a nonzero value. Call the NetUserSetInfo function.
     //
        pUsr->usri3_password_expired = TRUE;
        netRet = NetUserSetInfo( SERVER, USERNAME, 3, (LPBYTE)pUsr, &dwParmError);
    //
    // A zero return indicates success. 
    // If the return value is ERROR_INVALID_PARAMETER, 
    //  the dwParmError parameter will contain a value indicating the 
    //  invalid parameter within the user_info_3 structure. These values 
    //  are defined in the lmaccess.h file.
    //
        if( netRet == NERR_Success )
            printf("User %S will need to change password at next logon", USERNAME);
        else printf("Error %d occurred. Parm Error %d returned.\n", netRet, dwParmError);
    //
    // Must free the buffer returned by NetUserGetInfo.
    //
        NetApiBufferFree( pUsr);
    }
    else printf("NetUserGetInfo failed: %d\n", netRet);
}
```



 

 




