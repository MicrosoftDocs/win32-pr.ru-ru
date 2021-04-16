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
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="5abb5-103">Изменение элементов сведений о пользователе</span><span class="sxs-lookup"><span data-stu-id="5abb5-103">Changing Elements of User Information</span></span>

<span data-ttu-id="5abb5-104">Функции управления сетью предоставляют разнообразные уровни информации, помогающие изменить сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="5abb5-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="5abb5-105">Для успешного выполнения некоторых уровней требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="5abb5-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="5abb5-106">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="5abb5-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="5abb5-107">В примере кода в этом разделе показано, как изменить несколько элементов пользовательской информации, вызвав функцию [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-108">В коде используются различные структуры сведений об управлении сетью.</span><span class="sxs-lookup"><span data-stu-id="5abb5-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="5abb5-109">При изменении сведений о пользователе лучше использовать конкретный уровень для этого элемента информации.</span><span class="sxs-lookup"><span data-stu-id="5abb5-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="5abb5-110">Это предотвращает случайный сброс несвязанных данных при использовании значений нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="5abb5-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="5abb5-111">Настройка некоторых наиболее часто используемых уровней показана в следующих примерах кода:</span><span class="sxs-lookup"><span data-stu-id="5abb5-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="5abb5-112">Задание пароля пользователя, уровень 1003</span><span class="sxs-lookup"><span data-stu-id="5abb5-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="5abb5-113">Настройка привилегии пользователя, уровень 1005</span><span class="sxs-lookup"><span data-stu-id="5abb5-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="5abb5-114">Настройка домашнего каталога пользователя, уровень 1006</span><span class="sxs-lookup"><span data-stu-id="5abb5-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="5abb5-115">Настройка поля "комментарий пользователя", уровень 1007</span><span class="sxs-lookup"><span data-stu-id="5abb5-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="5abb5-116">Установка пользовательских флагов, уровень 1008</span><span class="sxs-lookup"><span data-stu-id="5abb5-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="5abb5-117">Задание пути к сценарию пользователя, уровень 1009</span><span class="sxs-lookup"><span data-stu-id="5abb5-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="5abb5-118">Установка флагов центра пользователей, уровень 1010</span><span class="sxs-lookup"><span data-stu-id="5abb5-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="5abb5-119">Настройка полного имени пользователя, уровень 1011</span><span class="sxs-lookup"><span data-stu-id="5abb5-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="5abb5-120">Во всех фрагментах кода предполагается, что пользователь определил директиву компиляции Юникода и включил соответствующие файлы заголовка пакета SDK следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5abb5-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


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



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="5abb5-121">Задание пароля пользователя, уровень 1003</span><span class="sxs-lookup"><span data-stu-id="5abb5-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="5abb5-122">В следующем фрагменте кода показано, как задать для пароля пользователя известное значение с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-123">В [**разделе \_ сведения о пользователе \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


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



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="5abb5-124">Настройка привилегии пользователя, уровень 1005</span><span class="sxs-lookup"><span data-stu-id="5abb5-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="5abb5-125">В следующем фрагменте кода показано, как задать уровень привилегий, назначенных пользователю с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-126">В [**разделе \_ сведения о пользователе \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="5abb5-127">Дополнительные сведения о правах доступа к учетной записи см. в разделе [привилегии](/windows/desktop/SecAuthZ/privileges) и [константы авторизации](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="5abb5-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


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



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="5abb5-128">Настройка домашнего каталога пользователя, уровень 1006</span><span class="sxs-lookup"><span data-stu-id="5abb5-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="5abb5-129">В следующем фрагменте кода показано, как указать путь к домашнему каталогу пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-130">Каталог может быть жестко запрограммированным путем или допустимым путем в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5abb5-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="5abb5-131">В [**разделе \_ сведения о пользователе \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


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



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="5abb5-132">Настройка поля "комментарий пользователя", уровень 1007</span><span class="sxs-lookup"><span data-stu-id="5abb5-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="5abb5-133">В следующем фрагменте кода показано, как связать комментарий с пользователем путем вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-134">В [**разделе \_ сведения о пользователе \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


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



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="5abb5-135">Установка пользовательских флагов, уровень 1008</span><span class="sxs-lookup"><span data-stu-id="5abb5-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="5abb5-136">В следующем фрагменте кода показано, как задать пользовательские флаги с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-137">В [**разделе \_ сведения о пользователе \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) содержится список допустимых значений флагов и описание каждого флага.</span><span class="sxs-lookup"><span data-stu-id="5abb5-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="5abb5-138">Обратите внимание, что \_ флаг сценария УФ должен быть установлен для сетей Windows NT, windows 2000, Windows XP и LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="5abb5-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="5abb5-139">Попытка задать другие флаги без задания УФ \_ скрипта в этих сетях приведет к сбою функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


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



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="5abb5-140">Задание пути к сценарию пользователя, уровень 1009</span><span class="sxs-lookup"><span data-stu-id="5abb5-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="5abb5-141">В следующем фрагменте кода показано, как задать путь для файла сценария входа определенного пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-142">Файл скрипта может иметь значение. CMD File,. EXE-файл или. Файл BAT.</span><span class="sxs-lookup"><span data-stu-id="5abb5-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="5abb5-143">Строка может также иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="5abb5-143">The string can also be null.</span></span> <span data-ttu-id="5abb5-144">В [**разделе \_ сведения о пользователе \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


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



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="5abb5-145">Установка флагов центра пользователей, уровень 1010</span><span class="sxs-lookup"><span data-stu-id="5abb5-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="5abb5-146">В следующем фрагменте кода показано, как задать флаги привилегий оператора для пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-147">В [**разделе \_ сведения о пользователе \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) содержится список допустимых значений флагов и описание каждого флага.</span><span class="sxs-lookup"><span data-stu-id="5abb5-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


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



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="5abb5-148">Настройка полного имени пользователя, уровень 1011</span><span class="sxs-lookup"><span data-stu-id="5abb5-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="5abb5-149">В следующем фрагменте кода показано, как задать полное имя пользователя с помощью вызова функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="5abb5-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="5abb5-150">В [**разделе \_ сведения о пользователе \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5abb5-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


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



 

 