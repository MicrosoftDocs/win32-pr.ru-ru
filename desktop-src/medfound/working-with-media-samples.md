---
description: Работа с примерами мультимедиа
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Работа с примерами мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999864"
---
# <a name="working-with-media-samples"></a>Работа с примерами мультимедиа

В этом разделе описывается использование интерфейса [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) для управления примерами объектов мультимедиа. Общие сведения о примерах мультимедиа см. в статье [примеры носителей](media-samples.md).

Чтобы создать пример носителя, вызовите функцию [**мфкреатесампле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) . Изначально список буферов примера пуст. Чтобы добавить буфер в конец списка, вызовите метод [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

В следующем коде показано, как создать пример и добавить в него буфер.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



Чтобы получить буферы из образца, рекомендуется вызвать метод [**имфсампле:: конверттоконтигуаусбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Этот метод возвращает один буфер контингуаус.

Чтобы выполнить итерацию по буферам в списке, начните с вызова [**имфсампле:: жетбуфферкаунт**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount). Этот метод возвращает количество буферов. Затем вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) и укажите индекс буфера для извлечения. Буферы индексируются с нуля.

В следующем коде показано, как выполнить итерацию по буферам в примере.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Примеры имеют отметку времени и длительность. Метка времени показывает, когда данные в образце должны быть визуализированы относительно часов представления. Длительность — это период времени, в течение которого данные должны быть визуализированы. Обычно компонент, создающий данные, задает начальную отметку времени и длительность. Эти значения могут быть изменены сеансом мультимедиа. Чтобы задать метку времени, вызовите [**имфсампле:: сетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Чтобы задать длительность, вызовите [**имфсампле:: сетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Примеры также могут иметь атрибуты, которые содержат дополнительные сведения о примере. Список образцов атрибутов см. в разделе [Sample Attributes](sample-attributes.md). Чтобы задать и получить атрибуты, используйте [**интерфейс имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), который [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) наследует.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры носителей](media-samples.md)
</dt> <dt>

[Буферы мультимедиа](media-buffers.md)
</dt> </dl>

 

 



