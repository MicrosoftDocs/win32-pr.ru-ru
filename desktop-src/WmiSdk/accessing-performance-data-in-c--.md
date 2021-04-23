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
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="6f73d-103">Доступ к данным о производительности в C++</span><span class="sxs-lookup"><span data-stu-id="6f73d-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="6f73d-104">API высокой производительности WMI — это серия интерфейсов, которые получают данные из [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="6f73d-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="6f73d-105">Эти интерфейсы нуждаются в использовании объекта [*обновления*](gloss-r.md) для увеличения частоты выборки.</span><span class="sxs-lookup"><span data-stu-id="6f73d-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="6f73d-106">Дополнительные сведения об использовании объекта Обновитель в сценариях см. [в разделе доступ к данным о производительности в скриптах](accessing-performance-data-in-script.md) и [задачах WMI: наблюдение за производительностью](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="6f73d-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="6f73d-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="6f73d-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6f73d-108">Обновление данных о производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="6f73d-109">Добавление перечислителей в обновитель WMI</span><span class="sxs-lookup"><span data-stu-id="6f73d-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="6f73d-110">Пример</span><span class="sxs-lookup"><span data-stu-id="6f73d-110">Example</span></span>](#example)
-   [<span data-ttu-id="6f73d-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6f73d-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="6f73d-112">Обновление данных о производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-112">Refreshing Performance Data</span></span>

<span data-ttu-id="6f73d-113">Объект обновления увеличивает производительность поставщика данных и клиента за счет извлечения данных без пересечения границ процесса.</span><span class="sxs-lookup"><span data-stu-id="6f73d-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="6f73d-114">Если клиент и сервер расположены на одном компьютере, то Обновитель загружает высокопроизводительный поставщик в процесс клиента и копирует данные непосредственно из объектов поставщика в клиентские объекты.</span><span class="sxs-lookup"><span data-stu-id="6f73d-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="6f73d-115">Если клиент и сервер расположены на разных компьютерах, то Обновитель повышает производительность за счет кэширования объектов на удаленном компьютере и передачи клиенту минимальных наборов данных.</span><span class="sxs-lookup"><span data-stu-id="6f73d-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="6f73d-116">Кроме того, Обновитель:</span><span class="sxs-lookup"><span data-stu-id="6f73d-116">A refresher also:</span></span>

-   <span data-ttu-id="6f73d-117">Автоматически повторно подключает клиента к удаленной службе WMI при возникновении ошибки сети или при перезапуске удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6f73d-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="6f73d-118">По умолчанию при сбое удаленного подключения между двумя компьютерами Обновитель пытается повторно подключить приложение к соответствующему высокопроизводительному поставщику.</span><span class="sxs-lookup"><span data-stu-id="6f73d-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="6f73d-119">Чтобы предотвратить повторное подключение, передайте флаг WBEM в вызове метода [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) **\_ \_ обновить \_ без \_ автоматического \_ повторного подключения** .</span><span class="sxs-lookup"><span data-stu-id="6f73d-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="6f73d-120">Клиенты скриптов должны присвоить свойству [**свбемрефрешер. Аутореконнект**](swbemrefresher-autoreconnect.md) **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6f73d-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="6f73d-121">Загружает несколько объектов и перечислителей, предоставляемых одним или несколькими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="6f73d-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="6f73d-122">Позволяет добавлять в обновитель несколько объектов, перечислителей или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="6f73d-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="6f73d-123">Перечисляет объекты.</span><span class="sxs-lookup"><span data-stu-id="6f73d-123">Enumerates objects.</span></span>

    <span data-ttu-id="6f73d-124">Как и другие поставщики, высокопроизводительный поставщик может перечислить объекты.</span><span class="sxs-lookup"><span data-stu-id="6f73d-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="6f73d-125">После завершения создания высокопроизводительного клиента может потребоваться увеличить время отклика.</span><span class="sxs-lookup"><span data-stu-id="6f73d-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="6f73d-126">Поскольку интерфейс [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) оптимизирован для ускорения, интерфейс не является внутренним среадсафе.</span><span class="sxs-lookup"><span data-stu-id="6f73d-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="6f73d-127">Поэтому во время операции обновления не следует обращаться к обновляемому объекту или перечислению.</span><span class="sxs-lookup"><span data-stu-id="6f73d-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="6f73d-128">Чтобы защитить объекты в потоках во время вызовов метода **ивбемобжектакцесс** , используйте методы [**Ивбемобжектакцесс:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) и [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="6f73d-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="6f73d-129">Для повышения производительности синхронизируйте потоки, чтобы не нужно было блокировать отдельные потоки.</span><span class="sxs-lookup"><span data-stu-id="6f73d-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="6f73d-130">Сокращение числа потоков и Синхронизация групп объектов для операций обновления обеспечивает максимальную общую производительность.</span><span class="sxs-lookup"><span data-stu-id="6f73d-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="6f73d-131">Добавление перечислителей в обновитель WMI</span><span class="sxs-lookup"><span data-stu-id="6f73d-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="6f73d-132">Количество экземпляров и данных в каждом экземпляре обновляется путем добавления перечислителя в обновитель, чтобы каждый вызов [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) получил полное перечисление.</span><span class="sxs-lookup"><span data-stu-id="6f73d-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="6f73d-133">В следующем примере кода C++ для правильной компиляции требуются следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="6f73d-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="6f73d-134">В следующей процедуре показано, как добавить перечислитель в обновитель.</span><span class="sxs-lookup"><span data-stu-id="6f73d-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="6f73d-135">**Добавление перечислителя в обновитель**</span><span class="sxs-lookup"><span data-stu-id="6f73d-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="6f73d-136">Вызовите метод [**ивбемконфигуререфрешер:: адденум**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) , используя путь к обновляемому объекту и интерфейсу [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="6f73d-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="6f73d-137">Обновитель возвращает указатель на интерфейс [**ивбемхиперфенум**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) .</span><span class="sxs-lookup"><span data-stu-id="6f73d-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="6f73d-138">Для доступа к объектам в перечислении можно использовать интерфейс **ивбемхиперфенум** .</span><span class="sxs-lookup"><span data-stu-id="6f73d-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

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

    

2.  <span data-ttu-id="6f73d-139">Создайте цикл, который выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6f73d-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="6f73d-140">Обновляет объект с помощью вызова [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="6f73d-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="6f73d-141">Предоставляет массив указателей интерфейса [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) для метода [**Ивбемхиперфенум:: GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .</span><span class="sxs-lookup"><span data-stu-id="6f73d-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="6f73d-142">Обращается к свойствам перечислителя с помощью методов [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) , переданных в [**GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="6f73d-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="6f73d-143">Для получения обновленного значения можно передать маркер свойства в каждый экземпляр [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) .</span><span class="sxs-lookup"><span data-stu-id="6f73d-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="6f73d-144">Клиент должен вызвать метод [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить указатели **ивбемобжектакцесс** , возвращаемые [**GetObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="6f73d-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="6f73d-145">Пример</span><span class="sxs-lookup"><span data-stu-id="6f73d-145">Example</span></span>

<span data-ttu-id="6f73d-146">В следующем примере кода C++ перечисляются высокопроизводительные классы, где клиент получает маркер свойства из первого объекта и повторно использует этот маркер для оставшейся части операции обновления.</span><span class="sxs-lookup"><span data-stu-id="6f73d-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="6f73d-147">Каждый вызов метода [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) обновляет количество экземпляров и данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6f73d-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6f73d-148">См. также</span><span class="sxs-lookup"><span data-stu-id="6f73d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f73d-149">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="6f73d-150">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="6f73d-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="6f73d-151">Обновление данных WMI в скриптах</span><span class="sxs-lookup"><span data-stu-id="6f73d-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="6f73d-152">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="6f73d-153">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="6f73d-154">Квалификаторы свойств для отформатированных классов счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="6f73d-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="6f73d-155">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="6f73d-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="6f73d-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="6f73d-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="6f73d-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="6f73d-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
