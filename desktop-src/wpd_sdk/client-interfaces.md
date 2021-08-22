---
description: Клиентские интерфейсы
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Клиентские интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590402"
---
# <a name="client-interfaces"></a>Клиентские интерфейсы

Приложения используют методы, поддерживаемые следующими интерфейсами для выполнения операций с портативными устройствами. Эти операции включают в себя открытие подключения к устройству, получение данных с устройства, запись данных на устройство и т. д.



| Интерфейс                                                                              | Описание                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иенумпортабледевицеобжектидс**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Перечисляет объекты на портативном устройстве.                                                                                                                                                                                        |
| [**ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Обеспечивает низкий уровень доступа к портативному устройству.                                                                                                                                                                                     |
| [**ипортабледевицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Извлекает различные возможности устройства, включая Поддерживаемые форматы, команды и функциональные объекты.                                                                                                                          |
| [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Предоставляет методы для создания, перечисления и удаления содержимого на устройстве.                                                                                                                                                              |
| [**ипортабледевицедатастреам**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Предоставляет дополнительные методы в **IStream** , используемые для передачи данных.                                                                                                                                                               |
| [**ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Реализуется приложением для получения асинхронных обратных вызовов.                                                                                                                                                                   |
| [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Перечисляет устройства, подключенные к компьютеру, и предоставляет простой способ запрашивать сведения об установке устройства (включая производителя, понятное имя и описание).                                       |
| [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Чтение и запись свойств объекта на устройстве.                                                                                                                                                                              |
| [**ипортабледевицепропертиесбулк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Асинхронно считывает и записывает несколько свойств для нескольких объектов на устройстве.                                                                                                                                               |
| [**ипортабледевицепропертиесбулккаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Реализуется приложением для отслеживания хода выполнения асинхронной операции, начатой с помощью интерфейса **ипортабледевицепропертиесбулк** .                                                                          |
| [**ипортабледевицересаурцес**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Предоставляет доступ к данным объекта.                                                                                                                                                                                                |
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | только Windows 7. Обеспечивает низкий уровень доступа к службе портативных устройств.                                                                                                                                                             |
| [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | только Windows 7. Извлекает различные возможности службы, включая Поддерживаемые форматы, команды, методы и профили подготовки к просмотру.                                                                                                |
| [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | только Windows 7. Вызывает методы синхронно и асинхронно для службы.                                                                                                                                                      |
| [**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | только Windows 7. Реализовано приложением для того, чтобы отследить завершение асинхронной операции метода службы путем вызова [ **ипортабледевицесервицемесодс:: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**ипортабледевицесервицеманажер**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | только Windows 7. Перечисляет службы, поддерживаемые устройством, и извлекает устройство, связанное со службой.                                                                                                             |



 

На следующей схеме показано, как приложение получает большую часть необходимых вам интерфейсов. Показаны не все методы интерфейсов или интерфейсы, реализуемые приложением.

![Схема, демонстрирующая создание и извлечение наиболее необходимых клиентских интерфейсов](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 



