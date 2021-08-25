---
description: Описывает, как определить, доступен ли конкретный набор API на текущем устройстве.
title: Определение доступности набора API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: cc4e26c6e59cfa0af095b297efb72a52d0be30a89a23d42d169e3bf45e72fd13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896534"
---
# <a name="detect-api-set-availability"></a>Определение доступности набора API

в некоторых случаях заданное имя контракта набора API может быть намеренно сопоставлено с пустым именем модуля на некоторых Windows 10 устройствах. причины этого различаются, но распространенным примером является то, что дорогостоящая функция в терминах системных ресурсов может быть удалена из Windows ос при настройке устройства с ограничением ресурсов. Это создает проблему, которая позволяет приложениям корректно управлять дополнительными функциями на уровне API.

Традиционным подходом для проверки доступности API Win32 является использование [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Однако это не является надежным средством для тестирования наборов API из-за поддержки [обратных переадресаций](api-set-loader-operation.md#reverse-forwarding) в Windows 10. Если к заданному API применяется обратная переадресация, то **LoadLibrary** или **GetProcAddress** могут разрешаться в допустимый указатель на функцию даже в тех случаях, когда внутренняя реализация была удалена. В этом случае указатель функции будет указывать на функцию-заглушку, которая просто возвращает ошибку.

Чтобы обнаружить этот случай, можно использовать функцию [исаписетимплементед](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) для запроса базовой доступности данной реализации API. Этот тест проверяет, что вызов этой функции приведет к выполнению функциональной реализации API.

В следующем примере кода показано, как использовать **исаписетимплементед** , чтобы определить, доступна ли функция [втсенумератесессионс](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) на текущем устройстве перед вызовом. 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```