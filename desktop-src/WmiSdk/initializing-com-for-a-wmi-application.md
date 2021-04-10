---
description: Первым шагом при подключении к WMI является настройка вызовов COM для CoInitializeEx и CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Инициализация COM для приложения WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999557"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="e0863-103">Инициализация COM для приложения WMI</span><span class="sxs-lookup"><span data-stu-id="e0863-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="e0863-104">Первым шагом при подключении к WMI является настройка вызовов COM для [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="e0863-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="e0863-105">В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.</span><span class="sxs-lookup"><span data-stu-id="e0863-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="e0863-106">В следующей процедуре описывается инициализация COM из клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e0863-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="e0863-107">**Инициализация COM из клиентского приложения**</span><span class="sxs-lookup"><span data-stu-id="e0863-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="e0863-108">Инициализируйте COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="e0863-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="e0863-109">Вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) является стандартной процедурой для настройки COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e0863-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="e0863-110">Таким образом, Инструментарий WMI не требует наличия дополнительных процедур при вызове **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="e0863-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="e0863-111">Дополнительные сведения см. в разделе [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="e0863-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="e0863-112">В следующем примере кода показано, как вызвать [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="e0863-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="e0863-113">Задайте общие уровни безопасности COM с помощью вызова интерфейса [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="e0863-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="e0863-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) — это стандартная функция, которую необходимо вызывать при настройке COM-интерфейса для процесса.</span><span class="sxs-lookup"><span data-stu-id="e0863-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="e0863-115">Вызовите **CoInitializeSecurity** , если хотите задать параметры безопасности по умолчанию для проверки подлинности, олицетворения или службы проверки подлинности для всего процесса.</span><span class="sxs-lookup"><span data-stu-id="e0863-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="e0863-116">Дополнительные сведения см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="e0863-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="e0863-117">Если вы хотите задать или изменить безопасность для определенного прокси-сервера, необходимо вызвать метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="e0863-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="e0863-118">Используйте **CoSetProxyBlanket** всякий раз, когда необходимо задать или изменить безопасность COM при выполнении внутри другого процесса, где нельзя управлять параметрами безопасности по умолчанию для проверки подлинности, олицетворения или службы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e0863-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="e0863-119">Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-подключения](setting-the-security-levels-on-a-wmi-connection.md) и [Настройка параметров безопасности для IWbemServices и других прокси-серверов](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="e0863-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="e0863-120">Инструментарий WMI имеет несколько проблем безопасности, о которых следует помнить при программировании клиентского приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="e0863-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="e0863-121">Дополнительные сведения см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="e0863-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="e0863-122">В следующем примере кода показано, как вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы установить безопасность COM для процесса.</span><span class="sxs-lookup"><span data-stu-id="e0863-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

<span data-ttu-id="e0863-123">После инициализации COM необходимо создать соединение с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="e0863-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="e0863-124">Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e0863-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0863-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e0863-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0863-126">Создание приложения WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="e0863-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="e0863-127">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="e0863-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
