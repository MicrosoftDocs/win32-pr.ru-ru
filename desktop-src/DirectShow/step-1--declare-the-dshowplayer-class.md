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
# <a name="step-1-declare-the-dshowplayer-class"></a>Шаг 1. объявление класса Дшовплайер

В этом разделе описывается шаг 1 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).

В этом руководстве `DShowPlayer` класс управляет всеми функциями DirectShow. Этот класс объявлен как фоловс.


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
-   Событие с константой WM \_ Graph \_ определяет сообщение частного окна. Это сообщение используется для уведомления приложения о событиях графа фильтра. См. [Шаг 6. Работа с событиями графа](step-6--handle-graph-events.md).
-   `GraphEventFN` является указателем на функцию обратного вызова для обработки событий графа фильтра. Приложение реализует эту функцию обратного вызова.
-   Переменная-член *m \_ пвидео* предоставляет оболочку для различных модулей подготовки видео DirectShow. См. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).
-   В рамках этого руководства функция [саферелеасе](../medfound/saferelease.md) используется для освобождения указателей на COM-интерфейсах.

Далее. [Шаг 2. объявление квидеорендерер и производных классов](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
