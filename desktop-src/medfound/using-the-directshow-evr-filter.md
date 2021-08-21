---
description: использование DirectShow фильтра евр
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: использование DirectShow фильтра евр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc454b6d298546afdbb5a06b7081505d9ddd7c2ab87a816e79bdb13836e9a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737317"
---
# <a name="using-the-directshow-evr-filter"></a>использование DirectShow фильтра евр

Чтобы создать расширенный фильтр модуля подготовки видео (Евр), вызовите **CoCreateInstance**. CLSID — это CLSID \_ енханцедвидеорендерер, определенный в UUID. h. Для использования фильтра Евр не нужно вызывать [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) или [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) .

дополнительные сведения об использовании фильтра евр в приложении DirectShow см. [в разделе воспроизведение звука и видео в DirectShow](../directshow/audio-video-playback-in-directshow.md).

Фильтр Евр начинается с одного входного ПИН-кода, который соответствует потоку ссылок. Чтобы добавить контакты для вложенных потоков, запросите фильтр для интерфейса [**иеврфилтерконфиг**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) и вызовите [**Иеврфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Вызовите этот метод перед подключением входных ПИН-кодов. ПИН-код 0 всегда является ссылочным потоком. Подключение этот пин-код перед любыми другими контактами, так как формат ссылочного потока может ограничить доступные форматы подпотока.

Перед запуском графа задайте окно обрезки видео и прямоугольник назначения. Дополнительные сведения см. [в разделе Использование элементов управления отображением видео](using-the-video-display-controls.md).

В отличие от микширования видео (VMR), ЕВР не имеет рабочих режимов (оконных, безоконных и т. д.). В частности:

-   Евр не поддерживает оконный режим. Приложение должно предоставить окно обрезки.
-   Евр не имеет режима без отрисовки. Чтобы заменить выступающий по умолчанию, вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   Евр не имеет режима смешения. Евр всегда создает микшер. Если у вас есть один входной поток, нет необходимости вызывать [**сетнумберофстреамс**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) , чтобы заставить Евр использовать микшер.

## <a name="filter-interfaces"></a>Интерфейсы фильтра

Фильтр Евр предоставляет следующие интерфейсы. некоторые из этих интерфейсов описаны в пакете SDK для DirectShow. Используйте **QueryInterface** для получения указателей на эти интерфейсы:

-   [**Иамцертифиедаутпутпротектион**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**Иамфилтермискфлагс**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**Ибасефилтер**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**иеврфилтерконфиг**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**Икспропертисет**](../directshow/ikspropertyset.md) (DirectShow)
-   [**Имедиаевентсинк**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**имфвидеопоситионмаппер**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**имфвидеорендерер**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**Икуалитиконтрол**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**Икуалпроп**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **испеЦифипропертипажес**

## <a name="input-pin-interfaces"></a>Интерфейсы входных закрепления

Входные контакты в фильтре Евр предоставляют следующие интерфейсы. Используйте **QueryInterface** для получения указателей на эти интерфейсы:

-   [**иеврвидеостреамконтрол**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**Имеминпутпин**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**Ипин**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**Икуалитиконтрол**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Кроме того, можно использовать интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) для получения следующего интерфейса:

-   [**идиректксвидеомемориконфигуратион**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Улучшенный модуль подготовки видео](enhanced-video-renderer.md)
</dt> </dl>

 

 
