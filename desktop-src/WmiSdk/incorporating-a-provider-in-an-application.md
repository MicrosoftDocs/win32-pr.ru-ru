---
description: Описывает, как включить поставщик COM WMI в качестве компонента в приложении, а не внутри процесса в WMI. Называемый несвязанным поставщиком, это рекомендуемый тип поставщика COM WMI для создания операционных систем Windows 2000 и более поздних версий.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Включение поставщика в приложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570816"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="91f35-104">Включение поставщика в приложение</span><span class="sxs-lookup"><span data-stu-id="91f35-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="91f35-105">При создании приложения, предназначенного для инструментирования, рекомендуется включить поставщик как компонент в самом приложении.</span><span class="sxs-lookup"><span data-stu-id="91f35-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="91f35-106">Такой подход позволяет инструментарий управления Windows (WMI) (WMI) взаимодействовать с поставщиком услуг напрямую, а не косвенно через API программы.</span><span class="sxs-lookup"><span data-stu-id="91f35-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="91f35-107">Отделение поставщика от WMI также позволяет приложению управлять временем существования поставщика, а не WMI.</span><span class="sxs-lookup"><span data-stu-id="91f35-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="91f35-108">Дополнительные сведения о создании поставщика, выполняемого в процессе WMI, см. в разделе [предоставление данных WMI с помощью записи поставщика](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="91f35-109">Дополнительные сведения о модели размещения и настройках безопасности для поставщика см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="91f35-110">На следующей схеме показана связь между WMI, несвязанным поставщиком и приложением.</span><span class="sxs-lookup"><span data-stu-id="91f35-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![отношение между WMI, несвязанным поставщиком и приложением](images/decoupledprov.png)

<span data-ttu-id="91f35-112">Дополнительные сведения о методах с разъединенными поставщиками см. в разделе [**ивбемдекаупледрегистрар**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) и [**ивбемдекаупледбасицевентпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="91f35-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="91f35-113">Несвязанный поставщик поддерживает экземпляры, методы, поставщики событий и потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="91f35-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="91f35-114">Он не поддерживает поставщики классов и свойств.</span><span class="sxs-lookup"><span data-stu-id="91f35-114">It does not support class and property providers.</span></span> <span data-ttu-id="91f35-115">Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [запись поставщика свойств](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="91f35-116">В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.</span><span class="sxs-lookup"><span data-stu-id="91f35-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="91f35-117">Следующая процедура использует примеры кода C++, чтобы описать, как внедрить в приложение несвязанный поставщик.</span><span class="sxs-lookup"><span data-stu-id="91f35-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="91f35-118">Метод инициализации приложения выполняет следующие действия, чтобы WMI взаимодействовал только с зарегистрированным несвязанным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="91f35-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="91f35-119">**Реализация несвязанного поставщика в приложении C++**</span><span class="sxs-lookup"><span data-stu-id="91f35-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="91f35-120">Инициализируйте библиотеку COM для использования вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="91f35-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="91f35-121">В следующем примере кода показано, как инициализировать библиотеку COM.</span><span class="sxs-lookup"><span data-stu-id="91f35-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="91f35-122">Задайте уровень безопасности процесса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91f35-122">Set the default process security level.</span></span>

    <span data-ttu-id="91f35-123">На этом уровне устанавливается уровень безопасности, необходимый для доступа других процессов к сведениям о клиентском процессе.</span><span class="sxs-lookup"><span data-stu-id="91f35-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="91f35-124">Уровень проверки подлинности должен \_ быть \_ \_ \_ установлен по умолчанию на уровне RPC C AUTHN.</span><span class="sxs-lookup"><span data-stu-id="91f35-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="91f35-125">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="91f35-126">В следующем примере кода показано, как задать уровень безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91f35-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="91f35-127">Регистрация несвязанного регистратора поставщика.</span><span class="sxs-lookup"><span data-stu-id="91f35-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="91f35-128">В следующем примере кода показано, как зарегистрировать несвязанный регистратор поставщика.</span><span class="sxs-lookup"><span data-stu-id="91f35-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="91f35-129">Регистрация несвязанного поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="91f35-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="91f35-130">В следующем примере кода показано, как зарегистрировать несвязанный поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="91f35-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="91f35-131">Выполните [вызовы WMI](making-calls-to-wmi.md) , необходимые для работы поставщика.</span><span class="sxs-lookup"><span data-stu-id="91f35-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="91f35-132">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="91f35-133">Дополнительные сведения о том, что поставщик служб запрашивает данные из скрипта или приложения, см. [в разделе олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="91f35-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="91f35-134">Непосредственно перед завершением работы приложение должно очищаться после самого себя.</span><span class="sxs-lookup"><span data-stu-id="91f35-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="91f35-135">В следующей процедуре описывается, как отменить регистрацию для несвязанного поставщика, чтобы инструментарий WMI не пытался запросить информацию.</span><span class="sxs-lookup"><span data-stu-id="91f35-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="91f35-136">В следующей процедуре описывается, как отменить регистрацию для несвязанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="91f35-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="91f35-137">**Отмена регистрации несвязанного поставщика**</span><span class="sxs-lookup"><span data-stu-id="91f35-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="91f35-138">Отмените регистрацию и освободите регистратор.</span><span class="sxs-lookup"><span data-stu-id="91f35-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="91f35-139">В следующем примере кода показано, как отменить регистрацию и освобождение регистратора.</span><span class="sxs-lookup"><span data-stu-id="91f35-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="91f35-140">Отмените регистрацию и освободите поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="91f35-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="91f35-141">В следующем примере кода показано, как отменить регистрацию и освободить поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="91f35-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="91f35-142">Очистите сервер COM.</span><span class="sxs-lookup"><span data-stu-id="91f35-142">Clean up the COM server.</span></span>

    <span data-ttu-id="91f35-143">В следующем примере кода показано, как отменить инициализацию библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="91f35-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="91f35-144">См. также</span><span class="sxs-lookup"><span data-stu-id="91f35-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f35-145">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="91f35-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="91f35-146">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="91f35-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="91f35-147">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="91f35-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



