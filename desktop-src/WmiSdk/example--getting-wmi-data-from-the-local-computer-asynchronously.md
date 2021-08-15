---
description: Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, получает данные асинхронно, а затем очищает.
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: Пример. асинхронное получение данных WMI с локального компьютера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67eb71247816319553389c451dd2e7ad268c49ee7aadeaddc118a3f08448171b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319432"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a>Пример. асинхронное получение данных WMI с локального компьютера

Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, получает данные асинхронно, а затем очищает. Этот пример возвращает имя операционной системы на локальном компьютере и отображает ее.

Для выполнения приложения WMI используется следующая процедура. Шаги с 1 по 5 содержат все шаги, необходимые для установки и подключения к WMI, а шаги 6 и семь — место, где имя операционной системы извлекается асинхронно.

**Асинхронное получение данных WMI с локального компьютера**

1.  Инициализируйте параметры COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

2.  Инициализируйте безопасность процессов COM путем вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).

3.  Получите исходный указатель WMI, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для корневого \\ пространства имен CIMV2 на локальном компьютере, вызвав [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Дополнительные сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md).

    Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  Настройте безопасность прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , чтобы служба WMI могла олицетворять клиента, вызвав метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).

6.  Используйте указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для выполнения запросов к WMI. В этом примере используется метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) для асинхронного получения данных. При асинхронном получении данных необходимо предоставить реализацию [**ивбемобжектсинк**](iwbemobjectsink.md). В этом примере реализуется реализация в классе Куерисинк. Код реализации и файл заголовка для этого класса предоставляются после основного примера. Метод **IWbemServices:: ексеккуерясинк** вызывает метод куерисинк:: обозначают при получении данных.

    Дополнительные сведения о создании WMI-запроса см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [вызов метода](calling-a-method.md).

7.  Дождитесь асинхронного получения данных. Чтобы вручную отключить асинхронный вызов, используйте метод [**IWbemServices:: канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

Следующий пример кода возвращает данные WMI с локального компьютера в асинхронном режиме.


```C++
#include "querysink.h"


int main(int argc, char **argv)
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

    hres =  CoInitializeSecurity(NULL, 
                                 -1,                          // COM authentication
                                 NULL,                        // Authentication services
                                 NULL,                        // Reserved
                                 RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
                                 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
                                 NULL,                        // Authentication info
                                 EOAC_NONE,                   // Additional capabilities 
                                 NULL);                       // Reserved

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
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
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(_bstr_t(L"ROOT\\CIMV2"), 
                               NULL,
                               NULL,
                               0,
                               NULL,
                               0,
                               0, 
                               &pSvc);
    
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

    hres = CoSetProxyBlanket(pSvc,                        // Indicates the proxy to set
                             RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
                             RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
                             NULL,                        // Server principal name 
                             RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
                             RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
                             NULL,                        // client identity
                             EOAC_NONE);                  // proxy capabilities 

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system.
    // The IWbemService::ExecQueryAsync method will call
    // the QuerySink::Indicate method when it receives a result
    // and the QuerySink::Indicate method will display the OS name
    QuerySink* pResponseSink = new QuerySink();
    pResponseSink->AddRef();
    hres = pSvc->ExecQueryAsync(bstr_t("WQL"), 
                                bstr_t("SELECT * FROM Win32_OperatingSystem"),
                                WBEM_FLAG_BIDIRECTIONAL, 
                                NULL,
                                pResponseSink);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        pResponseSink->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Wait to get the data from the query in step 6 -----------
    Sleep(500);
    pSvc->CancelAsyncCall(pResponseSink);

    // Cleanup
    // ========
    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



Следующий файл заголовка используется для класса Куерисинк. Класс Куерисинк используется в предыдущем примере кода.


```C++
// QuerySink.h
#ifndef QUERYSINK_H
#define QUERYSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;
 CRITICAL_SECTION threadLock; // for thread safety

public:
    QuerySink() { m_lRef = 0; bDone = false; 
     InitializeCriticalSection(&threadLock); }
    ~QuerySink() { bDone = true;
        DeleteCriticalSection(&threadLock); }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid,
        void** ppv);

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

 bool IsDone();
};

#endif    // end of QuerySink.h
```



Следующий пример кода является реализацией класса Куерисинк.


```C++
// QuerySink.cpp
#include "querysink.h"

ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        VARIANT varName;
        hres = apObjArray[i]->Get(_bstr_t(L"Name"),
            0, &varName, 0, 0);

        if (FAILED(hres))
        {
            cout << "Failed to get the data from the query"
                << " Error code = 0x"
                << hex << hres << endl;
            return WBEM_E_FAILED;       // Program has failed.
        }

        printf("Name: %ls\n", V_BSTR(&varName));
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
 if(lFlags == WBEM_STATUS_COMPLETE)
 {
  printf("Call complete.\n");

  EnterCriticalSection(&threadLock);
  bDone = true;
  LeaveCriticalSection(&threadLock);
 }
 else if(lFlags == WBEM_STATUS_PROGRESS)
 {
  printf("Call in progress.\n");
 }
    
    return WBEM_S_NO_ERROR;
}


bool QuerySink::IsDone()
{
    bool done = true;

 EnterCriticalSection(&threadLock);
 done = bDone;
 LeaveCriticalSection(&threadLock);

    return done;
}    // end of QuerySink.cpp
```



 

 
