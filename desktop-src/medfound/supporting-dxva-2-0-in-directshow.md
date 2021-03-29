---
description: В этом разделе описано, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в фильтре декодера DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Поддержка ДКСВА 2,0 в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898174"
---
# <a name="supporting-dxva-20-in-directshow"></a>Поддержка ДКСВА 2,0 в DirectShow

В этом разделе описано, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в фильтре декодера DirectShow. В частности, он описывает взаимодействие между декодером и модулем подготовки видео. В этом разделе не описывается, как реализовать декодирование ДКСВА.

-   [Предварительные условия](#prerequisites)
-   [Примечания по миграции](#migration-notes)
-   [Поиск конфигурации декодера](#finding-a-decoder-configuration)
-   [Уведомление модуля подготовки видео](#notifying-the-video-renderer)
-   [Выделение несжатых буферов](#allocating-uncompressed-buffers)
-   [Декодирование](#decoding)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

В этом разделе предполагается, что вы знакомы с написанием фильтров DirectShow. Дополнительные сведения см. в разделе [Создание фильтров DirectShow](../directshow/writing-directshow-filters.md) в документации по пакету SDK для DirectShow. В примерах кода в этом разделе предполагается, что фильтр декодера является производным от класса [**ктрансформфилтер**](../directshow/ctransformfilter.md) со следующим определением класса:


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



В оставшейся части этого раздела термин *декодера* относится к фильтру декодера, который получает сжатое видео и выводит несжатое видео. Термин *устройство декодера* относится к аппаратному ускорителю, реализованному графическим драйвером.

Ниже приведены основные шаги, которые должен выполнить фильтр декодера для поддержки ДКСВА 2,0:

1.  Согласование типа мультимедиа.
2.  Найдите конфигурацию декодера ДКСВА.
3.  Уведомление модуля подготовки отчетов о том, что декодер использует декодирование ДКСВА.
4.  Предоставьте пользовательский распределитель, который выделяет поверхности Direct3D.

Эти действия более подробно описаны в оставшейся части этого раздела.

## <a name="migration-notes"></a>Примечания по миграции

При миграции с ДКСВА 1,0 необходимо учитывать некоторые существенные различия между двумя версиями:

-   ДКСВА 2,0 не использует интерфейсы [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) и [**иамвидеоакцелераторнотифи**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , так как декодер может обращаться к API дксва 2,0 напрямую через интерфейс [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
-   Во время согласования типа мультимедиа декодер не использует GUID ускорения видео в качестве подтипа. Вместо этого подтип является просто несжатым видеоформатом (например, NV12), как при декодировании программного обеспечения.
-   Процедура настройки сочетания клавиш была изменена. В ДКСВА 1,0 декодер вызывает **EXECUTE** с помощью структуры **дксва \_ конфигпиктуредекоде** для настройки акцерлатор. В ДКСВА 2,0 декодер использует интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , как описано в следующем разделе.
-   Декодер выделяет несжатые буферы. Модуль подготовки видео больше не выделяет их.
-   Вместо вызова [**иамвидеоакцелератор::D исплайфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) для отображения декодированного кадра декодер доставляет кадр в модуль подготовки, вызывая [**Имеминпутпин:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), как и при декодировании программного обеспечения.
-   Декодер больше не отвечает за проверку безопасности буферов данных для обновлений. Поэтому ДКСВА 2,0 не имеет метода, эквивалентного [**иамвидеоакцелератор:: куерирендерстатус**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).
-   Наложение изображений выполняется модулем подготовки видео с помощью API процессора ДКСВА 2.0 Video. Декодеры, которые предоставляют подизображения (например, декодеры DVD), должны отсылать данные субтитров на отдельный выходной ПИН-код.

Для операций декодирования ДКСВА 2,0 использует те же структуры данных, что и ДКСВА 1,0.

Расширенный фильтр модуля подготовки видео (Евр) поддерживает ДКСВА 2,0. Фильтры рендеринга для микширования видео (VMR-7 и VMR-9) поддерживают только ДКСВА 1,0.

## <a name="finding-a-decoder-configuration"></a>Поиск конфигурации декодера

После того как декодер согласовывает тип выходного носителя, он должен найти совместимую конфигурацию для устройства декодера ДКСВА. Этот шаг можно выполнить в методе [**кбасеаутпутпин:: комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md) выходного контакта. Этот шаг гарантирует, что графический драйвер поддерживает возможности, необходимые для работы декодера, прежде чем декодер зафиксируется с помощью ДКСВА.

Чтобы найти конфигурацию для устройства декодера, выполните следующие действия.

1.  Запросите входной ПИН-код модуля подготовки отчетов для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Идентификатор GUID службы — это \_ Служба ускорения видео (MR) \_ \_ .
3.  Вызовите [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить маркер устройства Direct3D визуализатора.
4.  Вызовите [**IDirect3DDeviceManager9:: жетвидеосервице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) и передайте в него маркер устройства. Этот метод возвращает указатель на интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Вызовите [**идиректксвидеодекодерсервице:: жетдекодердевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Этот метод возвращает массив идентификаторов GUID устройства декодера.
6.  Пройдите по массиву идентификаторов GUID декодера, чтобы найти те, которые поддерживает фильтр декодера. Например, для декодера MPEG-2 необходимо найти **DXVA2 \_ ModeMPEG2 \_ мокомп**, **DXVA2 \_ ModeMPEG2 \_ идкт** или **DXVA2 \_ ModeMPEG2 \_ ВЛД**.

7.  При обнаружении идентификатора GUID устройства-кандидата передайте GUID в метод [**идиректксвидеодекодерсервице:: жетдекодеррендертаржетс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Этот метод возвращает массив форматов целевого объекта прорисовки, указанных как значения **D3DFORMAT** .
8.  Пройдите по форматам целевого объекта рендеринга и найдите тот, который соответствует выходному формату. Как правило, устройство декодера поддерживает один формат целевого объекта рендеринга. Фильтр декодера должен подключаться к модулю подготовки отчетов с помощью этого подтипа. При первом вызове [**комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md)декодер может запрограммировать формат целевого объекта прорисовки, а затем вернуть этот формат в качестве предпочтительного выходного типа.

9.  Вызовите [**идиректксвидеодекодерсервице:: жетдекодерконфигуратионс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Передайте тот же GUID устройства декодера, а также структуру [**DXVA2 \_ видеодеск**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) , описывающую предложенный формат. Метод возвращает массив структур [**DXVA2 \_ конфигпиктуредекоде**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Каждая структура описывает одну возможную конфигурацию для устройства декодера.

10. При условии, что предыдущие шаги выполнены успешно, сохраните маркер устройства Direct3D, GUID устройства декодера и структуру конфигурации. Этот фильтр будет использовать эти сведения для создания устройства декодера.

В следующем коде показано, как найти конфигурацию декодера.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Поскольку этот пример является универсальным, часть логики была помещена в вспомогательные функции, которые необходимо реализовать с помощью декодера. В следующем коде показаны объявления для этих функций:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Уведомление модуля подготовки видео

Если декодер находит конфигурацию декодера, следующий шаг заключается в уведомлении модуля подготовки отчетов о том, что декодер будет использовать аппаратное ускорение. Этот шаг можно выполнить в методе [**комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md) . Этот шаг должен быть выполнен до выбора распределителя, так как он влияет на выбор распределителя.

1.  Запросите входной ПИН-код модуля подготовки отчетов для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**идиректксвидеомемориконфигуратион**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) . Идентификатор GUID службы — **это \_ \_ \_ Служба ускорения видео (MR**).
3.  Вызовите метод [**идиректксвидеомемориконфигуратион:: жетаваилаблесурфацетипебиндекс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) в цикле, увеличивая переменную *двтипеиндекс* с нуля. Останавливаться, когда метод возвращает значение **DXVA2 \_ сурфацетипе \_ декодеррендертаржет** в параметре *пдвтипе* . Этот шаг гарантирует, что модуль подготовки видео поддерживает декодирование с аппаратным ускорением. Этот шаг всегда будет выполняться для фильтра Евр.
4.  Если предыдущий шаг выполнен, вызовите [**идиректксвидеомемориконфигуратион:: сетсурфацетипе**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) со значением DXVA2 \_ сурфацетипе \_ декодеррендертаржет. При вызове **сетсурфацетипе** с этим значением модуль подготовки видео переводится в режим дксва. Если модуль подготовки видео находится в этом режиме, декодер должен предоставить собственный распределитель.

В следующем коде показано, как уведомлять модуль подготовки видео.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Если декодер находит допустимую конфигурацию и успешно уведомляет модуль подготовки видео, декодер может использовать ДКСВА для декодирования. Декодер должен реализовать пользовательский распределитель для своего выходного ПИН-кода, как описано в следующем разделе.

## <a name="allocating-uncompressed-buffers"></a>Выделение несжатых буферов

В ДКСВА 2,0 декодер отвечает за выделение поверхностей Direct3D для использования в качестве несжатых буферов видео. Поэтому декодер должен реализовать пользовательский распределитель, который будет создавать поверхности. Примеры носителей, предоставляемые этим распределителем, будут содержать указатели на поверхности Direct3D. Евр получает указатель на поверхность, вызывая [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) на примере носителя. Идентификатор службы — это **\_ \_ Служба буфера MR**.

Чтобы предоставить пользовательский распределитель, выполните следующие действия.

1.  Определите класс для образцов мультимедиа. Этот класс может быть производным от класса [**кмедиасампле**](../directshow/cmediasample.md) . Внутри этого класса выполните следующие действия.
    -   Сохранить указатель на поверхность Direct3D.
    -   Реализуйте интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . В методе [**службы**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , если идентификатор GUID службы — это **\_ \_ Служба буфера MR**, запросите область Direct3D для запрошенного интерфейса. В противном случае служба " **услуга** " может вернуть **\_ \_ неподдерживаемую \_ службу MF E**.
    -   Переопределите метод [**кмедиасампле::**](../directshow/cmediasample-getpointer.md) noreturn, возвращающий E \_ нотимпл.
2.  Определите класс для распределителя. Распределитель может быть производным от класса [**кбасеаллокатор**](../directshow/cbaseallocator.md) . Внутри этого класса выполните следующие действия.
    -   Переопределите метод [**кбасеаллокатор:: Alloc**](../directshow/cbaseallocator-alloc.md) . Внутри этого метода вызовите [**идиректксвидеоакцелератионсервице:: креатесурфаце**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) , чтобы создать поверхности. (Интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) наследует этот метод от [**идиректксвидеоакцелератионсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)
    -   Переопределите метод [**кбасеаллокатор:: Free**](../directshow/cbaseallocator-free.md) , чтобы освободить поверхности.
3.  В закреплениях вывода фильтра Переопределите метод [**кбасеаутпутпин:: иниталлокатор**](../directshow/cbaseoutputpin-initallocator.md) . Внутри этого метода создайте экземпляр пользовательского распределителя.
4.  В фильтре реализуйте метод [**ктрансформфилтер::D еЦидебуфферсизе**](../directshow/ctransformfilter-decidebuffersize.md) . Параметр *pProperties* указывает количество поверхностей, требуемое для Евр. Добавьте к этому значению число поверхностей, которое требуется вашему декодеру, и вызовите [**имемаллокатор:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) на распределителье.

В следующем коде показано, как реализовать пример класса мультимедиа:


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



В следующем коде показано, как реализовать метод [**Alloc**](../directshow/cbaseallocator-alloc.md) для распределителя.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Ниже приведен код для метода [**Free**](../directshow/cbaseallocator-free.md) :


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



Дополнительные сведения о реализации пользовательских распределительов см. в разделе, посвященном [пользовательскому распределительу](../directshow/providing-a-custom-allocator.md) документации по пакету SDK для DirectShow.

## <a name="decoding"></a>Декодирование

Чтобы создать устройство декодера, вызовите метод [**идиректксвидеодекодерсервице:: креатевидеодекодер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Метод возвращает указатель на интерфейс [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) устройства декодера.

Для проверки маркера устройства в каждом кадре вызовите [**IDirect3DDeviceManager9:: тестдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) . Если устройство изменилось, метод возвращает DXVA2 \_ E \_ новое \_ видео \_ устройство. Если это происходит, выполните следующие действия.

1.  Закройте обработчик устройства, вызвав [**IDirect3DDeviceManager9:: клоседевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Освободите указатели [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) и [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Откройте новый маркер устройства.
4.  Согласование новой конфигурации декодера, как описано в разделе [Поиск конфигурации декодера](#finding-a-decoder-configuration).
5.  Создайте новое устройство декодера.

Предполагая, что маркер устройства является допустимым, процесс декодирования работает следующим образом:

1.  Вызовите [**идиректксвидеодекодер:: бегинфраме**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Сделайте следующее или несколько раз:
    1.  Вызовите [**идиректксвидеодекодер::-buffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , чтобы получить буфер декодера дксва.
    2.  Заполните буфер.
    3.  Вызовите [**идиректксвидеодекодер:: релеасебуффер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Вызовите метод [**идиректксвидеодекодер:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , чтобы выполнить операции декодирования в кадре.

ДКСВА 2,0 использует те же структуры данных, что и ДКСВА 1,0, для операций декодирования. Для исходного набора профилей ДКСВА (для H. 261, H. 263 и MPEG-2) эти структуры данных описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

В каждой паре вызовов [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**выполнения**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) бегинфраме можно вызвать метод несколько [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) раз, но только один раз для каждого типа буфера дксва. Если вызвать его дважды с тем же типом буфера, данные будут перезаписаны.

После вызова [**EXECUTE**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)вызовите [**Имеминпутпин:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) , чтобы передать кадр в модуль подготовки видео, как при декодировании программного обеспечения. Метод **Receive** является асинхронным; После возврата декодер может продолжить декодирование следующего кадра. Драйвер дисплея предотвращает перезапись буфера во время использования буфера всеми командами декодирования. Декодер не должен повторно использовать поверхность для декодирования другого кадра, пока модуль подготовки отчетов не выпустит пример. Когда модуль подготовки отчетов освобождает пример, распределитель помещает пример обратно в пул доступных образцов. Чтобы получить следующий доступный пример, вызовите метод [**кбасеаутпутпин:: жетделиверибуффер**](../directshow/cbaseoutputpin-getdeliverybuffer.md), который, в свою очередь, вызывает [**имемаллокатор::**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)GetNext. Дополнительные сведения см. в разделе Общие сведения о [потоке данных в DirectShow](../directshow/overview-of-data-flow-in-directshow.md) в документации по DirectShow.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ускорение видео DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
