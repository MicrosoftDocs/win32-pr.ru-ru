---
description: Обработка событий перерисовки в видеозаписи
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Обработка событий перерисовки в видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990253"
---
# <a name="handling-repaint-events-in-video-capture"></a>Обработка событий перерисовки в видеозаписи

Если вы создаете граф видеозаписи без использования интерфейса [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) и выполняете предварительный просмотр видео с помощью старого фильтра модуля подготовки отчетов, следует переопределить обработку по умолчанию для событий [**\_ перерисовки EC**](ec-repaint.md) . Запросите диспетчер графа фильтров для интерфейса [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) и вызовите метод [**Имедиаевент:: КАНЦЕЛДЕФАУЛСАНДЛИНГ**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) со значением EC \_ repain:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Это предотвращает возможную ошибку, которая может привести к повреждению файла записи. Если пользователь покрывает и обнаруживает окно предварительного просмотра, фильтр модуля подготовки отчетов получает \_ сообщение WM Paint. По умолчанию модуль подготовки отчетов запрашивает новый кадр, а диспетчер графа фильтров приостанавливает граф, чтобы задержать еще один кадр видео. Если это происходит во время записи файла графа, файл будет поврежден. Переопределение \_ поведения ПЕРЕрисовки EC по умолчанию не потребует от модуля подготовки запроса нового кадра.

Вам не нужно выполнять этот шаг, если вы используете интерфейс **ICaptureGraphBuilder2** , так как построитель диаграмм для записи делает это автоматически. Кроме того, не требуется, если для предварительного просмотра используется модуль подготовки видео (VMR). VMR всегда имеет последний доступный кадр, поэтому он не отправляет \_ события ПЕРЕрисовки EC.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



