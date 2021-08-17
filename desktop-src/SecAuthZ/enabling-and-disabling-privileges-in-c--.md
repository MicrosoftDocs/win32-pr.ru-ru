---
description: Включение привилегий в маркере доступа позволяет процессу выполнять действия на уровне системы, которые раньше не могли.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Включение и отключение привилегий в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781730"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Включение и отключение привилегий в C++

Включение привилегий в маркере доступа позволяет процессу выполнять действия на уровне системы, которые раньше не могли. Приложение должно тщательно проверять, подходит ли привилегия для типа учетной записи, особенно для следующих мощных привилегий.



| Константа прав доступа           | Строковое значение                  | Отображаемое имя                        |
|------------------------------|-------------------------------|-------------------------------------|
| SE \_ \_имя ассигнпримаритокен | SeAssignPrimaryTokenPrivilege | Замена токена уровня процесса       |
| SE \_ имя РЕЗЕРВной копии \_             | SeBackupPrivilege             | Архивация файлов и каталогов       |
| SE \_ \_имя отладки              | SeBackupPrivilege              | Отладка программ                      |
| SE \_ УВЕЛИЧИТЬ \_ имя квоты \_    | SeIncreaseQuotaPrivilege      | Настройка квот памяти для процесса  |
| SE \_ \_имя TCB                | SeTcbPrivilege                | работа в качества части операционной системы; |



 

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



 

