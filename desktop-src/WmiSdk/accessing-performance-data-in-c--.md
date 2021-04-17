---
description: API высокой производительности WMI — это серия интерфейсов, которые получают данные из классов счетчиков производительности.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Доступ к данным о производительности в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693753"
---
# <a name="accessing-performance-data-in-c"></a>Доступ к данным о производительности в C++

API высокой производительности WMI — это серия интерфейсов, которые получают данные из [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes). Эти интерфейсы нуждаются в использовании объекта [*обновления*](gloss-r.md) для увеличения частоты выборки. Дополнительные сведения об использовании объекта Обновитель в сценариях см. [в разделе доступ к данным о производительности в скриптах](accessing-performance-data-in-script.md) и [задачах WMI: наблюдение за производительностью](wmi-tasks--performance-monitoring.md).

В этом разделе обсуждаются следующие разделы:

-   [Обновление данных о производительности](#refreshing-performance-data)
-   [Добавление перечислителей в обновитель WMI](#adding-enumerators-to-the-wmi-refresher)
-   [Пример](#example)
-   [См. также](#related-topics)

## <a name="refreshing-performance-data"></a>Обновление данных о производительности

Объект обновления увеличивает производительность поставщика данных и клиента за счет извлечения данных без пересечения границ процесса. Если клиент и сервер расположены на одном компьютере, то Обновитель загружает высокопроизводительный поставщик в процесс клиента и копирует данные непосредственно из объектов поставщика в клиентские объекты. Если клиент и сервер расположены на разных компьютерах, то Обновитель повышает производительность за счет кэширования объектов на удаленном компьютере и передачи клиенту минимальных наборов данных.

Кроме того, Обновитель:

-   Автоматически повторно подключает клиента к удаленной службе WMI при возникновении ошибки сети или при перезапуске удаленного компьютера.

    По умолчанию при сбое удаленного подключения между двумя компьютерами Обновитель пытается повторно подключить приложение к соответствующему высокопроизводительному поставщику. Чтобы предотвратить повторное подключение, передайте флаг WBEM в вызове метода [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) **\_ \_ обновить \_ без \_ автоматического \_ повторного подключения** . Клиенты скриптов должны присвоить свойству [**свбемрефрешер. Аутореконнект**](swbemrefresher-autoreconnect.md) **значение false**.

-   Загружает несколько объектов и перечислителей, предоставляемых одним или несколькими поставщиками.

    Позволяет добавлять в обновитель несколько объектов, перечислителей или и то, и другое.

-   Перечисляет объекты.

    Как и другие поставщики, высокопроизводительный поставщик может перечислить объекты.

После завершения создания высокопроизводительного клиента может потребоваться увеличить время отклика. Поскольку интерфейс [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) оптимизирован для ускорения, интерфейс не является внутренним среадсафе. Поэтому во время операции обновления не следует обращаться к обновляемому объекту или перечислению. Чтобы защитить объекты в потоках во время вызовов метода **ивбемобжектакцесс** , используйте методы [**Ивбемобжектакцесс:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) и [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) . Для повышения производительности синхронизируйте потоки, чтобы не нужно было блокировать отдельные потоки. Сокращение числа потоков и Синхронизация групп объектов для операций обновления обеспечивает максимальную общую производительность.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Добавление перечислителей в обновитель WMI

Количество экземпляров и данных в каждом экземпляре обновляется путем добавления перечислителя в обновитель, чтобы каждый вызов [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) получил полное перечисление.

В следующем примере кода C++ для правильной компиляции требуются следующие ссылки и \# операторы include.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



В следующей процедуре показано, как добавить перечислитель в обновитель.

**Добавление перечислителя в обновитель**

1.  Вызовите метод [**ивбемконфигуререфрешер:: адденум**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) , используя путь к обновляемому объекту и интерфейсу [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

    Обновитель возвращает указатель на интерфейс [**ивбемхиперфенум**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) . Для доступа к объектам в перечислении можно использовать интерфейс **ивбемхиперфенум** .

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Создайте цикл, который выполняет следующие действия:

    -   Обновляет объект с помощью вызова [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Предоставляет массив указателей интерфейса [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) для метода [**Ивбемхиперфенум:: GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .
    -   Обращается к свойствам перечислителя с помощью методов [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) , переданных в [**GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

        Для получения обновленного значения можно передать маркер свойства в каждый экземпляр [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) . Клиент должен вызвать метод [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить указатели **ивбемобжектакцесс** , возвращаемые [**GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

## <a name="example"></a>Пример

В следующем примере кода C++ перечисляются высокопроизводительные классы, где клиент получает маркер свойства из первого объекта и повторно использует этот маркер для оставшейся части операции обновления. Каждый вызов метода [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) обновляет количество экземпляров и данных экземпляра.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md)
</dt> <dt>

[Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> <dt>

[Квалификаторы свойств для отформатированных классов счетчиков производительности](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Типы счетчиков производительности WMI](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
