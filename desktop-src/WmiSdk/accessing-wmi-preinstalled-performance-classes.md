---
description: Репозиторий WMI содержит предустановленные классы производительности для всех объектов библиотеки производительности.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Доступ к предустановленным классам производительности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693158"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Доступ к предустановленным классам производительности WMI

Репозиторий WMI содержит предустановленные классы производительности для всех объектов библиотеки производительности. Например, экземпляры класса производительности "необработанные данные" [**Win32 \_ перфравдата \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) представляют процессы. Этот объект производительности отображается в системном мониторе как объект процесса.

Свойство **пажефаултсперсек** [**\_ \_ \_ процесса Win32 Перфравдата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) представляет счетчик производительности "ошибок страниц в секунду" для процесса. Классы [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) содержат значения вычисляемых данных, отображаемые в системном мониторе (Perfmon.exe). Значение свойства **пажефаултсперсек** [**\_ \_ \_ процесса Win32 перфформаттеддата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) совпадает со значением, которое отображается в системном мониторе.

Для доступа к данным производительности с помощью [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)можно использовать [API COM для WMI](com-api-for-wmi.md) или [API скриптов для инструментария WMI](scripting-api-for-wmi.md) . В обоих случаях для получения каждого образца данных требуется объект [*обновления*](gloss-r.md) . Дополнительные сведения и примеры кода сценариев для использования обновлений и доступа к классам производительности см. в разделе [задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md). Дополнительные сведения см. [в разделе доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Доступ к данным о производительности из C++

В следующем примере кода C++ поставщик счетчика производительности используется для доступа к предопределенным высокопроизводительным классам. Он создает объект обновления и добавляет объект в обновитель. Объект является экземпляром [**\_ \_ \_ процесса Win32 перфравдата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) , который наблюдает за производительностью определенного процесса. Код считывает только одно свойство счетчика в объекте Process, свойство **банк данных** . Для правильной компиляции кода требуются следующие ссылки и операторы **\# include** .


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



В следующей процедуре показано, как получить доступ к данным из высокопроизводительного поставщика в C++.

**Доступ к данным из высокопроизводительного поставщика в C++**

1.  Установите соединение с пространством имен WMI и установите безопасность WMI с помощью вызова [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) и [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Этот шаг является стандартным шагом к созданию клиентского приложения WMI. Дополнительные сведения см. [в разделе Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md).

2.  Создайте объект обновления, используя [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с CLSID \_ вбемрефрешер. Запросите интерфейс [**ивбемконфигуререфрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) с помощью метода [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . Запросите интерфейс [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) с помощью метода **QueryInterface** .

    Интерфейс [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) является основным интерфейсом для объекта [**обновления**](swbemrefreshableitem-refresher.md) WMI.

    В следующем примере кода C++ показано, как получить [**ивбемконфигуререфрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Добавьте объект в обновитель с помощью вызова метода [**ивбемконфигуререфрешер:: аддобжектбипас**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .

    При добавлении объекта в обновитель Инструментарий WMI обновляет объект при каждом вызове метода [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . Добавляемый объект назначает поставщик в квалификаторах его класса.

    В следующем примере кода C++ показано, как вызвать [**аддобжектбипас**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Чтобы настроить более быстрый доступ к объекту, подключитесь к интерфейсу [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) через [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в интерфейсе [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .

    В следующем примере кода C++ показано, как получить указатель на объект, используя [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) вместо [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    Интерфейс [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) повышает производительность, так как вы можете получить дескрипторы для конкретных свойств счетчика, и для этого необходимо заблокировать и разблокировать объект в коде, что является операцией, которую [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) выполняет для каждого доступа к свойству.

5.  Получите дескрипторы свойств для проверки с помощью вызовов метода [**ивбемобжектакцесс:: жетпропертихандле**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .

    Дескрипторы свойств одинаковы для всех экземпляров класса, что означает использование дескриптора свойства, полученного из конкретного экземпляра, для всех экземпляров определенного класса. Можно также получить маркер из объекта класса, чтобы получить значения свойств из объекта экземпляра.

    В следующем примере кода C++ показано, как получить маркер свойства.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Создайте цикл программирования, который выполняет следующие действия:

    -   Обновите объект с помощью вызова [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , используя указатель, созданный в предыдущем вызове функции [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

        В этом вызове Обновитель инструментария WMI обновляет клиентский объект с помощью данных, предоставляемых поставщиком.

    -   Выполните любое действие, необходимое для объекта, например получение имени свойства, типа данных или значения.

        Доступ к свойству можно получить с помощью маркера свойства, полученного ранее. Из-за вызова [**обновления**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) WMI обновляет свойство каждый раз через цикл.

В следующем примере C++ показано, как использовать API высокой производительности WMI.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
