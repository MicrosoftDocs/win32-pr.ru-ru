---
description: В этом разделе описывается использование Мфплай для предварительного просмотра видео из видеокамеры.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Предварительный просмотр видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711385"
---
# <a name="video-preview"></a>Предварительный просмотр видео

\[Мфплай доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. \]

В этом разделе описывается использование Мфплай для предварительного просмотра видео из видеокамеры.

Мфплай предоставляет самый простой способ Microsoft Media Foundation для предварительного просмотра видео с устройства записи. Мфплай следует использовать, если выполняются следующие условия.

-   Записывать видео в файл не нужно.
-   Точный контроль над отображением видео не требуется. (Например, не нужно управлять созданием устройства Direct3D.)
-   Перед отрисовкой не нужно обрабатывать видеоданные с камеры.

В противном случае [средство чтения исходного кода](source-reader.md) может быть лучшим вариантом.

Чтобы использовать Мфплай с устройством видеозаписи, выполните следующие действия.

1.  Создайте источник мультимедиа для устройства записи. См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).
2.  Вызовите [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) , чтобы создать экземпляр объекта Player.
3.  Вызовите метод [**имфпмедиаплайер:: креатемедиаитемфромобжект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) . Передайте указатель на интерфейс Имфмедиасаурце источника мультимедиа. Метод получает указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .
4.  Вызовите [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать предварительный просмотр.

В следующем коде показаны следующие шаги.


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



В типичном приложении необходимо предоставить указатель на интерфейс обратного вызова в функции [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) и использовать интерфейс обратного вызова для получения событий от проигрывателя. Для простоты показанный здесь код пропускает эти шаги. Дополнительные сведения см. [в разделе Начало работы with мфплай](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Завершение работы

Перед завершением работы приложения завершите работу источника мультимедиа и объекта Player следующим образом:

1.  Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа.
2.  Вызовите метод [**имфпмедиаплайер:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) в объекте Player.


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a>Требования

Для Мфплай требуется Windows 7.

## <a name="related-topics"></a>См. также

<dl> <dt>

[мфплай](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Видеозапись](audio-video-capture.md)
</dt> </dl>

 

 



