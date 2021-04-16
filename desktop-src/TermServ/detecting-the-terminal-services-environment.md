---
title: Обнаружение среды службы удаленных рабочих столов
description: Для оптимизации производительности в приложениях рекомендуется определить, работают ли они в службы удаленных рабочих столовном сеансе клиента.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532153"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Обнаружение среды службы удаленных рабочих столов

Для оптимизации производительности в приложениях рекомендуется определить, работают ли они в службы удаленных рабочих столовном сеансе клиента. Например, если приложение выполняется в удаленном сеансе, оно должно исключить ненужные графические эффекты, как описано в разделе [графические эффекты](graphic-effects.md). Если пользователь запускает приложение в локальной среде, это не так важно для приложения, чтобы оптимизировать его поведение.

В следующем примере показана функция, возвращающая **значение true** , если приложение выполняется в удаленном сеансе, и **значение false** , если приложение выполняется в консоли.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Дополнительные сведения см. [в разделе Связывание во время выполнения с Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Не следует использовать **жетсистемметрикс (SM \_ ремотесессион)** , чтобы определить, выполняется ли приложение в удаленном сеансе в Windows 8 и более поздних версиях или Windows Server 2012 и более поздних версиях, если удаленный сеанс также может использовать улучшения виртуальных GPU RemoteFX в протоколе удаленного интерфейса (RDP) Майкрософт. В этом случае **жетсистемметрикс (SM \_ ремотесессион)** определит удаленный сеанс как локальный сеанс.

Приложение может проверить следующий раздел реестра, чтобы определить, является ли сеанс удаленным сеансом, использующим виртуальный графический процессор RemoteFX. Если локальный сеанс существует, этот раздел реестра предоставляет идентификатор локального сеанса.

**HKEY \_ локальный \_ компьютер \\ система \\ CurrentControlSet \\ Управление \\ сервером терминалов \\ гласссессионид**

Если идентификатор текущего сеанса, в котором выполняется приложение, совпадает с кодом в разделе реестра, приложение выполняется в локальном сеансе. Сеансы, идентифицированные как удаленный сеанс таким образом, включают удаленные сеансы, использующие RemoteFX. Это показано в следующем образце кода.


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 




