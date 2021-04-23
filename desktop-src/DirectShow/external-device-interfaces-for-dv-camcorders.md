---
description: Внешние интерфейсы устройств для цифровых видеокамер
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Внешние интерфейсы устройств для цифровых видеокамер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909802"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a>Внешние интерфейсы устройств для цифровых видеокамер

Фильтр [записи видео WDM](wdm-video-capture-filter.md) предоставляет три интерфейса для управления видеокамерой.



| Метка | Значение |
|------------------------------------------------|-------------------------------------------------|
| [**иамекстдевице**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Базовый интерфейс для внешнего управления устройством. |
| [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Управляет функциями ВИДЕОМАГНИТОФОНА.                     |
| [**иамтимекодереадер**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Считывает код времени с устройства.                 |



 

> [!Note]  
> Чтобы использовать эти интерфейсы с драйвером видеокамеры МСДВ, включите в проект файл заголовка Кспртдефс. h.

 

После выбора устройства записи и создания экземпляра фильтра записи запросите фильтр для этих интерфейсов. В следующем примере объявляется пользовательская структура, содержащая указатели интерфейса, а также логические значения, определяющие доступность каждого интерфейса:


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



