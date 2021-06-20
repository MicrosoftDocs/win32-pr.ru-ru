---
title: Получение свойств объекта WPD
description: Приложение Впдсервицеаписампле демонстрирует, как приложение может извлекать свойства объекта содержимого, поддерживаемые данной службой контактов.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404317"
---
# <a name="retrieving-wpd-object-properties"></a>Получение свойств объекта WPD

Службы часто содержат дочерние объекты, принадлежащие одному из форматов, поддерживаемых каждой службой. Например, служба контактов может поддерживать несколько контактных объектов из формата абстрактного контакта. Каждый объект Contact описывается связанными свойствами (имя контактного лица, номер телефона, адрес электронной почты и т. д.).

Приложение Впдсервицеаписампле содержит код, демонстрирующий, как приложение может извлекать свойства объекта содержимого, поддерживаемые данной службой контактов. В этом образце используются следующие интерфейсы.



| Интерфейс | Описание    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Извлекает интерфейс **IPortableDeviceContent2** для доступа к поддерживаемым методам службы. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Предоставляет доступ к методам, относящимся к содержимому.                                             |
| [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Возвращает значения свойств объекта.                                                        |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)               | Содержит значения свойств, которые были считаны для этого объекта.                                    |
| [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) | Содержит параметры для данного метода.                                                  |



 

Когда пользователь выбирает параметр "7" в командной строке, приложение вызывает метод **реадконтентпропертиес** , который находится в модуле контентпропертиес. cpp.

Этот метод получает следующие четыре свойства для указанного объекта Contact.



| Свойство                     | Описание                                                                                                                                                                                                      | PROPERTYKEY служб устройств     | Эквивалентный \_ PROPERTYKEY WPD         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Идентификатор родительского объекта     | Строка, указывающая идентификатор родителя данного объекта.                                                                                                                                            | PKEY \_ женерикобж \_ ParentID      | \_ \_ идентификатор родительского объекта \_ WPD             |
| Имя объекта                  | Строка, указывающая имя данного объекта                                                                                                                                                             | \_Имя PKEY женерикобж \_          | \_имя объекта \_ WPD                   |
| Постоянный уникальный идентификатор | Строка, указывающая уникальный идентификатор для данного объекта. Этот идентификатор сохраняется в сеансах в отличие от идентификатора объекта. Для служб это должно быть строковое представление идентификатора GUID. | PKEY \_ женерикобж \_ персистентуид | \_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD |
| Формат объекта                | Глобальный уникальный идентификатор (GUID), указывающий формат файла, соответствующего заданному объекту.                                                                                                        | PKEY \_ женерикобж \_ обжектформат  | \_Формат объекта \_ WPD                 |



 

-   Идентификатор родителя
-   Имя
-   персистентуид
-   Формат

Обратите внимание, что перед получением свойств содержимого пример приложения открывает службу контактов на подключенном устройстве.

В следующем коде для метода **реадконтентпропертиес** показано, как приложение использует интерфейс [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) для получения интерфейса [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) . Передавая ПРОПЕРТИКЭЙС запрошенных свойств в метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **реадконтентпропертиес** извлекает запрошенные значения, а затем отображает их в окне консоли.


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPropertiesToRead));
    if (SUCCEEDED(hr))
    {
        // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
        // NOTE: We are not handling any special error cases here so we can proceed with
        // adding as many of the target properties as we can.
        if (pPropertiesToRead != NULL)
        {
            HRESULT hrTemp = S_OK;
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
    if (SUCCEEDED(hr))
    {
        hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                    pPropertiesToRead,   // The properties we want to read
                                    &pObjectProperties); // Driver supplied property values for the specified object
        if (FAILED(hr))
        {
            printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
        }
    }

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



