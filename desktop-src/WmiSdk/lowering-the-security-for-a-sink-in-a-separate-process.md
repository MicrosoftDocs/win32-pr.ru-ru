---
description: Инструментарий управления Windows (WMI) (WMI) может создать приемник для получения асинхронных обратных вызовов для клиентского приложения в отдельном процессе.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Понижение безопасности приемника в отдельном процессе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693272"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="bad0a-103">Понижение безопасности приемника в отдельном процессе</span><span class="sxs-lookup"><span data-stu-id="bad0a-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="bad0a-104">Инструментарий управления Windows (WMI) (WMI) может создать приемник для получения асинхронных обратных вызовов для клиентского приложения в отдельном процессе.</span><span class="sxs-lookup"><span data-stu-id="bad0a-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="bad0a-105">Отдельный процесс Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="bad0a-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="bad0a-106">Используйте интерфейс [**ивбемунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="bad0a-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="bad0a-107">**Ивбемунсекуредапартмент** позволяет управлять проверкой подлинности обратных вызовов в приемнике Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="bad0a-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="bad0a-108">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="bad0a-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="bad0a-109">Затем можно снизить безопасность этого процесса, и WMI сможет получить доступ к приемнику без ограничений.</span><span class="sxs-lookup"><span data-stu-id="bad0a-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="bad0a-110">Для помощи с этим методом Инструментарий WMI предоставляет Unsecapp.exe процесс для работы в качестве отдельного процесса.</span><span class="sxs-lookup"><span data-stu-id="bad0a-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="bad0a-111">Unsecapp.exe можно разместить с помощью вызова интерфейса [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="bad0a-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="bad0a-112">Интерфейс [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) позволяет клиентскому приложению создавать отдельный выделенный процесс, выполняющий Unsecapp.exe для размещения реализации [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bad0a-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="bad0a-113">Выделенный процесс может вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы предоставить WMI доступ к выделенному процессу, не нарушая безопасность основного процесса.</span><span class="sxs-lookup"><span data-stu-id="bad0a-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="bad0a-114">После инициализации выделенный процесс выступает в качестве посредника между основным процессом и WMI.</span><span class="sxs-lookup"><span data-stu-id="bad0a-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="bad0a-115">В следующей процедуре описывается выполнение асинхронного вызова с помощью [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="bad0a-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="bad0a-116">**Выполнение асинхронного вызова с помощью Иунсекуредапартмент**</span><span class="sxs-lookup"><span data-stu-id="bad0a-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="bad0a-117">Создайте выделенный процесс с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="bad0a-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="bad0a-118">В следующем примере кода метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) вызывается для создания выделенного процесса.</span><span class="sxs-lookup"><span data-stu-id="bad0a-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="bad0a-119">Создайте экземпляр объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="bad0a-120">В следующем примере кода создается новый объект приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="bad0a-121">Создайте заглушку для приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="bad0a-122">Заглушка — это функция-оболочка, созданная из приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="bad0a-123">В следующем примере кода вызывается [**креатеобжектстуб**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) , чтобы создать заглушку для приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="bad0a-124">Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для оболочки и запросите указатель на интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bad0a-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="bad0a-125">В следующем примере кода метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) вызывается и запрашивается указатель на интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="bad0a-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="bad0a-126">Освободите указатель объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="bad0a-127">Можно освободить указатель на объект, так как заглушка теперь является владельцем указателя.</span><span class="sxs-lookup"><span data-stu-id="bad0a-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="bad0a-128">В следующем примере кода освобождается указатель объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="bad0a-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="bad0a-129">Используйте заглушку при любом асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="bad0a-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="bad0a-130">По завершении работы с вызовом Освободите локальный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="bad0a-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="bad0a-131">В следующем примере кода заглушка используется в асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="bad0a-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="bad0a-132">Иногда может потребоваться отменить асинхронный вызов после выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="bad0a-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="bad0a-133">Если необходимо отменить вызов, отмените вызов с тем же указателем, который был изначально выполнил вызов.</span><span class="sxs-lookup"><span data-stu-id="bad0a-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="bad0a-134">В следующем примере кода показано, как отменить асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="bad0a-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="bad0a-135">При завершении использования асинхронного вызова Освободите локальный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="bad0a-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="bad0a-136">Не забудьте освободить указатель *пстубсинк* только после того, как вы подтвердите, что асинхронный вызов не нужно отменять.</span><span class="sxs-lookup"><span data-stu-id="bad0a-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="bad0a-137">Кроме того, не освобождайте *пстубсинк* после того, как инструментарий WMI освобождает указатель приемника *псинк* .</span><span class="sxs-lookup"><span data-stu-id="bad0a-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="bad0a-138">При освобождении *пстубсинк* после *псинк* создается циклическая ссылка, в которой приемник и заглушка постоянно остаются в памяти.</span><span class="sxs-lookup"><span data-stu-id="bad0a-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="bad0a-139">Вместо этого можно освободить указатель в вызове [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , СДЕЛАНном WMI, чтобы сообщить о завершении исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="bad0a-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="bad0a-140">После завершения выполните деинициализацию COM с помощью вызова метода [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="bad0a-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="bad0a-141">В следующем примере кода показано, как вызвать метод [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя *пунсекапп* .</span><span class="sxs-lookup"><span data-stu-id="bad0a-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="bad0a-142">В примерах кода в этом разделе \# для правильной компиляции требуется следующая инструкция Reference и include.</span><span class="sxs-lookup"><span data-stu-id="bad0a-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="bad0a-143">Дополнительные сведения о функции и параметрах [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) см. в документации по [com](../cossdk/component-services-portal.md) в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="bad0a-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
