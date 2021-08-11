---
description: Важное значение устарело.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Пример MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241739"
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

этот пример доступен в [репозитории github для классических примеров Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
