---
description: Получение свойств для нескольких объектов по формату объектов
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Получение свойств для нескольких объектов по формату объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497847"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Получение свойств для нескольких объектов по формату объектов

Помимо полного извлечения свойств для коллекции идентификаторов объектов, приложение может также выполнять полное извлечение свойств для всех объектов определенного типа. Как и в предыдущем примере, для полного извлечения для данного типа требуется, чтобы драйвер устройства поддерживал операции полного извлечения.

Приложение может выполнять групповое извлечение с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Предоставляет доступ к методам, относящимся к содержимому.                   |
| [**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)                 | Используется для задания извлекаемых свойств.                   |
| [**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Используется для определения того, поддерживает ли данный драйвер групповые операции. |
| [**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Поддерживает операцию извлечения с массовым набором.                             |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для хранения идентификаторов объектов для групповой операции.       |



 

Функция Реадконтентпропертиесбулкфилтерингформат в модуле Контентпропертиес. cpp примера приложения демонстрирует операцию множественного извлечения для объектов определенного типа или формата.

Код, обнаруженный в функции Реадконтентпропертиесбулкфилтерингформат, почти идентичен коду, обнаруженному в функции Реадконтентпропертиесбулк. (Полное описание этой функции см. в разделе [Получение свойств для нескольких объектов](retrieving-properties-for-multiple-objects.md) .)

Одно основное различие возникает при постановке операции в очередь. При фильтрации по типу или формату вызывается метод [**ипортабледевицепропертиесбулк:: куеуежетвалуесбйобжектформат**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) , а не метод [**Ипортабледевицепропертиесбулк:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Интерфейс Ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



