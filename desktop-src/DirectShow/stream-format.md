---
description: Формат потока
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Формат потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684117"
---
# <a name="stream-format"></a>Формат потока

Драйвер МСДВ и УВК может выводить два формата DV: чередование аудио-видео или видео. Чередование аудио-видео — это исходный формат с устройства. Формат видео содержит те же данные, но образцы помечены как не имеющие звуковых данных. Формат видео хранится в основном для обеспечения совместимости с приложениями, которые используют видео для Windows. Дополнительные сведения см. в разделе [видео AVI типа "тип 1" и "тип-2](type-1-vs--type-2-dv-avi-files.md)".

**Драйвер МСДВ**

Драйвер МСДВ имеет два выходных контакта. Первый выходной ПИН-код отправляет данные с чередованием, а второй выходной закрепление отправляет данные только для видео. В каждый момент времени может быть подключен только один выходной ПИН-код. Чтобы выбрать формат, подключите соответствующий выходной ПИН-код. Для поиска формата можно использовать интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) на выходном ПИН-коде.

**Драйвер УВК**

В отличие от драйвера МСДВ драйвер УВК доставляет оба формата из одного и того же ПИН-кода. Форматом по умолчанию является "только видео". Чтобы выбрать формат, используйте интерфейс **иамстреамконфиг** на выходном ПИН-коде. Вызовите метод **жетстреамкапс** , чтобы перечислить типы мультимедиа для выходного контакта. Если основной тип соответствует требуемому формату, то для каждого типа носителя вызовите **сетформат** и передайте этот тип мультимедиа.



| Формат                      | Основной тип             |
|-----------------------------|------------------------|
| Аудио и видео с чередованием | \_Чередующийся MEDIATYPE |
| Только видео                  | \_Видео MEDIATYPE       |



 

Следующая функция задает формат, основанный на идентификаторе GUID основного типа.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



Драйвер МСДВ также поддерживает **иамстреамконфиг**, поэтому можно написать код, который работает для обоих типов устройств.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



