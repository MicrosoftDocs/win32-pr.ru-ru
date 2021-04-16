---
title: Изменение элементов сведений о пользователе
description: Функции управления сетью предоставляют разнообразные уровни информации, помогающие изменить сведения о пользователе.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672297"
---
# <a name="changing-elements-of-user-information"></a>Изменение элементов сведений о пользователе

Функции управления сетью предоставляют разнообразные уровни информации, помогающие изменить сведения о пользователе. Для успешного выполнения некоторых уровней требуются права администратора. Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).

В примере кода в этом разделе показано, как изменить несколько элементов пользовательской информации, вызвав функцию [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В коде используются различные структуры сведений об управлении сетью.

При изменении сведений о пользователе лучше использовать конкретный уровень для этого элемента информации. Это предотвращает случайный сброс несвязанных данных при использовании значений нижнего уровня.

Настройка некоторых наиболее часто используемых уровней показана в следующих примерах кода:

-   [Задание пароля пользователя, уровень 1003](#setting-the-user-password-level-1003)
-   [Настройка привилегии пользователя, уровень 1005](#setting-the-user-privilege-level-1005)
-   [Настройка домашнего каталога пользователя, уровень 1006](#setting-the-user-home-directory-level-1006)
-   [Настройка поля "комментарий пользователя", уровень 1007](#setting-the-user-comment-field-level-1007)
-   [Установка пользовательских флагов, уровень 1008](#setting-the-user-flags-level-1008)
-   [Задание пути к сценарию пользователя, уровень 1009](#setting-the-user-script-path-level-1009)
-   [Установка флагов центра пользователей, уровень 1010](#setting-the-user-authority-flags-level-1010)
-   [Настройка полного имени пользователя, уровень 1011](#setting-the-user-full-name-level-1011)

Во всех фрагментах кода предполагается, что пользователь определил директиву компиляции Юникода и включил соответствующие файлы заголовка пакета SDK следующим образом:


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a>Задание пароля пользователя, уровень 1003

В следующем фрагменте кода показано, как задать для пароля пользователя известное значение с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) содержатся дополнительные сведения.


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a>Настройка привилегии пользователя, уровень 1005

В следующем фрагменте кода показано, как задать уровень привилегий, назначенных пользователю с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) содержатся дополнительные сведения. Дополнительные сведения о правах доступа к учетной записи см. в разделе [привилегии](/windows/desktop/SecAuthZ/privileges) и [константы авторизации](/windows/desktop/SecAuthZ/authorization-constants).


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a>Настройка домашнего каталога пользователя, уровень 1006

В следующем фрагменте кода показано, как указать путь к домашнему каталогу пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . Каталог может быть жестко запрограммированным путем или допустимым путем в Юникоде. В [**разделе \_ сведения о пользователе \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) содержатся дополнительные сведения.


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a>Настройка поля "комментарий пользователя", уровень 1007

В следующем фрагменте кода показано, как связать комментарий с пользователем путем вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) содержатся дополнительные сведения.


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a>Установка пользовательских флагов, уровень 1008

В следующем фрагменте кода показано, как задать пользовательские флаги с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) содержится список допустимых значений флагов и описание каждого флага.

Обратите внимание, что \_ флаг сценария УФ должен быть установлен для сетей Windows NT, windows 2000, Windows XP и LAN Manager. Попытка задать другие флаги без задания УФ \_ скрипта в этих сетях приведет к сбою функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a>Задание пути к сценарию пользователя, уровень 1009

В следующем фрагменте кода показано, как задать путь для файла сценария входа определенного пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . Файл скрипта может иметь значение. CMD File,. EXE-файл или. Файл BAT. Строка может также иметь значение null. В [**разделе \_ сведения о пользователе \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) содержатся дополнительные сведения.


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a>Установка флагов центра пользователей, уровень 1010

В следующем фрагменте кода показано, как задать флаги привилегий оператора для пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) содержится список допустимых значений флагов и описание каждого флага.


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a>Настройка полного имени пользователя, уровень 1011

В следующем фрагменте кода показано, как задать полное имя пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . В [**разделе \_ сведения о пользователе \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) содержатся дополнительные сведения.


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 