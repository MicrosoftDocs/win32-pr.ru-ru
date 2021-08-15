---
description: использование категории изображений Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: использование категории изображений Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972633"
---
# <a name="using-the-windows-media-video-91-image-category"></a>использование категории изображений Windows Media Video 9,1

категория изображений Windows media video 9,1 отличается от других категорий вывода, поддерживаемых кодировщиком и декодером Windows media video 9. Вместо обработки несжатого видео он принимает специальные образцы, состоящие из структурированных данных преобразования и, иногда, растровых изображений RGB, на которых выполняются преобразования.

содержимое закодированного Windows media video 9,1 практически идентично содержимому обычного Windows содержимого в кодировке media видео 9, но определяется его собственным FOURCC ("вмвп").

тип выходных данных кодировщика для видеоизображения задается точно так же, как стандартный Windows Media video, за исключением того, что для параметров подтипа и сжатия должны быть заданы идентификаторы изображений видео. Это включает в себя необходимость получить частные данные кодека и добавить их в структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Дополнительные сведения см. в разделе [Настройка кодирования видео](configuringvideoencoding.md).

Конфигурация входного типа для видеоизображения также очень похожа на входную конфигурацию для других видеокодировщиков. вы можете получить частично завершенный [**DMO \_ \_ тип носителя**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) из кодировщика, вызвав [**имедиаобжект:: жетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), или, если вы используете Media Foundation SDK, вызвав [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) и извлекая **\_ \_ тип носителя DMO** с помощью [**мфкреатеаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Затем вы устанавливаете размер фрейма и структуру формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) так же, как и для стандартного видео. Как и в случае с типом выходных данных, необходимо убедиться, что подтипы и значения сжатия заданы соответствующим образом.

## <a name="creating-input-samples"></a>Создание примеров входных данных

Примеры входных данных для кодека видеоизображения структурированы. определение структуры и констант, используемых для изображения видео, не включается в интерфейсы видеокодеков Windows Media Audio и video. эти определения включены в пакет sdk для Windows media format, и их использование полностью описано в документации пакета sdk для Windows media format.

## <a name="decoding"></a>Декодирование

Не существует специальных требований для декодирования видео снимка экрана. в отличие от другого подтипа (медиасубтипе \_ вмвп), используемого для ввода декодера, поток сжатого видеоизображения по сути идентичен стандартному потоку Windows Media video.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
