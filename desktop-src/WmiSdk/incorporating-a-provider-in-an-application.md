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
# <a name="incorporating-a-provider-in-an-application"></a>Включение поставщика в приложение

При создании приложения, предназначенного для инструментирования, рекомендуется включить поставщик как компонент в самом приложении. Такой подход позволяет инструментарий управления Windows (WMI) (WMI) взаимодействовать с поставщиком услуг напрямую, а не косвенно через API программы. Отделение поставщика от WMI также позволяет приложению управлять временем существования поставщика, а не WMI. Дополнительные сведения о создании поставщика, выполняемого в процессе WMI, см. в разделе [предоставление данных WMI с помощью записи поставщика](supplying-data-to-wmi-by-writing-a-provider.md). Дополнительные сведения о модели размещения и настройках безопасности для поставщика см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

На следующей схеме показана связь между WMI, несвязанным поставщиком и приложением.

![отношение между WMI, несвязанным поставщиком и приложением](images/decoupledprov.png)

Дополнительные сведения о методах с разъединенными поставщиками см. в разделе [**ивбемдекаупледрегистрар**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) и [**ивбемдекаупледбасицевентпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> Несвязанный поставщик поддерживает экземпляры, методы, поставщики событий и потребителей событий. Он не поддерживает поставщики классов и свойств. Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [запись поставщика свойств](writing-a-property-provider.md).

 

В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Следующая процедура использует примеры кода C++, чтобы описать, как внедрить в приложение несвязанный поставщик. Метод инициализации приложения выполняет следующие действия, чтобы WMI взаимодействовал только с зарегистрированным несвязанным поставщиком.

**Реализация несвязанного поставщика в приложении C++**

1.  Инициализируйте библиотеку COM для использования вызывающим потоком.

    В следующем примере кода показано, как инициализировать библиотеку COM.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Задайте уровень безопасности процесса по умолчанию.

    На этом уровне устанавливается уровень безопасности, необходимый для доступа других процессов к сведениям о клиентском процессе. Уровень проверки подлинности должен \_ быть \_ \_ \_ установлен по умолчанию на уровне RPC C AUTHN. Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).

    В следующем примере кода показано, как задать уровень безопасности по умолчанию.

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

    

3.  Регистрация несвязанного регистратора поставщика.

    В следующем примере кода показано, как зарегистрировать несвязанный регистратор поставщика.

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

    

4.  Регистрация несвязанного поставщика событий.

    В следующем примере кода показано, как зарегистрировать несвязанный поставщик событий.

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

    

5.  Выполните [вызовы WMI](making-calls-to-wmi.md) , необходимые для работы поставщика. Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md). Дополнительные сведения о том, что поставщик служб запрашивает данные из скрипта или приложения, см. [в разделе олицетворение клиента](impersonating-a-client.md).

Непосредственно перед завершением работы приложение должно очищаться после самого себя. В следующей процедуре описывается, как отменить регистрацию для несвязанного поставщика, чтобы инструментарий WMI не пытался запросить информацию.

В следующей процедуре описывается, как отменить регистрацию для несвязанного поставщика.

**Отмена регистрации несвязанного поставщика**

1.  Отмените регистрацию и освободите регистратор.

    В следующем примере кода показано, как отменить регистрацию и освобождение регистратора.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Отмените регистрацию и освободите поставщик событий.

    В следующем примере кода показано, как отменить регистрацию и освободить поставщик событий.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Очистите сервер COM.

    В следующем примере кода показано, как отменить инициализацию библиотеки COM.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Защита поставщика](securing-your-provider.md)
</dt> <dt>

[Разработка поставщика WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 



