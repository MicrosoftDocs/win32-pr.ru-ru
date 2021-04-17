---
description: Вы можете использовать процедуру и пример кода в этом разделе для завершения клиентского приложения WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, получает уведомление о событии, а затем очищается.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: Пример. получение уведомлений о событиях через WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6380d306783f8b547d0d93df0275fd36e17e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497913"
---
# <a name="example-receiving-event-notifications-through-wmi"></a><span data-ttu-id="bfea1-103">Пример. получение уведомлений о событиях через WMI</span><span class="sxs-lookup"><span data-stu-id="bfea1-103">Example: Receiving Event Notifications Through WMI</span></span>

<span data-ttu-id="bfea1-104">Вы можете использовать процедуру и пример кода в этом разделе для завершения клиентского приложения WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, получает уведомление о событии, а затем очищается.</span><span class="sxs-lookup"><span data-stu-id="bfea1-104">You can use the procedure and code example in this topic to complete WMI client application that performs COM initialization, connects to WMI on the local computer, receives an event notification, and then cleans up.</span></span> <span data-ttu-id="bfea1-105">Этот пример уведомляет пользователя о событии при создании нового процесса.</span><span class="sxs-lookup"><span data-stu-id="bfea1-105">The example notifies the user of an event when a new process is created.</span></span> <span data-ttu-id="bfea1-106">События получаются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bfea1-106">The events are received asynchronously.</span></span>

<span data-ttu-id="bfea1-107">Для выполнения приложения WMI используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="bfea1-107">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="bfea1-108">Шаги с 1 по 5 содержат все шаги, необходимые для установки и подключения к WMI, а шаг 6 — место получения уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="bfea1-108">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and step 6 is where the event notifications are received.</span></span>

<span data-ttu-id="bfea1-109">**Получение уведомления о событии через WMI**</span><span class="sxs-lookup"><span data-stu-id="bfea1-109">**To receive a event notification through WMI**</span></span>

1.  <span data-ttu-id="bfea1-110">Инициализируйте параметры COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="bfea1-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="bfea1-111">Дополнительные сведения см. [в разделе Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-111">Fore more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="bfea1-112">Инициализируйте безопасность процессов COM путем вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="bfea1-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="bfea1-113">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="bfea1-114">Получите исходный указатель WMI, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="bfea1-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="bfea1-115">Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="bfea1-116">Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для корневого \\ пространства имен CIMV2 на локальном компьютере, вызвав [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="bfea1-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="bfea1-117">Сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="bfea1-118">Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="bfea1-119">Настройте безопасность прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , чтобы служба WMI могла олицетворять клиента, вызвав метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="bfea1-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="bfea1-120">Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="bfea1-121">Используйте указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для выполнения запросов к WMI.</span><span class="sxs-lookup"><span data-stu-id="bfea1-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="bfea1-122">В этом примере используется метод [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) для получения асинхронных событий.</span><span class="sxs-lookup"><span data-stu-id="bfea1-122">This example uses the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method to receive asynchronous events.</span></span> <span data-ttu-id="bfea1-123">При получении асинхронных событий необходимо предоставить реализацию [**ивбемобжектсинк**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-123">When you receive asynchronous events, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="bfea1-124">В этом примере реализуется реализация в классе Евентсинк.</span><span class="sxs-lookup"><span data-stu-id="bfea1-124">This example provides the implementation in the EventSink class.</span></span> <span data-ttu-id="bfea1-125">Код реализации и код файла заголовка для этого класса предоставляются ниже основного примера.</span><span class="sxs-lookup"><span data-stu-id="bfea1-125">The implementation code and header file code for this class are provided below the main example.</span></span> <span data-ttu-id="bfea1-126">Метод **IWbemServices:: ExecNotificationQueryAsync** вызывает метод **Евентсинк:: обозначают** при получении события.</span><span class="sxs-lookup"><span data-stu-id="bfea1-126">The **IWbemServices::ExecNotificationQueryAsync** method calls the **EventSink::Indicate** method whenever an event is received.</span></span> <span data-ttu-id="bfea1-127">В этом примере метод **евентсинк:: обозначают** вызывается при каждом создании процесса.</span><span class="sxs-lookup"><span data-stu-id="bfea1-127">For this example the **EventSink::Indicate** method is called whenever a process is created.</span></span> <span data-ttu-id="bfea1-128">Чтобы протестировать этот пример, запустите код и запустите процесс, например Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="bfea1-128">To test this example, run the code and start a process such as Notepad.exe.</span></span> <span data-ttu-id="bfea1-129">Это активирует уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="bfea1-129">This triggers an event notification.</span></span>

    <span data-ttu-id="bfea1-130">Дополнительные сведения о выполнении запросов WMI см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="bfea1-130">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="bfea1-131">Следующий пример кода получает уведомления о событиях через WMI.</span><span class="sxs-lookup"><span data-stu-id="bfea1-131">The following example code receives event notifications through WMI.</span></span>


```C++
#include "eventsink.h"

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="bfea1-132">Следующий файл заголовка используется для класса Евентсинк.</span><span class="sxs-lookup"><span data-stu-id="bfea1-132">The following header file is used for the class EventSink.</span></span> <span data-ttu-id="bfea1-133">Класс Евентсинк используется в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="bfea1-133">The EventSink class is used in the previous code example.</span></span>


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};

#endif    // end of EventSink.h
```



<span data-ttu-id="bfea1-134">Следующий пример кода является реализацией класса Евентсинк.</span><span class="sxs-lookup"><span data-stu-id="bfea1-134">The following example code is an implementation of the EventSink class.</span></span>


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
