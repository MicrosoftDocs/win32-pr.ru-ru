---
description: Сведения об API Ммдевице
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Сведения об API Ммдевице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e2f33c6969e00006c12b0bc6dc1ba37b70c5ff38ea2846633d5eb61da03b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077548"
---
# <a name="about-mmdevice-api"></a>Сведения об API Ммдевице

API Windows мультимедиа-устройства (ммдевице) позволяет клиентам аудио находить [устройства конечных точек аудио](audio-endpoint-devices.md), определять их возможности и создавать экземпляры драйверов для этих устройств.

Файл заголовка Ммдевицеапи. h определяет интерфейсы в API Ммдевице.

API Ммдевице состоит из нескольких интерфейсов. Первый из них — интерфейс [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Для доступа к интерфейсам в API Ммдевице клиент получает ссылку на интерфейс **иммдевицеенумератор** объекта перечислителя устройства, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , как показано в следующем фрагменте кода:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



В предыдущем фрагменте кода CLSID \_ ммдевицеенумератор и IID \_ иммдевицеенумератор — это значения GUID, которые присоединяются как атрибуты к объекту **ммдевицеенумератор** Class и к интерфейсу [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Вызов [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) передает эти значения по ссылке. Переменная `hr` имеет тип **HRESULT**, а переменная `pEnumerator` — указатель на интерфейс **иммдевицеенумератор** объекта перечислителя устройства. **Иммдевицеенумератор** предоставляет методы для перечисления устройств конечных точек аудио. сведения об операторе **\_ \_ ууидоф** , функции **cocreateinstance** и \_ константах клскткс *Xxx* см. в документации по Windows SDK.

С помощью интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) клиент может получить ссылки на другие интерфейсы в API ммдевице. API Ммдевице реализует следующие интерфейсы.



| Интерфейс                                          | Описание                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Представляет звуковое устройство.                     |
| [**иммдевицеколлектион**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Представляет коллекцию звуковых устройств.       |
| [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Предоставляет методы для перечисления звуковых устройств. |
| [**иммендпоинт**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Представляет устройство звуковой конечной точки.            |



 

Кроме того, клиенты API Ммдевице, которым требуется уведомление об изменениях состояния на устройствах конечных точек аудио, должны реализовать следующий интерфейс.



| Интерфейс                                              | Описание                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Предоставляет уведомления при добавлении или удалении устройства конечной точки аудио, при изменении состояния или свойств устройства, а также при изменении роли по умолчанию, назначенной устройству. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устройства конечных точек звука](audio-endpoint-devices.md)
</dt> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 
