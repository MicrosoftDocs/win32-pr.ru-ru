---
description: Клиентские интерфейсы
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Клиентские интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911143"
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
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Только Windows 7. Обеспечивает низкий уровень доступа к службе портативных устройств.                                                                                                                                                             |
| [**ипортабледевицесервицекапабилитиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Только Windows 7. Извлекает различные возможности службы, включая Поддерживаемые форматы, команды, методы и профили подготовки к просмотру.                                                                                                |
| [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Только Windows 7. Вызывает методы синхронно и асинхронно для службы.                                                                                                                                                      |
| [**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Только Windows 7. Реализовано приложением для того, чтобы отследить завершение асинхронной операции метода службы путем вызова [ **ипортабледевицесервицемесодс:: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**ипортабледевицесервицеманажер**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Только Windows 7. Перечисляет службы, поддерживаемые устройством, и извлекает устройство, связанное со службой.                                                                                                             |



 

На следующей схеме показано, как приложение получает большую часть необходимых вам интерфейсов. Показаны не все методы интерфейсов или интерфейсы, реализуемые приложением.

![Схема, демонстрирующая создание и извлечение наиболее необходимых клиентских интерфейсов](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 



