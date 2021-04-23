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
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="b982b-103">Создание новой учетной записи компьютера</span><span class="sxs-lookup"><span data-stu-id="b982b-103">Creating a New Computer Account</span></span>

<span data-ttu-id="b982b-104">В следующем примере кода показано, как создать новую учетную запись компьютера с помощью функции [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .</span><span class="sxs-lookup"><span data-stu-id="b982b-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="b982b-105">Ниже приведены рекомендации по управлению учетными записями компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b982b-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="b982b-106">Для согласованности с служебными программами управления учетными записями необходимо указать все символы в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="b982b-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="b982b-107">Имя учетной записи компьютера всегда содержит знак доллара в конце ($).</span><span class="sxs-lookup"><span data-stu-id="b982b-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="b982b-108">Все функции, используемые для управления учетными записями компьютеров, должны создавать имя компьютера, чтобы последний символ имени учетной записи компьютера был знаком доллара ($).</span><span class="sxs-lookup"><span data-stu-id="b982b-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="b982b-109">Для междоменного доверия имя учетной записи — Трустингдомаиннаме $.</span><span class="sxs-lookup"><span data-stu-id="b982b-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="b982b-110">Максимальная длина имени компьютера равна максимальной \_ \_ длине ComputerName (15).</span><span class="sxs-lookup"><span data-stu-id="b982b-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="b982b-111">Эта длина не включает в себя знак доллара в конце ($).</span><span class="sxs-lookup"><span data-stu-id="b982b-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="b982b-112">Пароль для новой учетной записи компьютера должен быть строчным представлением имени учетной записи компьютера без знака доллара в конце ($).</span><span class="sxs-lookup"><span data-stu-id="b982b-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="b982b-113">Для междоменного доверия пароль может быть произвольным значением, которое соответствует значению, указанному на стороне отношения доверия.</span><span class="sxs-lookup"><span data-stu-id="b982b-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="b982b-114">Максимальная длина пароля — LM20 \_ пвлен (14).</span><span class="sxs-lookup"><span data-stu-id="b982b-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="b982b-115">Пароль должен быть усечен до этой длины, если длина имени учетной записи компьютера превышает эту длину.</span><span class="sxs-lookup"><span data-stu-id="b982b-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="b982b-116">Пароль, указанный во время создания учетной записи компьютера, действителен только до тех пор, пока учетная запись компьютера не станет активной в домене.</span><span class="sxs-lookup"><span data-stu-id="b982b-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="b982b-117">При активации доверительных отношений устанавливается новый пароль.</span><span class="sxs-lookup"><span data-stu-id="b982b-117">A new password is established during trust relationship activation.</span></span>


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



<span data-ttu-id="b982b-118">Пользователь, который вызывает функции управления учетной записью, должен иметь права администратора на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="b982b-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="b982b-119">В случае с существующими учетными записями компьютеров создатель учетной записи может управлять учетной записью, независимо от административного членства.</span><span class="sxs-lookup"><span data-stu-id="b982b-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="b982b-120">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="b982b-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="b982b-121">Семачинеаккаунтпривилеже можно предоставить на целевом компьютере, чтобы предоставить определенным пользователям возможность создавать учетные записи компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b982b-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="b982b-122">Это дает возможность создавать учетные записи компьютеров без прав администратора.</span><span class="sxs-lookup"><span data-stu-id="b982b-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="b982b-123">Прежде чем добавлять учетную запись компьютера, вызывающая сторона должна включить эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="b982b-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="b982b-124">Дополнительные сведения о правах доступа к учетной записи см. в разделе [привилегии](/windows/desktop/SecAuthZ/privileges) и [константы авторизации](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="b982b-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 