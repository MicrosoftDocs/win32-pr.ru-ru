---
description: В этом разделе описывается, как перечислить устройства видеозаписи в системе пользователей и как создать экземпляр устройства.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Перечисление устройств видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476c4b41e6f8913414200c7a811ba9625f2c4bc9cfea66875ec5f15b788bdc05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061624"
---
# <a name="enumerating-video-capture-devices"></a>Перечисление устройств видеозаписи

В этом разделе описывается, как перечислить устройства видеозаписи в системе пользователя и как создать экземпляр устройства.

Чтобы перечислить устройства видеозаписи в системе, выполните следующие действия.

1.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов. Эта функция получает указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Вызовите метод [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) , чтобы задать атрибут [ \_ \_ \_ \_ типа источника атрибута MF девсаурце](mf-devsource-attribute-source-type.md) . Задайте для атрибута значение **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ видкап \_ GUID**.
3.  Вызовите [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources). Эта функция получает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей и размер массива. Каждый указатель представляет отдельное устройство захвата видео.

Чтобы создать экземпляр устройства записи, выполните следующие действия.

-   Вызовите метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , чтобы получить указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .

Следующий код показывает эти действия.


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



После создания источника мультимедиа Освободите указатели интерфейса и освободите память для массива:


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



