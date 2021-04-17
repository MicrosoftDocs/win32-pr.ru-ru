---
description: Интерфейсы службы
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Интерфейсы службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711399"
---
# <a name="service-interfaces"></a>Интерфейсы службы

Некоторые интерфейсы в Media Foundation должны быть получены путем вызова метода [**имфжетсервице:: WebService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , а не путем вызова **QueryInterface**. Метод [**WebMethod**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) работает, как QueryInterface, но со следующими отличиями.

-   В дополнение к идентификатору интерфейса в нем принимается идентификатор GUID идентификатора службы.
-   Он может вернуть указатель на другой объект, реализующий интерфейс, вместо того чтобы возвращать указатель на исходный объект, к которому выполняется запрос.

> [!Note]  
> Интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) очень похож на интерфейс **IServiceProvider** , используемый в некоторых других API.

 

*Служба* — это определенный интерфейс, полученный из определенного класса объектов через интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Определены следующие службы.



| Идентификатор службы                          | Интерфейс                                                                                                                                | Объекты, которые могут предоставлять доступ к этой службе                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ служба поставщика метаданных \_ MF             | [**имфметадатапровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Источники мультимедиа                                                                                                                                     |
| \_Служба MF медиасаурце \_                    | [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Поддерживается в Windows 8.1 и более поздних версиях.<br/>                                                                                                    |
| \_PMP \_ сервера MF \_                    | [**имфпмпсервер**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Сеанс защищенного пути к носителю (PMP).                                                                                                         |
| \_службы MF Quality \_ Services                       | [**имфкуалитядвисе**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Источники мультимедиа.                                                                                                                                    |
| \_ \_ Служба управления скоростью \_ MF                  | [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Источники мультимедиа, сеанс мультимедиа                                                                                                                      |
| \_ \_ Служба управления скоростью \_ MF                  | [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Источники мультимедиа, приемники мультимедиа, сеанс мультимедиа                                                                                                         |
| \_Удаленный \_ прокси-сервер MF                           | [**имфремотепрокси**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Учетные записи-посредники для удаленных объектов.                                                                                                                       |
| \_Служба MF Sami \_                           | [**имфсамистиле**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Синхронизированный доступный источник мультимедиа обмена мультимедиа (SAMI).                                                                                    |
| \_ \_ \_ служба поставщика представления источника \_ MF | [**имфмедиасаурцепресентатионпровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Источник Sequencer                                                                                                                                  |
| Служба времени код MF \_ \_                       | [**имфтимекодетранслате**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Источник носителя ASF.                                                                                                                                 |
| \_ \_ \_ Служба редактора атрибутов MF \_ топоноде    | [**имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Сеанс мультимедиа                                                                                                                                     |
| \_инкапсулированный в оболочку \_ объект                         | [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Обтекаемые объекты                                                                                                                                   |
| \_Служба буфера с оболочкой MF \_ \_                |                                                                                                                                          | Поддерживается в Windows 8.1 и более поздних версиях.<br/>                                                                                                    |
| \_ \_ Пример службы с УПАКОВАНной MF \_                 |                                                                                                                                          | Поддерживается в Windows 8.1 и более поздних версиях.<br/>                                                                                                    |
| MF \_ ворккуеуе \_ Services                     | [**имфворккуеуесервицес**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Сеанс мультимедиа                                                                                                                                     |
| \_Служба мфнет савежоб \_                     | [**имфсавежоб**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Байтовые потоки                                                                                                                                      |
| \_Служба статистики \_ мфнетсаурце            | **ипропертисторе**                                                                                                                       | Источник сети. Используйте эту службу для получения статистики сети. См [**. \_ свойство мфнетсаурце Statistics**](mfnetsource-statistics-property.md). |
| \_ \_ служба политики MR \_ Audio                  | [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Модуль подготовки звука                                                                                                                                    |
| \_Служба буфера \_ Mr                         | **IDirect3DSurface9**                                                                                                                    | Буферы поверхности DirectX                                                                                                                           |
| \_ \_ Служба тома для политики записи \_ MR \_        | [**имфсимплеаудиоволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Источник записи звука                                                                                                                              |
| \_ \_ Служба томов с политикой MR \_                 | [**имфсимплеаудиоволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Модуль подготовки звука                                                                                                                                    |
| \_ \_ Служба тома MR \_ Stream                 | [**имфаудиостреамволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Модуль подготовки звука                                                                                                                                    |
| \_ \_ Служба ускорения видео Mr \_            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **идиректксвидеоакцелератионсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Улучшенный обработчик видео (Евр)                                                                                                                     |
| \_ \_ Служба ускорения видео Mr \_            | [**идиректксвидеомемориконфигуратион**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Входные сигналы в фильтре Евр DirectShow                                                                                                           |
| \_ \_ Служба ускорения видео Mr \_            | [**Интерфейс Имфвидеосамплеаллокатор**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Приемники потоков Евр.                                                                                                                                 |
| \_ \_ Служба видеомикшера MR \_                   | Различные интерфейсы, предоставляемые микшером Евр. См. раздел [Использование элементов управления видео микшера](using-the-video-mixer-controls.md).                   | евр                                                                                                                                               |
| \_ \_ Служба прорисовки видео Mr \_                  | Различные интерфейсы, предоставляемые средством отображения Евр. См. раздел [Использование элементов управления отображением видео](using-the-video-display-controls.md).           | евр                                                                                                                                               |



 

Для получения интерфейсов, перечисленных в этой таблице, из объектов, перечисленных в этой таблице, необходимо использовать [**службу**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Get.

В некоторых случаях интерфейс возвращается в виде службы одним классом объектов и возвращается через **QueryInterface** другим классом объектов. На страницах ссылок для каждого интерфейса указывается, когда следует использовать [**службу**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) IsReference и когда следует использовать **QueryInterface**.

> [!Caution]  
> Объект может быть реализован таким образом, что он возвращает интерфейс службы через **QueryInterface** и [**GetObject.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Однако использование **QueryInterface** , если требуется **услуга** , может привести к проблемам совместимости позже.

 

Функция [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) — это вспомогательная функция, которая запрашивает объект для [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) , а затем [**вызывает метод GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) объекта.

## <a name="examples"></a>Примеры

В следующем примере запрос к сеансу мультимедиа для [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) и получение интерфейса [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



Следующий пример эквивалентен предыдущему примеру, но использует функцию [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) .


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 




