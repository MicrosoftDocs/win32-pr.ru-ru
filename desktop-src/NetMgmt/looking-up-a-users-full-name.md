---
title: Поиск полного имени пользователя
description: Компьютеры могут быть организованы в домен, который представляет собой набор компьютеров в сети. Администратор домена хранит сведения об учетной записи централизованного пользователя и группы.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661575"
---
# <a name="looking-up-a-users-full-name"></a><span data-ttu-id="1980d-104">Поиск полного имени пользователя</span><span class="sxs-lookup"><span data-stu-id="1980d-104">Looking Up a User's Full Name</span></span>

<span data-ttu-id="1980d-105">Компьютеры могут быть организованы в *домен*, который представляет собой набор компьютеров в сети.</span><span class="sxs-lookup"><span data-stu-id="1980d-105">Computers can be organized into a *domain*, which is a collection of computers network.</span></span> <span data-ttu-id="1980d-106">Администратор домена хранит сведения об учетной записи централизованного пользователя и группы.</span><span class="sxs-lookup"><span data-stu-id="1980d-106">The domain administrator maintains centralized user and group account information.</span></span>

<span data-ttu-id="1980d-107">Поиск полного имени пользователя с учетом имени пользователя и имени домена:</span><span class="sxs-lookup"><span data-stu-id="1980d-107">To find the full name of a user, given the user name and domain name:</span></span>

-   <span data-ttu-id="1980d-108">Преобразование имени пользователя и доменного имени в Юникод, если они еще не являются строками в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1980d-108">Convert the user name and domain name to Unicode, if they are not already Unicode strings.</span></span>
-   <span data-ttu-id="1980d-109">Найдите имя компьютера контроллера домена (DC), вызвав [**нетжетдкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span><span class="sxs-lookup"><span data-stu-id="1980d-109">Look up the computer name of the domain controller (DC) by calling [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span></span>
-   <span data-ttu-id="1980d-110">Найдите имя пользователя на компьютере контроллера домена, вызвав [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span><span class="sxs-lookup"><span data-stu-id="1980d-110">Look up the user name on the DC computer by calling [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span></span>
-   <span data-ttu-id="1980d-111">Преобразуйте полное имя пользователя в ANSI, если программа не ожидает работы со строками в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1980d-111">Convert the full user name to ANSI, unless the program is expecting to work with Unicode strings.</span></span>

<span data-ttu-id="1980d-112">Следующий пример кода — это функция (FullName), которая принимает имя пользователя и доменное имя в первых двух аргументах и возвращает полное имя пользователя в третьем аргументе.</span><span class="sxs-lookup"><span data-stu-id="1980d-112">The following sample code is a function (GetFullName) that takes a user name and a domain name in the first two arguments and returns the user's full name in the third argument.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




