---
description: В этом разделе описывается шаг 1 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: Шаг 1. объявление класса Дшовплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673995"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="1fd50-103">Шаг 1. объявление класса Дшовплайер</span><span class="sxs-lookup"><span data-stu-id="1fd50-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="1fd50-104">В этом разделе описывается шаг 1 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="1fd50-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="1fd50-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="1fd50-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="1fd50-106">В этом руководстве `DShowPlayer` класс управляет всеми функциями DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1fd50-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="1fd50-107">Этот класс объявлен как фоловс.</span><span class="sxs-lookup"><span data-stu-id="1fd50-107">This class is declared as folows.</span></span>


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





<span data-ttu-id="1fd50-108">Примечания.</span><span class="sxs-lookup"><span data-stu-id="1fd50-108">Notes:</span></span>

-   <span data-ttu-id="1fd50-109">`PlaybackState`Перечисление описывает текущее состояние `DShowPlayer` объекта.</span><span class="sxs-lookup"><span data-stu-id="1fd50-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="1fd50-110">Событие с константой WM \_ Graph \_ определяет сообщение частного окна.</span><span class="sxs-lookup"><span data-stu-id="1fd50-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="1fd50-111">Это сообщение используется для уведомления приложения о событиях графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="1fd50-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="1fd50-112">См. [Шаг 6. Работа с событиями графа](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="1fd50-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="1fd50-113">`GraphEventFN` является указателем на функцию обратного вызова для обработки событий графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="1fd50-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="1fd50-114">Приложение реализует эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1fd50-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="1fd50-115">Переменная-член *m \_ пвидео* предоставляет оболочку для различных модулей подготовки видео DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1fd50-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="1fd50-116">См. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1fd50-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="1fd50-117">В рамках этого руководства функция [саферелеасе](../medfound/saferelease.md) используется для освобождения указателей на COM-интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="1fd50-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="1fd50-118">Далее. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1fd50-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd50-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1fd50-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd50-120">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1fd50-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
