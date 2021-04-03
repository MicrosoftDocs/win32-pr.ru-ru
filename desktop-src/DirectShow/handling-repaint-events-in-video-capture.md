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
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="2de1b-103">Обработка событий перерисовки в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2de1b-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="2de1b-104">Если вы создаете граф видеозаписи без использования интерфейса [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) и выполняете предварительный просмотр видео с помощью старого фильтра модуля подготовки отчетов, следует переопределить обработку по умолчанию для событий [**\_ перерисовки EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="2de1b-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="2de1b-105">Запросите диспетчер графа фильтров для интерфейса [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) и вызовите метод [**Имедиаевент:: КАНЦЕЛДЕФАУЛСАНДЛИНГ**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) со значением EC \_ repain:</span><span class="sxs-lookup"><span data-stu-id="2de1b-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="2de1b-106">Это предотвращает возможную ошибку, которая может привести к повреждению файла записи.</span><span class="sxs-lookup"><span data-stu-id="2de1b-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="2de1b-107">Если пользователь покрывает и обнаруживает окно предварительного просмотра, фильтр модуля подготовки отчетов получает \_ сообщение WM Paint.</span><span class="sxs-lookup"><span data-stu-id="2de1b-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="2de1b-108">По умолчанию модуль подготовки отчетов запрашивает новый кадр, а диспетчер графа фильтров приостанавливает граф, чтобы задержать еще один кадр видео.</span><span class="sxs-lookup"><span data-stu-id="2de1b-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="2de1b-109">Если это происходит во время записи файла графа, файл будет поврежден.</span><span class="sxs-lookup"><span data-stu-id="2de1b-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="2de1b-110">Переопределение \_ поведения ПЕРЕрисовки EC по умолчанию не потребует от модуля подготовки запроса нового кадра.</span><span class="sxs-lookup"><span data-stu-id="2de1b-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="2de1b-111">Вам не нужно выполнять этот шаг, если вы используете интерфейс **ICaptureGraphBuilder2** , так как построитель диаграмм для записи делает это автоматически.</span><span class="sxs-lookup"><span data-stu-id="2de1b-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="2de1b-112">Кроме того, не требуется, если для предварительного просмотра используется модуль подготовки видео (VMR).</span><span class="sxs-lookup"><span data-stu-id="2de1b-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="2de1b-113">VMR всегда имеет последний доступный кадр, поэтому он не отправляет \_ события ПЕРЕрисовки EC.</span><span class="sxs-lookup"><span data-stu-id="2de1b-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2de1b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2de1b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de1b-115">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="2de1b-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="2de1b-116">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="2de1b-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



