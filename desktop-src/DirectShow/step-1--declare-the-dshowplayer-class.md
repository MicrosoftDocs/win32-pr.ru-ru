---
description: В этом разделе приводится шаг 1 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: Шаг 1. объявление класса Дшовплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02cbf35e9c71df9d71ab3df7cdbb3edf5d3f25bb5e77a01734f7d842fc3097f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951893"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>Шаг 1. объявление класса Дшовплайер

В этом разделе приводится шаг 1 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). полный код приведен в разделе [пример воспроизведения DirectShow](directshow-playback-example.md).

в этом руководстве `DShowPlayer` класс управляет всеми функциональными возможностями DirectShow. Этот класс объявлен как фоловс.


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





Примечания.

-   `PlaybackState`Перечисление описывает текущее состояние `DShowPlayer` объекта.
-   Событие с константой WM \_ Graph \_ определяет сообщение частного окна. Это сообщение используется для уведомления приложения о событиях графа фильтра. см. раздел [Step 6: Handle Graph events](step-6--handle-graph-events.md).
-   `GraphEventFN` является указателем на функцию обратного вызова для обработки событий графа фильтра. Приложение реализует эту функцию обратного вызова.
-   переменная-член *m \_ пвидео* предоставляет оболочку для различных DirectShow модулей подготовки видео. См. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).
-   В рамках этого руководства функция [саферелеасе](../medfound/saferelease.md) используется для освобождения указателей на COM-интерфейсах.

Далее. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
