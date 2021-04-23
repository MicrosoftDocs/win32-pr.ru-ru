---
description: Описывает, как определить, доступен ли конкретный набор API на текущем устройстве.
title: Определение доступности набора API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/24/2020
ms.locfileid: "104134779"
---
# <a name="detect-api-set-availability"></a><span data-ttu-id="a2ee6-103">Определение доступности набора API</span><span class="sxs-lookup"><span data-stu-id="a2ee6-103">Detect API set availability</span></span>

<span data-ttu-id="a2ee6-104">В некоторых случаях заданное имя контракта набора API может быть намеренно сопоставлено с пустым именем модуля на некоторых устройствах Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="a2ee6-105">Причины этого различаются, но распространенным примером является то, что дорогостоящая функция в терминах системных ресурсов может быть удалена из операционной системы Windows при настройке устройства с ограничением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="a2ee6-106">Это создает проблему, которая позволяет приложениям корректно управлять дополнительными функциями на уровне API.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="a2ee6-107">Традиционным подходом для проверки доступности API Win32 является использование [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="a2ee6-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="a2ee6-108">Однако это не является надежным средством для тестирования наборов API из-за поддержки [обратных переадресаций](api-set-loader-operation.md#reverse-forwarding) в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="a2ee6-109">Если к заданному API применяется обратная переадресация, то **LoadLibrary** или **GetProcAddress** могут разрешаться в допустимый указатель на функцию даже в тех случаях, когда внутренняя реализация была удалена.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="a2ee6-110">В этом случае указатель функции будет указывать на функцию-заглушку, которая просто возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="a2ee6-111">Чтобы обнаружить этот случай, можно использовать функцию [исаписетимплементед](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) для запроса базовой доступности данной реализации API.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="a2ee6-112">Этот тест проверяет, что вызов этой функции приведет к выполнению функциональной реализации API.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="a2ee6-113">В следующем примере кода показано, как использовать **исаписетимплементед** , чтобы определить, доступна ли функция [втсенумератесессионс](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) на текущем устройстве перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="a2ee6-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

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