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
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="1835f-103">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="1835f-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="1835f-104">Репозиторий WMI содержит предустановленные классы производительности для всех объектов библиотеки производительности.</span><span class="sxs-lookup"><span data-stu-id="1835f-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="1835f-105">Например, экземпляры класса производительности "необработанные данные" [**Win32 \_ перфравдата \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) представляют процессы.</span><span class="sxs-lookup"><span data-stu-id="1835f-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="1835f-106">Этот объект производительности отображается в системном мониторе как объект процесса.</span><span class="sxs-lookup"><span data-stu-id="1835f-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="1835f-107">Свойство **пажефаултсперсек** [**\_ \_ \_ процесса Win32 Перфравдата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) представляет счетчик производительности "ошибок страниц в секунду" для процесса.</span><span class="sxs-lookup"><span data-stu-id="1835f-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="1835f-108">Классы [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) содержат значения вычисляемых данных, отображаемые в системном мониторе (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="1835f-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="1835f-109">Значение свойства **пажефаултсперсек** [**\_ \_ \_ процесса Win32 перфформаттеддата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) совпадает со значением, которое отображается в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="1835f-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="1835f-110">Для доступа к данным производительности с помощью [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)можно использовать [API COM для WMI](com-api-for-wmi.md) или [API скриптов для инструментария WMI](scripting-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="1835f-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="1835f-111">В обоих случаях для получения каждого образца данных требуется объект [*обновления*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="1835f-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="1835f-112">Дополнительные сведения и примеры кода сценариев для использования обновлений и доступа к классам производительности см. в разделе [задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="1835f-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="1835f-113">Дополнительные сведения см. [в разделе доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="1835f-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="1835f-114">Доступ к данным о производительности из C++</span><span class="sxs-lookup"><span data-stu-id="1835f-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="1835f-115">В следующем примере кода C++ поставщик счетчика производительности используется для доступа к предопределенным высокопроизводительным классам.</span><span class="sxs-lookup"><span data-stu-id="1835f-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="1835f-116">Он создает объект обновления и добавляет объект в обновитель.</span><span class="sxs-lookup"><span data-stu-id="1835f-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="1835f-117">Объект является экземпляром [**\_ \_ \_ процесса Win32 перфравдата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) , который наблюдает за производительностью определенного процесса.</span><span class="sxs-lookup"><span data-stu-id="1835f-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="1835f-118">Код считывает только одно свойство счетчика в объекте Process, свойство **банк данных** .</span><span class="sxs-lookup"><span data-stu-id="1835f-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="1835f-119">Для правильной компиляции кода требуются следующие ссылки и операторы **\# include** .</span><span class="sxs-lookup"><span data-stu-id="1835f-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="1835f-120">В следующей процедуре показано, как получить доступ к данным из высокопроизводительного поставщика в C++.</span><span class="sxs-lookup"><span data-stu-id="1835f-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="1835f-121">**Доступ к данным из высокопроизводительного поставщика в C++**</span><span class="sxs-lookup"><span data-stu-id="1835f-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="1835f-122">Установите соединение с пространством имен WMI и установите безопасность WMI с помощью вызова [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) и [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="1835f-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="1835f-123">Этот шаг является стандартным шагом к созданию клиентского приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="1835f-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="1835f-124">Дополнительные сведения см. [в разделе Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="1835f-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="1835f-125">Создайте объект обновления, используя [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с CLSID \_ вбемрефрешер.</span><span class="sxs-lookup"><span data-stu-id="1835f-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="1835f-126">Запросите интерфейс [**ивбемконфигуререфрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) с помощью метода [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="1835f-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="1835f-127">Запросите интерфейс [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) с помощью метода **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="1835f-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="1835f-128">Интерфейс [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) является основным интерфейсом для объекта [**обновления**](swbemrefreshableitem-refresher.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="1835f-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="1835f-129">В следующем примере кода C++ показано, как получить [**ивбемконфигуререфрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span><span class="sxs-lookup"><span data-stu-id="1835f-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

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

    

3.  <span data-ttu-id="1835f-130">Добавьте объект в обновитель с помощью вызова метода [**ивбемконфигуререфрешер:: аддобжектбипас**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .</span><span class="sxs-lookup"><span data-stu-id="1835f-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="1835f-131">При добавлении объекта в обновитель Инструментарий WMI обновляет объект при каждом вызове метода [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="1835f-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="1835f-132">Добавляемый объект назначает поставщик в квалификаторах его класса.</span><span class="sxs-lookup"><span data-stu-id="1835f-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="1835f-133">В следующем примере кода C++ показано, как вызвать [**аддобжектбипас**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span><span class="sxs-lookup"><span data-stu-id="1835f-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

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

    

4.  <span data-ttu-id="1835f-134">Чтобы настроить более быстрый доступ к объекту, подключитесь к интерфейсу [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) через [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в интерфейсе [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="1835f-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="1835f-135">В следующем примере кода C++ показано, как получить указатель на объект, используя [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) вместо [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span><span class="sxs-lookup"><span data-stu-id="1835f-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="1835f-136">Интерфейс [**ивбемобжектакцесс**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) повышает производительность, так как вы можете получить дескрипторы для конкретных свойств счетчика, и для этого необходимо заблокировать и разблокировать объект в коде, что является операцией, которую [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) выполняет для каждого доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="1835f-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="1835f-137">Получите дескрипторы свойств для проверки с помощью вызовов метода [**ивбемобжектакцесс:: жетпропертихандле**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .</span><span class="sxs-lookup"><span data-stu-id="1835f-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="1835f-138">Дескрипторы свойств одинаковы для всех экземпляров класса, что означает использование дескриптора свойства, полученного из конкретного экземпляра, для всех экземпляров определенного класса.</span><span class="sxs-lookup"><span data-stu-id="1835f-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="1835f-139">Можно также получить маркер из объекта класса, чтобы получить значения свойств из объекта экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1835f-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="1835f-140">В следующем примере кода C++ показано, как получить маркер свойства.</span><span class="sxs-lookup"><span data-stu-id="1835f-140">The following C++ code example shows how to retrieve a property handle.</span></span>

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

    

6.  <span data-ttu-id="1835f-141">Создайте цикл программирования, который выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1835f-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="1835f-142">Обновите объект с помощью вызова [**ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , используя указатель, созданный в предыдущем вызове функции [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="1835f-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="1835f-143">В этом вызове Обновитель инструментария WMI обновляет клиентский объект с помощью данных, предоставляемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1835f-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="1835f-144">Выполните любое действие, необходимое для объекта, например получение имени свойства, типа данных или значения.</span><span class="sxs-lookup"><span data-stu-id="1835f-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="1835f-145">Доступ к свойству можно получить с помощью маркера свойства, полученного ранее.</span><span class="sxs-lookup"><span data-stu-id="1835f-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="1835f-146">Из-за вызова [**обновления**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) WMI обновляет свойство каждый раз через цикл.</span><span class="sxs-lookup"><span data-stu-id="1835f-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="1835f-147">В следующем примере C++ показано, как использовать API высокой производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="1835f-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1835f-148">См. также</span><span class="sxs-lookup"><span data-stu-id="1835f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1835f-149">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="1835f-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="1835f-150">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="1835f-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
