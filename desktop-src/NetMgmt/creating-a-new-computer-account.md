---
title: Создание новой учетной записи компьютера
description: В следующем примере кода показано, как создать новую учетную запись компьютера с помощью функции Нетусерадд.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672304"
---
# <a name="creating-a-new-computer-account"></a>Создание новой учетной записи компьютера

В следующем примере кода показано, как создать новую учетную запись компьютера с помощью функции [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .

Ниже приведены рекомендации по управлению учетными записями компьютеров.

-   Для согласованности с служебными программами управления учетными записями необходимо указать все символы в верхнем регистре.
-   Имя учетной записи компьютера всегда содержит знак доллара в конце ($). Все функции, используемые для управления учетными записями компьютеров, должны создавать имя компьютера, чтобы последний символ имени учетной записи компьютера был знаком доллара ($). Для междоменного доверия имя учетной записи — Трустингдомаиннаме $.
-   Максимальная длина имени компьютера равна максимальной \_ \_ длине ComputerName (15). Эта длина не включает в себя знак доллара в конце ($).
-   Пароль для новой учетной записи компьютера должен быть строчным представлением имени учетной записи компьютера без знака доллара в конце ($). Для междоменного доверия пароль может быть произвольным значением, которое соответствует значению, указанному на стороне отношения доверия.
-   Максимальная длина пароля — LM20 \_ пвлен (14). Пароль должен быть усечен до этой длины, если длина имени учетной записи компьютера превышает эту длину.
-   Пароль, указанный во время создания учетной записи компьютера, действителен только до тех пор, пока учетная запись компьютера не станет активной в домене. При активации доверительных отношений устанавливается новый пароль.


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



Пользователь, который вызывает функции управления учетной записью, должен иметь права администратора на целевом компьютере. В случае с существующими учетными записями компьютеров создатель учетной записи может управлять учетной записью, независимо от административного членства. Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).

Семачинеаккаунтпривилеже можно предоставить на целевом компьютере, чтобы предоставить определенным пользователям возможность создавать учетные записи компьютеров. Это дает возможность создавать учетные записи компьютеров без прав администратора. Прежде чем добавлять учетную запись компьютера, вызывающая сторона должна включить эту привилегию. Дополнительные сведения о правах доступа к учетной записи см. в разделе [привилегии](/windows/desktop/SecAuthZ/privileges) и [константы авторизации](/windows/desktop/SecAuthZ/authorization-constants).

 

 