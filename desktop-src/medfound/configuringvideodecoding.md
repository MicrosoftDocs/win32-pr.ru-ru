---
description: Настройка декодирования видео
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Настройка декодирования видео (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035342"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Настройка декодирования видео (Microsoft Media Foundation)

Декодирование по сути является противоположностью кодировки в плане конфигурации. Декодер поддерживает очень мало свойств, и ни один из них не требуется. Установите тип входных данных в тип, используемый для выходных данных декодера (включая частные данные кодека). Затем задайте для выходных данных нужный формат без сжатия, задайте структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , отражающую правильный размер кадра, и начните обработку образцов.

Необходимо предоставить декодеру тип мультимедиа, содержащий частные данные кодека, расположенные непосредственно после структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Декодер не может декодировать содержимое без этих данных. Проверка формата, выполняемая декодером, не проверяет личные данные. Если частные данные кодека отсутствуют или неверны, декодер реагирует как на повреждение потока. Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование личных данных видеокодека](usingvideocodecprivatedata.md)
</dt> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
