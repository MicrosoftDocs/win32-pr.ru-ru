---
description: Microsoft Media Foundation поддерживает запись аудио и видео.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Видеозапись Аудио/видео в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693868"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Видеозапись Аудио/видео в Media Foundation

Microsoft Media Foundation поддерживает запись аудио и видео. Устройства видеозаписи поддерживаются драйвером класса УВК и должны быть совместимы с УВК 1,1. Устройства записи звука поддерживаются через API сеанса Windows Audio (ВАСАПИ).

Устройство записи представляется в Media Foundation объектом источника мультимедиа, который предоставляет интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . В большинстве случаев приложение не будет использовать этот интерфейс напрямую, но будет использовать API более высокого уровня, например [средство чтения исходного кода](source-reader.md) для управления устройством записи.

## <a name="enumerate-capture-devices"></a>Перечисление устройств записи

Чтобы перечислить устройства записи в системе, выполните следующие действия.

1.  Вызовите функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.
2.  Задайте для [атрибута \_ девсаурце \_ \_ \_ типа источника атрибута MF](mf-devsource-attribute-source-type.md) одно из следующих значений:

    | Значение                                                    | Описание                      |
    |----------------------------------------------------------|----------------------------------|
    | **\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ аудкап \_ GUID** | Перечисление устройств записи звука. |
    | **\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ GUID** | Перечисление устройств видеозаписи. |

    

     

3.  Вызовите функцию [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Эта функция выделяет массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Каждый указатель представляет объект активации для одного устройства в системе.
4.  Вызовите метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , чтобы создать экземпляр источника мультимедиа из одного из объектов активации.

В следующем примере создается источник мультимедиа для первого устройства записи видео в списке перечисления:


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



Вы можете запросить объекты активации для различных атрибутов, включая следующие:

-   Атрибут [ \_ \_ \_ понятного \_ имени атрибута MF девсаурце](mf-devsource-attribute-friendly-name.md) содержит отображаемое имя устройства. Отображаемое имя подходит для отображения пользователю, но оно может быть неуникальным.
-   Для видеоустройств [ \_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ символьная \_ ссылка](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) содержит символическую ссылку на устройство. Символьная ссылка уникальным образом идентифицирует устройство в системе, но не является строкой, доступной для чтения.
-   Для звуковых устройств в атрибуте [ \_ девсаурце \_ \_ типа источника атрибут MF \_ \_ аудкап \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) содержится идентификатор конечной точки аудио устройства. Идентификатор конечной точки аудио похож на символическую ссылку. Он однозначно определяет устройство в системе, но не является строкой, доступной для чтения.

Следующий пример принимает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей и выводит отображаемое имя каждого устройства в окне отладки:


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



Если вы уже знакомы с символической ссылкой для видеоустройства, существует другой способ создания источника мультимедиа для устройства:

1.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.
2.  Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника](mf-devsource-attribute-source-type.md) атрибут **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ \_ GUID видкап**.
3.  Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника \_ видкап \_ символьную \_ ссылку](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) на символьную ссылку.
4.  Вызовите функцию [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Первый возвращает указатель [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Последний возвращает указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) на объект активации. Для создания источника можно использовать объект активации. (Объект активации можно маршалировать в другой процесс, поэтому он полезен, если необходимо создать источник в другом процессе. Дополнительные сведения см. в разделе [объекты активации](activation-objects.md).)

В следующем примере используется символьная ссылка видеоустройства и создается источник мультимедиа.


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



Существует эквивалентный способ создания звукового устройства из идентификатора конечной точки аудио:

1.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.
2.  Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника](mf-devsource-attribute-source-type.md) атрибут **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ \_ GUID аудкап**.
3.  Задайте для [атрибута \_ девсаурце \_ \_ типа источника атрибута MF \_ \_ аудкап \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) идентификатор конечной точки.
4.  Вызовите функцию [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

В следующем примере используется идентификатор конечной точки аудио и создается источник мультимедиа.


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>Использование устройства записи

После создания источника мультимедиа для устройства записи используйте [средство чтения исходного кода](source-reader.md) для получения данных с устройства. Модуль чтения исходного кода предоставляет примеры носителей, содержащие звуковые данные и видеокадры записи. Следующий шаг зависит от сценария приложения:

-   Предварительный просмотр видео. Используйте Microsoft Direct3D или Direct2D для вывода видео.
-   Запись файла. для кодирования файла используйте [модуль записи приемника](sink-writer.md) .
-   Предварительный просмотр аудио: используйте [васапи](/windows/desktop/CoreAudio/wasapi).

Если вы хотите объединить запись звука с видеозаписью, используйте *Объединенный источник мультимедиа*. Объединенный источник мультимедиа содержит коллекцию источников мультимедиа и объединяет все свои потоки в один объект источника мультимедиа. Чтобы создать экземпляр агрегатного источника мультимедиа, вызовите функцию [**мфкреатеаггрегатесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .

## <a name="shut-down-the-capture-device"></a>Завершение работы устройства записи

Если устройство записи больше не требуется, необходимо завершить работу устройства, вызвав метод [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) для объекта [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , полученного путем вызова [**Мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Сбой вызова функции **завершения работы** может привести к созданию ссылок на память, так как система может оставаться ссылкой на ресурсы **имфмедиасаурце** , пока не будет вызвано **Завершение работы** .


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Если вы выделили строку, содержащую символическую ссылку на устройство записи, также следует освободить этот объект.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> </dl>

 

 
