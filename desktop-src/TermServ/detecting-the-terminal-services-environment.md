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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="16b66-103">Обнаружение среды службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="16b66-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="16b66-104">Для оптимизации производительности в приложениях рекомендуется определить, работают ли они в службы удаленных рабочих столовном сеансе клиента.</span><span class="sxs-lookup"><span data-stu-id="16b66-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="16b66-105">Например, если приложение выполняется в удаленном сеансе, оно должно исключить ненужные графические эффекты, как описано в разделе [графические эффекты](graphic-effects.md).</span><span class="sxs-lookup"><span data-stu-id="16b66-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="16b66-106">Если пользователь запускает приложение в локальной среде, это не так важно для приложения, чтобы оптимизировать его поведение.</span><span class="sxs-lookup"><span data-stu-id="16b66-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="16b66-107">В следующем примере показана функция, возвращающая **значение true** , если приложение выполняется в удаленном сеансе, и **значение false** , если приложение выполняется в консоли.</span><span class="sxs-lookup"><span data-stu-id="16b66-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="16b66-108">Дополнительные сведения см. [в разделе Связывание во время выполнения с Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="16b66-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="16b66-109">Не следует использовать **жетсистемметрикс (SM \_ ремотесессион)** , чтобы определить, выполняется ли приложение в удаленном сеансе в Windows 8 и более поздних версиях или Windows Server 2012 и более поздних версиях, если удаленный сеанс также может использовать улучшения виртуальных GPU RemoteFX в протоколе удаленного интерфейса (RDP) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="16b66-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="16b66-110">В этом случае **жетсистемметрикс (SM \_ ремотесессион)** определит удаленный сеанс как локальный сеанс.</span><span class="sxs-lookup"><span data-stu-id="16b66-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="16b66-111">Приложение может проверить следующий раздел реестра, чтобы определить, является ли сеанс удаленным сеансом, использующим виртуальный графический процессор RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="16b66-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="16b66-112">Если локальный сеанс существует, этот раздел реестра предоставляет идентификатор локального сеанса.</span><span class="sxs-lookup"><span data-stu-id="16b66-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="16b66-113">**HKEY \_ локальный \_ компьютер \\ система \\ CurrentControlSet \\ Управление \\ сервером терминалов \\ гласссессионид**</span><span class="sxs-lookup"><span data-stu-id="16b66-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="16b66-114">Если идентификатор текущего сеанса, в котором выполняется приложение, совпадает с кодом в разделе реестра, приложение выполняется в локальном сеансе.</span><span class="sxs-lookup"><span data-stu-id="16b66-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="16b66-115">Сеансы, идентифицированные как удаленный сеанс таким образом, включают удаленные сеансы, использующие RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="16b66-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="16b66-116">Это показано в следующем образце кода.</span><span class="sxs-lookup"><span data-stu-id="16b66-116">The following sample code demonstrates this.</span></span>


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



 

 




