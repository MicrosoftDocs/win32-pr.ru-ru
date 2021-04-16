---
description: Получение свойств для одного объекта
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Получение свойств для одного объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712480"
---
# <a name="retrieving-properties-for-a-single-object"></a>Получение свойств для одного объекта

После того как приложение извлекает идентификатор объекта (см. раздел " [Перечисление содержимого](enumerating-content.md) ") для данного объекта, он может получить описательные сведения об этом объекте, вызвав методы в [**интерфейсе ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) и [**интерфейсе ипортабледевицекэйколлектион**](iportabledevicekeycollection.md).

Метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) GetObject извлекает список указанных свойств для заданного объекта. (Приложение может также вызвать метод GetObjects и указать значение **null** для параметра PKEY, чтобы получить все свойства для данного объекта, однако производительность этого метода может значительно замедлиться при получении всех свойств.)

Однако перед тем, как приложение вызовет методы GetObject, необходимо задать свойства для извлечения, задав соответствующие ключи в [**объекте ипортабледевицекэйколлектион**](iportabledevicekeycollection.md). Приложение определит интересующие вас свойства, вызвав метод [**ипортабледевицекэйколлектион:: Add**](iportabledevicekeycollection-add.md) и УКАЗАВ значение PROPERTYKEY, идентифицирующее каждое свойство, которое оно будет извлекать.

Функция Реадконтентпропертиес в модуле Контентпропертиес. cpp примера приложения демонстрирует, как извлекаются пять свойств для выбранного объекта. В следующей таблице описаны все эти свойства и соответствующие значения РЕФПРОПЕРТИКЭЙ.



| Свойство                     | Описание                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Идентификатор родительского объекта     | Строка, указывающая идентификатор родителя данного объекта.                                                                            | \_ \_ идентификатор родительского объекта \_ WPD             |
| Имя объекта                  | Строка, указывающая имя данного объекта.                                                                                            | \_имя объекта \_ WPD                   |
| Постоянный уникальный идентификатор | Строка, указывающая уникальный идентификатор для данного объекта. (Этот идентификатор сохраняется в сеансах, в отличие от идентификатора объекта.) | \_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD |
| Формат объекта                | Глобальный уникальный идентификатор (GUID), указывающий формат файла, соответствующего заданному объекту.                                       | \_Формат объекта \_ WPD                 |
| Тип содержимого объекта          | Идентификатор GUID, указывающий тип содержимого, связанного с данным объектом.                                                                        | \_ \_ тип содержимого объекта \_ WPD          |



 

В следующем фрагменте функции Реадконтентпропертиес показано, как в примере приложения использовался [**интерфейс ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) и метод [**Ипортабледевицекэйколлектион:: Add**](iportabledevicekeycollection-add.md) для определения получаемых свойств.


```C++
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
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



После того как пример приложения настроил соответствующие ключи, он вызывает метод [**ипортабледевицепропертиес::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) GetObject, чтобы получить указанные значения для заданного объекта.


```C++
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
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



