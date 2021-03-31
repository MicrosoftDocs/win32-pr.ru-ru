---
description: После установки уровней безопасности для указателя IWbemServices можно получить доступ к различным возможностям инструментария WMI. После завершения работы с инструментарием WMI необходимо завершить работу приложения.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Очистка и завершение работы приложения WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998983"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="f767f-104">Очистка и завершение работы приложения WMI</span><span class="sxs-lookup"><span data-stu-id="f767f-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="f767f-105">После установки уровней безопасности для указателя [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) можно получить доступ к различным возможностям инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="f767f-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="f767f-106">После завершения работы с инструментарием WMI необходимо завершить работу приложения.</span><span class="sxs-lookup"><span data-stu-id="f767f-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="f767f-107">Ниже описана процедура очистки и завершения работы приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="f767f-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="f767f-108">**Очистка и завершение работы приложения WMI**</span><span class="sxs-lookup"><span data-stu-id="f767f-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="f767f-109">Освободите все открытые COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f767f-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="f767f-110">Необходимо помнить два основных интерфейса: [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) и [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="f767f-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="f767f-111">Вызов [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="f767f-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="f767f-112">Как и для всех приложений COM, необходимо вызвать [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) в конце приложения.</span><span class="sxs-lookup"><span data-stu-id="f767f-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="f767f-113">Выйдите из приложения.</span><span class="sxs-lookup"><span data-stu-id="f767f-113">Exit your application.</span></span>

    <span data-ttu-id="f767f-114">В следующем примере кода показано, как выйти из клиентского приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="f767f-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="f767f-115">`pSvc`Переменная имеет тип [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , а переменная Плок имеет тип [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="f767f-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="f767f-116">Инициализация COM, доступ к инструментарию WMI и выход из приложения успешно завершены.</span><span class="sxs-lookup"><span data-stu-id="f767f-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="f767f-117">Дополнительные сведения см. в разделе [пример. Создание приложения WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="f767f-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f767f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f767f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f767f-119">Создание приложения WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="f767f-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
