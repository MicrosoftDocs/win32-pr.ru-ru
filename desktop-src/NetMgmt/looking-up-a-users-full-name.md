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
# <a name="looking-up-a-users-full-name"></a>Поиск полного имени пользователя

Компьютеры могут быть организованы в *домен*, который представляет собой набор компьютеров в сети. Администратор домена хранит сведения об учетной записи централизованного пользователя и группы.

Поиск полного имени пользователя с учетом имени пользователя и имени домена:

-   Преобразование имени пользователя и доменного имени в Юникод, если они еще не являются строками в Юникоде.
-   Найдите имя компьютера контроллера домена (DC), вызвав [**нетжетдкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Найдите имя пользователя на компьютере контроллера домена, вызвав [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Преобразуйте полное имя пользователя в ANSI, если программа не ожидает работы со строками в Юникоде.

Следующий пример кода — это функция (FullName), которая принимает имя пользователя и доменное имя в первых двух аргументах и возвращает полное имя пользователя в третьем аргументе.


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



 

 




