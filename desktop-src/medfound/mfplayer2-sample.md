---
description: Важное значение устарело.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Пример MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898198"
---
# <a name="mfplayer2-sample"></a>Пример MFPlayer2

> [!IMPORTANT]
> Не рекомендуется. Этот API может быть удален из будущих выпусков Windows. Приложения должны использовать [сеанс мультимедиа](media-session.md) для воспроизведения.

 

Демонстрирует некоторые функции воспроизведения, пропущенные в примере [симплеплай](simpleplay-sample.md) , например:

-   Нужна
-   Rate-управление (Быстрая перемотка вперед и назад)
-   Громкость звука и звуковые элементы управления
-   Масштаб видео

На следующем рисунке показаны элементы управления, используемые для этих функций.

![снимок экрана образца мфплайер ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие API-интерфейсы.

-   [**иаудиосессионконтрол**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**иаудиосессионманажер**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**иммдевице**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**иммдевицеенумератор**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**исимплеаудиоволуме**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
