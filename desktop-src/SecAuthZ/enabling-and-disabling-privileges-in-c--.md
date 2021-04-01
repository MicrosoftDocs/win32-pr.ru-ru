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
# <a name="enabling-and-disabling-privileges-in-c"></a>Включение и отключение привилегий в C++

Включение привилегий в маркере доступа позволяет процессу выполнять действия на уровне системы, которые раньше не могли. Приложение должно тщательно проверять, подходит ли привилегия для типа учетной записи, особенно для следующих мощных привилегий.



| Константа прав доступа           | Строковое значение                  | Отображаемое имя                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_имя ассигнпримаритокен для SE \_ | SeAssignPrimaryTokenPrivilege | Замена маркера уровня процесса       |
| SE \_ имя резервной копии \_             | SeBackupPrivilege             | Архивация файлов и каталогов       |
| \_имя отладки для SE \_              | SeBackupPrivilege              | Отладка программ                      |
| SE \_ увеличение \_ имени квоты \_    | SeIncreaseQuotaPrivilege      | Настройка квот памяти для процесса  |
| \_имя TCB (SE) \_                | SeTcbPrivilege                | работа в качества части операционной системы; |



 

Перед включением любой из этих потенциально опасных привилегий определите, чтобы функции или операции в коде действительно требовали привилегий. Например, очень малое число функций в операционной системе действительно требует **SeTcbPrivilege**. Список всех доступных привилегий см. в разделе [константы прав](authorization-constants.md).

В следующем примере показано, как включить или отключить привилегии в [*маркере доступа*](/windows/desktop/SecGloss/a-gly). В примере вызывается функция [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) для получения [*локально уникального идентификатора*](/windows/desktop/SecGloss/l-gly) (LUID), используемого локальной системой для идентификации привилегий. Затем в примере вызывается функция [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , которая либо включает, либо отключает привилегию, зависящую от значения параметра *бенаблепривилеже* .


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



 

