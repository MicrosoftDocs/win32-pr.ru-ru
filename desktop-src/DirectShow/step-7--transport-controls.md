---
description: В этом разделе приводится шаг 7 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: Шаг 7. элементы управления транспорта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684124"
---
# <a name="step-7-transport-controls"></a><span data-ttu-id="7de00-103">Шаг 7. элементы управления транспорта</span><span class="sxs-lookup"><span data-stu-id="7de00-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="7de00-104">В этом разделе приводится шаг 7 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="7de00-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="7de00-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="7de00-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="7de00-106">Последним шагом является добавление элементов управления транспорта (воспроизведение, пауза и остановка).</span><span class="sxs-lookup"><span data-stu-id="7de00-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="7de00-107">Чтобы воспроизвести файл, вызовите [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span><span class="sxs-lookup"><span data-stu-id="7de00-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



<span data-ttu-id="7de00-108">Чтобы приостановить, вызовите [**имедиаконтрол::P Аусе**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span><span class="sxs-lookup"><span data-stu-id="7de00-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



<span data-ttu-id="7de00-109">Чтобы прерывать работу, вызовите [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="7de00-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7de00-110">См. также</span><span class="sxs-lookup"><span data-stu-id="7de00-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7de00-111">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="7de00-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="7de00-112">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="7de00-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="7de00-113">Фильтрация состояний</span><span class="sxs-lookup"><span data-stu-id="7de00-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 



