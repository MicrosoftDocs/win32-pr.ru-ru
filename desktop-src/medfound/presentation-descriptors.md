---
description: Дескрипторы представления
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Дескрипторы представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963faeebbb180b504cc11202645a9432bbb3a94e988495b9ddcf96e550b05519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238835"
---
# <a name="presentation-descriptors"></a>Дескрипторы представления

*Презентация* — это набор связанных потоков мультимедиа с общим временем презентации. Например, презентация может состоять из видеопотоков и аудио-видео из фильма. *Дескриптор представления* — это объект, содержащий описание конкретной презентации. Дескрипторы презентации используются для настройки источников мультимедиа и некоторых приемников мультимедиа.

Каждый дескриптор презентации содержит список из одного или нескольких *потоковых дескрипторов*. Они описывают потоки в презентации. Потоки можно либо выбрать, либо отменить выбор. Данные создаются только выбранными потоками. Невыбранные потоки не являются активными и не создают никаких данных. Каждый дескриптор потока имеет *обработчик типа мультимедиа*, который используется для изменения типа носителя потока или получения текущего типа мультимедиа потока. (Дополнительные сведения о типах носителей см. в разделе [типы носителей](media-types.md).)

В следующей таблице показаны основные интерфейсы, предоставляемые каждым из этих объектов.



| Объект                  | Интерфейс                                                      |
|-------------------------|----------------------------------------------------------------|
| Дескриптор представления | [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Дескриптор потока       | [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Обработчик типа мультимедиа      | [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Презентации источника мультимедиа

Каждый источник мультимедиа предоставляет дескриптор представления, описывающий конфигурацию по умолчанию для источника. В конфигурации по умолчанию выбран по крайней мере один поток, и каждый выбранный поток имеет тип мультимедиа. Чтобы получить дескриптор презентации, вызовите метод [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Метод возвращает указатель [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

Вы можете изменить дескриптор представления исходного кода, чтобы выбрать другой набор потоков. Не изменяйте дескриптор представления, если источник мультимедиа не остановлен. Изменения применяются при вызове [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) для запуска источника.

Чтобы получить количество потоков, вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Чтобы получить дескриптор потока для потока, вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) и передайте индекс потока. Потоки индексируются с нуля. Метод **жетстреамдескрипторбиндекс** возвращает указатель [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) . Он также возвращает логический флаг, указывающий, выбран ли поток. Если выбран поток, источник мультимедиа создает данные для этого потока. В противном случае источник не создает никаких данных для этого потока. Чтобы выбрать поток, вызовите [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) с индексом потока. Чтобы отменить выбор потока, вызовите [**имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

В следующем коде показано, как получить дескриптор представления из источника мультимедиа и перечислить потоки.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Обработчики типов мультимедиа

Чтобы изменить тип носителя потока или получить текущий тип мультимедиа потока, используйте обработчик типа мультимедиа дескриптора потока. Вызовите метод [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) , чтобы получить обработчик типа мультимедиа. Этот метод возвращает указатель [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

Если нужно просто узнать, какой тип данных находится в потоке, например в аудио или видео, вызовите [**имфмедиатипехандлер:: жетмажортипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Этот метод возвращает идентификатор GUID для основного типа носителя. Например, приложение воспроизведения обычно подключает звуковой поток к обработчику звука и видеопотоку для модуля подготовки видео. При использовании сеанса мультимедиа или загрузчика топологии для создания топологии основной GUID типа может быть единственным нужным вам сведениям о форматировании.

Если приложению требуются более подробные сведения о текущем формате, вызовите [**имфмедиатипехандлер:: жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Этот метод возвращает указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) типа мультимедиа. Используйте этот интерфейс для получения сведений о формате.

Обработчик типа мультимедиа также содержит список поддерживаемых типов носителей для потока. Чтобы получить размер списка, вызовите метод [**имфмедиатипехандлер:: жетмедиатипекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Чтобы получить тип мультимедиа из списка, вызовите [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) с индексом типа мультимедиа. Типы носителей возвращаются в порядке приближения к приоритету. Например, для звуковых форматов предпочтительнее использовать более высокие скорости выборки по сравнению с более низкими тарифами. Однако нет правила, определяющего порядок, поэтому его следует рассматривать как правило.

Список поддерживаемых типов может не содержать все возможные типы носителей, поддерживаемые потоком. Чтобы проверить, поддерживается ли определенный тип носителя, вызовите метод [**имфмедиатипехандлер:: исмедиатипесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Чтобы задать тип мультимедиа, вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Если метод завершится с ошибкой, поток будет содержать данные, которые соответствует указанному формату. Метод **сеткуррентмедиатипе** не изменяет список предпочтительных типов.

В следующем коде показано, как получить обработчик типа мультимедиа, перечислить предпочтительные типы мультимедиа и задать тип носителя. В этом примере предполагается, что приложение имеет некоторый алгоритм, не показанный здесь, для выбора типа носителя. Конкретные особенности будут сильно зависеть от вашего приложения.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



