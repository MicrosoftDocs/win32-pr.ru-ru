---
description: Использование категории изображений Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Использование категории изображений Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684780"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Использование категории изображений Windows Media Video 9,1

Категория изображений Windows Media Video 9,1 отличается от других категорий вывода, поддерживаемых кодировщиком и декодером Windows Media Video 9. Вместо обработки несжатого видео он принимает специальные образцы, состоящие из структурированных данных преобразования и, иногда, растровых изображений RGB, на которых выполняются преобразования.

Закодированное содержимое изображения Windows Media Video 9,1 практически идентично содержимому обычного закодированного содержимого Windows Media видео 9, но определяется его собственным FOURCC ("ВМВП").

Тип выходных данных кодировщика для видеоизображения задается точно так же, как и стандартное видео Windows Media, за исключением того, что для параметров подтипа и сжатия должны быть заданы идентификаторы изображений видео. Это включает в себя необходимость получить частные данные кодека и добавить их в структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Дополнительные сведения см. в разделе [Настройка кодирования видео](configuringvideoencoding.md).

Конфигурация входного типа для видеоизображения также очень похожа на входную конфигурацию для других видеокодировщиков. Вы можете получить частично завершенный [**\_ \_ тип мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) из кодировщика, вызвав [**имедиаобжект:: жетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), или, если вы используете Media Foundation SDK, вызвав [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) и извлекая **\_ \_ тип мультимедиа DMO** с помощью [**мфкреатеаммедиатипефроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Затем вы устанавливаете размер фрейма и структуру формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) так же, как и для стандартного видео. Как и в случае с типом выходных данных, необходимо убедиться, что подтипы и значения сжатия заданы соответствующим образом.

## <a name="creating-input-samples"></a>Создание примеров входных данных

Примеры входных данных для кодека видеоизображения структурированы. Определение структуры и констант, используемых для изображения видео, не включается в интерфейсы кодеков аудио и видео Windows Media. Эти определения включены в пакет SDK Windows Media Format, и их использование полностью описано в документации пакета SDK Windows Media Format.

## <a name="decoding"></a>Декодирование

Не существует специальных требований для декодирования видео снимка экрана. В отличие от другого подтипа (МЕДИАСУБТИПЕ \_ вмвп), используемого для ввода декодера, поток сжатого видеоизображения по сути идентичен стандартному потоку видео Windows Media.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
