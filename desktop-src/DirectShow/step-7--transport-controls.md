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
# <a name="step-7-transport-controls"></a>Шаг 7. элементы управления транспорта

В этом разделе приводится шаг 7 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).

Последним шагом является добавление элементов управления транспорта (воспроизведение, пауза и остановка). Чтобы воспроизвести файл, вызовите [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).


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



Чтобы приостановить, вызовите [**имедиаконтрол::P Аусе**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).


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



Чтобы прерывать работу, вызовите [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Пример воспроизведения DirectShow](directshow-playback-example.md)
</dt> <dt>

[Фильтрация состояний](filter-states.md)
</dt> </dl>

 

 



