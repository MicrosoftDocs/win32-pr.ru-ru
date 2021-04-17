---
description: В этом разделе описывается использование аудио-и видеоэффектов с Мфплай.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Как добавить аудио или видео эффекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711799"
---
# <a name="how-to-add-audio-or-video-effects"></a>Как добавить аудио или видео эффекты

\[Мфплай доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. \]

В этом разделе описывается использование аудио-и видеоэффектов с Мфплай.

Чтобы использовать действие с Мфплай, этот результат должен быть реализован в виде Media Foundation преобразования (MFT). Дополнительные сведения см. в разделе [преобразования Media Foundation](media-foundation-transforms.md).

**Добавление звуковых эффектов или видео**

1.  Создайте экземпляр файла MFT, который реализует этот результат.
2.  Вызовите [**имфпмедиаплайер:: инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Вызовите [**инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) перед открытием файла мультимедиа для воспроизведения. Мфплай автоматически определяет, является ли это действие видеороликом или звуковым действием.

Метод [**инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) также принимает логический параметр, указывающий, является ли результат необязательным или обязательным. Если Мфплай не может добавить требуемый результат (например, из-за несовместимости формата потока), возникает ошибка воспроизведения. В большинстве случаев лучше задать необязательный результат.

Мфплай продолжит использовать этот результат для всех последующих воспроизведений. Чтобы удалить этот результат, вызовите [**имфпмедиаплайер:: ремовиффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) или [**Имфпмедиаплайер:: ремовеаллеффектс**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a>Требования

Для Мфплай требуется Windows 7.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



