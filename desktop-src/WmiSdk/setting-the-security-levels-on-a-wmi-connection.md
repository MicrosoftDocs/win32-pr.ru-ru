---
description: После получения указателя на прокси-сервер IWbemServices необходимо настроить безопасность прокси-сервера для доступа к WMI через прокси-сервер.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Установка уровней безопасности для WMI-соединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712945"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="66d2b-103">Установка уровней безопасности для WMI-соединения</span><span class="sxs-lookup"><span data-stu-id="66d2b-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="66d2b-104">После получения указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) необходимо настроить безопасность прокси-сервера для доступа к WMI через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="66d2b-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="66d2b-105">Необходимо задать безопасность, так как прокси-сервер **IWbemServices** предоставляет доступ к необработанному объекту.</span><span class="sxs-lookup"><span data-stu-id="66d2b-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="66d2b-106">Как правило, безопасность COM не позволяет одному процессу получить доступ к другому процессу, если не заданы соответствующие свойства безопасности.</span><span class="sxs-lookup"><span data-stu-id="66d2b-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="66d2b-107">Дополнительные сведения см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="66d2b-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="66d2b-108">Для подключений к разным операционным системам требуются разные уровни проверки подлинности и олицетворения.</span><span class="sxs-lookup"><span data-stu-id="66d2b-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="66d2b-109">Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="66d2b-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="66d2b-110">В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.</span><span class="sxs-lookup"><span data-stu-id="66d2b-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="66d2b-111">Следующая процедура описывает, как задать уровни безопасности для WMI-соединения.</span><span class="sxs-lookup"><span data-stu-id="66d2b-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="66d2b-112">**Установка уровней безопасности для WMI-соединения**</span><span class="sxs-lookup"><span data-stu-id="66d2b-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="66d2b-113">Задайте уровни безопасности для прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) с помощью вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="66d2b-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="66d2b-114">В следующем примере кода описывается распространенный способ вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="66d2b-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

<span data-ttu-id="66d2b-115">После установки уровней безопасности для указателя [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) можно получить доступ к различным возможностям инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="66d2b-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="66d2b-116">После завершения работы с инструментарием WMI необходимо завершить работу приложения.</span><span class="sxs-lookup"><span data-stu-id="66d2b-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="66d2b-117">Дополнительные сведения см. [в разделе Очистка и завершение работы приложения WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="66d2b-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
