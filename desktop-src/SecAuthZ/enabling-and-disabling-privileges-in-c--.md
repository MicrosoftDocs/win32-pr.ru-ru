---
description: Включение привилегий в маркере доступа позволяет процессу выполнять действия на уровне системы, которые раньше не могли.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Включение и отключение привилегий в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081287"
---
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="22e4c-103">Включение и отключение привилегий в C++</span><span class="sxs-lookup"><span data-stu-id="22e4c-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="22e4c-104">Включение привилегий в маркере доступа позволяет процессу выполнять действия на уровне системы, которые раньше не могли.</span><span class="sxs-lookup"><span data-stu-id="22e4c-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="22e4c-105">Приложение должно тщательно проверять, подходит ли привилегия для типа учетной записи, особенно для следующих мощных привилегий.</span><span class="sxs-lookup"><span data-stu-id="22e4c-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="22e4c-106">Константа прав доступа</span><span class="sxs-lookup"><span data-stu-id="22e4c-106">Privilege constant</span></span>           | <span data-ttu-id="22e4c-107">Строковое значение</span><span class="sxs-lookup"><span data-stu-id="22e4c-107">String value</span></span>                  | <span data-ttu-id="22e4c-108">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="22e4c-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="22e4c-109">\_имя ассигнпримаритокен для SE \_</span><span class="sxs-lookup"><span data-stu-id="22e4c-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="22e4c-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="22e4c-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="22e4c-111">Замена маркера уровня процесса</span><span class="sxs-lookup"><span data-stu-id="22e4c-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="22e4c-112">SE \_ имя резервной копии \_</span><span class="sxs-lookup"><span data-stu-id="22e4c-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="22e4c-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="22e4c-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="22e4c-114">Архивация файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="22e4c-114">Back up files and directories</span></span>       |
| <span data-ttu-id="22e4c-115">\_имя отладки для SE \_</span><span class="sxs-lookup"><span data-stu-id="22e4c-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="22e4c-116">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="22e4c-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="22e4c-117">Отладка программ</span><span class="sxs-lookup"><span data-stu-id="22e4c-117">Debug programs</span></span>                      |
| <span data-ttu-id="22e4c-118">SE \_ увеличение \_ имени квоты \_</span><span class="sxs-lookup"><span data-stu-id="22e4c-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="22e4c-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="22e4c-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="22e4c-120">Настройка квот памяти для процесса</span><span class="sxs-lookup"><span data-stu-id="22e4c-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="22e4c-121">\_имя TCB (SE) \_</span><span class="sxs-lookup"><span data-stu-id="22e4c-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="22e4c-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="22e4c-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="22e4c-123">работа в качества части операционной системы;</span><span class="sxs-lookup"><span data-stu-id="22e4c-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="22e4c-124">Перед включением любой из этих потенциально опасных привилегий определите, чтобы функции или операции в коде действительно требовали привилегий.</span><span class="sxs-lookup"><span data-stu-id="22e4c-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="22e4c-125">Например, очень малое число функций в операционной системе действительно требует **SeTcbPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="22e4c-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="22e4c-126">Список всех доступных привилегий см. в разделе [константы прав](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="22e4c-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="22e4c-127">В следующем примере показано, как включить или отключить привилегии в [*маркере доступа*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="22e4c-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="22e4c-128">В примере вызывается функция [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) для получения [*локально уникального идентификатора*](/windows/desktop/SecGloss/l-gly) (LUID), используемого локальной системой для идентификации привилегий.</span><span class="sxs-lookup"><span data-stu-id="22e4c-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="22e4c-129">Затем в примере вызывается функция [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , которая либо включает, либо отключает привилегию, зависящую от значения параметра *бенаблепривилеже* .</span><span class="sxs-lookup"><span data-stu-id="22e4c-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

