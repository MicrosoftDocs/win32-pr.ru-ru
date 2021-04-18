---
description: Настройка декодирования видео
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Настройка декодирования видео (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701326"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Настройка декодирования видео (Microsoft Media Foundation)

Декодирование по сути является противоположностью кодировки в плане конфигурации. Декодер поддерживает очень мало свойств, и ни один из них не требуется. Установите тип входных данных в тип, используемый для выходных данных декодера (включая частные данные кодека). Затем задайте для выходных данных нужный формат без сжатия, задайте структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , отражающую правильный размер кадра, и начните обработку образцов.

Необходимо предоставить декодеру тип мультимедиа, содержащий частные данные кодека, расположенные непосредственно после структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Декодер не может декодировать содержимое без этих данных. Проверка формата, выполняемая декодером, не проверяет личные данные. Если частные данные кодека отсутствуют или неверны, декодер реагирует как на повреждение потока. Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование личных данных видеокодека](usingvideocodecprivatedata.md)
</dt> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
