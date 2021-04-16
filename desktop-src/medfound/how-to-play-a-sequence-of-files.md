---
description: В этом разделе описывается воспроизведение последовательности аудио-и видеофайлов с помощью Мфплай.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Как воспроизвести последовательность файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650688"
---
# <a name="how-to-play-a-sequence-of-files"></a>Как воспроизвести последовательность файлов

\[Мфплай доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. \]

В этом разделе описывается воспроизведение последовательности аудио-и видеофайлов с помощью Мфплай.


В разделе [Начало работы with мфплай](getting-started-with-mfplay.md) показано, как воспроизвести один файл мультимедиа. Можно также использовать Мфплай для воспроизведения последовательности файлов.

### <a name="synchronous-blocking-method"></a>Синхронный (блокирующий) метод

1.  Вызовите метод [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . Метод создает элемент мультимедиа.
2.  Вызовите [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) , чтобы поставить в очередь элемент мультимедиа для воспроизведения.
3.  Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать воспроизведение.

Эти действия показаны в следующем коде.


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



Метод [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) принимает следующие параметры:

-   Первый параметр — это URL-адрес файла.
-   Второй параметр указывает, блокируется ли метод. Указание значения **true**, как показано здесь, приводит к тому, что метод блокируется до создания элемента мультимедиа.
-   Третий параметр связывает произвольное значение **типа \_ DWORD** с элементом мультимедиа. Это значение можно получить позже, вызвав [**имфпмедиаитем:: UserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   Четвертый параметр получает указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) элемента мультимедиа.

### <a name="asynchronous-non-blocking-method"></a>Асинхронный (не блокирующий) метод

Избегайте параметра блокировки при вызове [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) из потока пользовательского интерфейса, так как для выполнения может потребоваться значительное время. Метод обычно открывает файл или сетевое подключение и считывает достаточно данных для анализа заголовков файлов, все из которых может занять некоторое время. Поэтому, как правило, лучше установить для второго параметра значение **false**. Этот параметр приводит к асинхронному выполнению метода. При использовании асинхронного параметра последний параметр должен иметь **значение NULL**:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



При создании элемента мультимедиа приложение получает событие **МФП \_ event \_ Type \_ MEDIAITEM \_ Created** . Структура данных для этого события содержит указатель на элемент мультимедиа. Передайте этот указатель методу [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) , чтобы поставить в очередь элемент для воспроизведения.


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a>Требования

Для Мфплай требуется Windows 7.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



