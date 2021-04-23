---
description: В этом разделе содержится код руководства по воспроизведению аудио-и видеороликов в DirectShow.
ms.assetid: 8cf0f281-3680-4329-80d0-8282d1051c1a
title: воспроизведение. h
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03bd6ebd1d0b37c0351fbbe1b4e7906b243ffc7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805230"
---
# <a name="playbackh"></a><span data-ttu-id="66d5d-103">воспроизведение. h</span><span class="sxs-lookup"><span data-stu-id="66d5d-103">playback.h</span></span>

<span data-ttu-id="66d5d-104">В этом разделе содержится код руководства по [воспроизведению аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="66d5d-104">This topic contains code for the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.

#pragma once

class CVideoRenderer;

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



## <a name="related-topics"></a><span data-ttu-id="66d5d-105">См. также</span><span class="sxs-lookup"><span data-stu-id="66d5d-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d5d-106">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="66d5d-106">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="66d5d-107">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="66d5d-107">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> </dl>

 

 



