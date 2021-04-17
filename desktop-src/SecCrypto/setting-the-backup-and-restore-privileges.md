---
description: Чтобы успешно вызвать API резервного копирования и восстановления служб сертификации, маркер вызывающего объекта должен включать права на резервное копирование и восстановление.
ms.assetid: 409a9fad-7141-4ba8-ab3d-fb590366001e
title: Настройка привилегий резервного копирования и восстановления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd70c3726c435efa1f000add101bbf50b725bb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662121"
---
# <a name="setting-the-backup-and-restore-privileges"></a>Настройка привилегий резервного копирования и восстановления

Чтобы успешно вызвать API резервного копирования и восстановления служб сертификации, маркер вызывающего объекта должен включать [*права*](../secgloss/p-gly.md)на резервное копирование и восстановление. Эти привилегии могут быть заданы программно, и в следующем примере можно задать или удалить эти привилегии. Права на резервное копирование и восстановление необходимы для всех приложений резервного копирования и восстановления, а не только для резервного копирования и восстановления служб сертификатов. Сведения о влиянии на безопасность при изменении привилегий см. в разделе [выполнение с особыми привилегиями](../secbp/running-with-special-privileges.md).


```C++
// The following example can be used to enable or disable the
// backup privilege. By making the indicated substitutions, you can
// also use this example to enable or disable the restore privilege 
// Use the following statement to enable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);
// Use the following statement to disable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, FALSE);
// Use SE_RESTORE_NAME for the restore privilege.
// The main function in this example enables the backup privilege.
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>


HRESULT ModifyPrivilege(
    IN LPCTSTR szPrivilege,
    IN BOOL fEnable)
{
    HRESULT hr = S_OK;
    TOKEN_PRIVILEGES NewState;
    LUID             luid;
    HANDLE hToken    = NULL;

    // Open the process token for this process.
    if (!OpenProcessToken(GetCurrentProcess(),
                          TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY,
                          &hToken ))
    {
        printf("Failed OpenProcessToken\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Get the local unique ID for the privilege.
    if ( !LookupPrivilegeValue( NULL,
                                szPrivilege,
                                &luid ))
    {
        CloseHandle( hToken );
        printf("Failed LookupPrivilegeValue\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Assign values to the TOKEN_PRIVILEGE structure.
    NewState.PrivilegeCount = 1;
    NewState.Privileges[0].Luid = luid;
    NewState.Privileges[0].Attributes = 
              (fEnable ? SE_PRIVILEGE_ENABLED : 0);

    // Adjust the token privilege.
    if (!AdjustTokenPrivileges(hToken,
                               FALSE,
                               &NewState,
                               0,
                               NULL,
                               NULL))
    {
        printf("Failed AdjustTokenPrivileges\n");
        hr = ERROR_FUNCTION_FAILED;
    }

    // Close the handle.
    CloseHandle(hToken);

    return hr;
}

void main(void)
{
    HRESULT hr;

    hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);

    if (!SUCCEEDED(hr))
        printf("\nFailed to modify privilege.\n");
    else
        printf("\nSuccessfully modified privilege.\n");
}

```



 

 
