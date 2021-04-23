---
description: 'После установки стандартных вызовов COM необходимо подключиться к WMI с помощью вызова метода Ивбемлокатор:: Коннектсервер.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Создание соединения с пространством имен WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498060"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="20769-103">Создание соединения с пространством имен WMI</span><span class="sxs-lookup"><span data-stu-id="20769-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="20769-104">После установки стандартных вызовов COM необходимо подключиться к WMI с помощью вызова метода [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="20769-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="20769-105">Метод **коннектсервер** возвращает прокси-сервер интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="20769-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="20769-106">С помощью **IWbemServices** можно получить доступ к различным возможностям инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="20769-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="20769-107">В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.</span><span class="sxs-lookup"><span data-stu-id="20769-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="20769-108">В следующей процедуре описывается создание соединения с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="20769-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="20769-109">**Создание соединения с пространством имен WMI**</span><span class="sxs-lookup"><span data-stu-id="20769-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="20769-110">Инициализируйте интерфейс [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) с помощью вызова [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="20769-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="20769-111">Инструментарий WMI не требует выполнения каких либо дополнительных процедур при вызове [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="20769-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="20769-112">В следующем примере кода показано, как инициализировать [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="20769-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   <span data-ttu-id="20769-113">Подключитесь к инструментарию WMI с помощью вызова метода [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="20769-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="20769-114">Метод [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) возвращает прокси-сервер для интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , который использует для доступа к локальному или удаленному пространству имен WMI, указанному в вызове **коннектсервер**.</span><span class="sxs-lookup"><span data-stu-id="20769-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="20769-115">В следующем примере кода показано, как вызвать [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="20769-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

<span data-ttu-id="20769-116">После получения указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) необходимо установить безопасность на прокси-сервере для доступа к WMI.</span><span class="sxs-lookup"><span data-stu-id="20769-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="20769-117">Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="20769-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20769-118">См. также</span><span class="sxs-lookup"><span data-stu-id="20769-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20769-119">Создание приложения WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="20769-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="20769-120">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="20769-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
