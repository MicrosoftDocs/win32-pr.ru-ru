---
description: Получение поддерживаемых методов службы
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Получение поддерживаемых методов службы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911120"
---
# <a name="retrieving-supported-service-methods"></a>Получение поддерживаемых методов службы

Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой. Они относятся к каждому типу служб и представляются уникальными идентификаторами GUID.

Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации.

Приложения могут программно запрашивать Поддерживаемые методы и получать доступ к этим методам и их атрибутам с помощью интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .

Методы службы не следует путать с командами WPD. Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером. Команды являются предопределенными, сгруппированные по категориям, например \_ категории WPD \_ Common, и представляются структурой PROPERTYKEY. Дополнительные сведения см. в разделе [**команды**](commands.md) .

Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может извлекать методы, поддерживаемые данной службой контактов, с помощью интерфейсов, приведенных в следующей таблице.



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Интерфейс                                                                            | Описание                                                                                                    |
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Используется для получения интерфейса **ипортабледевицесервицекапабилитиес** для доступа к поддерживаемым методам службы. |
| [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Предоставляет доступ к поддерживаемым методам, атрибутам методов и параметрам методов.                             |
| [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Содержит список поддерживаемых методов.                                                                        |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                               | Содержит атрибуты для метода и для параметров данного метода.                                      |
| [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)                 | Содержит параметры для данного метода.                                                                    |



 

Когда пользователь выбирает параметр "5" в командной строке, приложение вызывает метод **листсуппортедмесодс** , который находится в модуле сервицемесодс. cpp.

Обратите внимание, что перед получением списка событий пример приложения открывает службу контактов на подключенном устройстве.

В WPD метод описывается его именем, правами доступа, параметрами и связанными данными. Пример приложения отображает понятное имя, например "Кустоммесод", или GUID. За именем метода или идентификатором GUID следует доступ к данным ("чтение и запись"), имя любого связанного формата и данные параметра. Эти данные включают имя параметра, использование, VARTYPE и форму.

Пять методов в модуле Сервицемесодс. cpp поддерживают извлечение методов (и связанных данных) для заданной службы Contacts: **листсуппортедмесодс**, **дисплаймесод**, **дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс**. Метод **листсуппортедмесодс** извлекает количество поддерживаемых методов и идентификатор GUID для каждого; Затем он вызывает метод **дисплаймесод** . Метод **дисплаймесод** вызывает метод [**Ипортабледевицесервицекапапбилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) для получения параметров данного метода, параметров и т. д. После того как **дисплаймесод** извлекает данные метода, он отображает имя (или GUID), ограничения доступа, связанный формат (если он есть) и описания параметров. **Дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс** — это вспомогательные функции, которые отображают соответствующие поля данных.

Метод **листсуппортедмесодс** вызывает метод [**Ипортабледевицесервице:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Используя этот интерфейс, он получает Поддерживаемые методы, вызывая метод [**ипортабледевицесервицекапабилитиес:: жетсуппортедмесодс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . Метод **жетсуппортедмесодс** извлекает идентификаторы GUID для каждого метода, поддерживаемого службой, и копирует этот идентификатор GUID в объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .

В следующем коде используется метод **листсуппортедмесодс** .


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



После того как метод **листсуппортедмесодс** извлекает идентификатор GUID для каждого события, поддерживаемого данной службой, он вызывает метод **дисплаймесод** для получения атрибутов, зависящих от метода. К этим атрибутам относятся: понятное для скрипта имя, необходимые ограничения доступа, любой связанный формат и список параметров.

Метод **дисплаймесод** вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) для получения коллекции атрибутов для данного метода. Затем он вызывает метод [**ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md) для получения имени метода. **Дисплаймесод** вызывает [**Ипортабледевицевалуес:: жетунсигнединтежервалуе**](iportabledevicevalues-getunsignedintegervalue.md) для получения доступа рестрктионс. После этого он вызывает [**ипортабледевицевалуес:: жетгуидвалуе**](iportabledevicevalues-getguidvalue.md) для получения любого связанного формата. И, наконец, **дисплаймесод** вызывает метод [**Ипортабледевицевалуес:: жетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) для получения данных параметра. Он передает данные, возвращаемые этими методами, в вспомогательные функции **дисплаймесодакцесс**, **DisplayFormat** и **дисплаймесодпараметерс** , которые отображают сведения для данного метода.

В следующем коде используется метод **дисплаймесод** .


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



Вспомогательная функция **дисплаймесодакцесс** получает значение типа DWORD, которое содержит параметры доступа метода. Он сравнивает это значение с командой WPD, доступное для \_ команды, \_ \_ Read и WPD, \_ \_ \_ чтобы определить права доступа метода. Используя результат, он отображает строку, указывающую ограничение доступа для данного метода.

В следующем коде используется вспомогательная функция **дисплаймесодакцесс** .


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



Вспомогательная функция **дисплаймесод** получает объект [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) и идентификатор GUID метода в качестве параметров. Используя объект **ипортабледевицесервицекапабилитиес** , он вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) для получения атрибутов метода и их отображения в окне консоли приложения.

Вспомогательная функция **дисплаймесодпараметерс** получает объект [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , GUID метода и объект ипортабледевицекэйколлектион, содержащий параметры метода. Используя объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , он вызывает метод [**Ипортабледевицесервицекапабилитиес:: жетмесодпараметераттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) для получения имени параметра, использования, VarType и формы. Эта информация отображается в окне консоли приложения.

В следующем коде используется вспомогательная функция **дисплаймесодпараметерс** .


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



