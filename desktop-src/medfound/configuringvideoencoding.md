---
description: Настройка кодирования видео
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Настройка кодирования видео (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143201"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Настройка кодирования видео (Microsoft Media Foundation)

Чтобы настроить кодировщик видео, выполните следующие действия.

1.  Задайте любые свойства в кодировщике DMO с помощью **ипропертибаг:: Write**. В следующем списке приводится список минимального набора свойств, необходимых для кодирования видеопотока CBR (все эти значения могут использоваться по умолчанию):

    -   Свойство[мфпкэй \_ видеовиндов](mfpkey-videowindowproperty.md) указывает окно буфера, используемое для потока. Дополнительные сведения о параметре окна буфера и его влиянии на содержимое см. в разделе [методы кодирования](encodingmethods.md). Окно буфера по умолчанию — три секунды, что подходит для многих сценариев.
    -   Сложность видео задается для определения компромисса между качеством закодированного содержимого и временем, необходимым для кодирования. Если значение не задано, используется значение по умолчанию. Однако рекомендованные режимы для конкретного кодека можно найти, вызвав [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) для получения g \_ всзвмвккомплекситексливе, g \_ всзвмвккомплекситексоффлине и g \_ всзвмвккомплекситексмакс. Затем можно задать для параметра [мфпкэй \_ комплекситекс](mfpkey-complexityexproperty.md) значение от 0 до сообщаемой максимальной сложности.
    -   [Мфпкэй \_ ЧЕТКОе](mfpkey-crispproperty.md) указывает относительную важность сглаживания видео и качество изображения закодированных кадров. В большинстве случаев значение по умолчанию работает нормально.
    -   Для содержимого видео, хранящегося в контейнере, отличном от ASF, свойство [мфпкэй \_ асфоверхеадперфраме](mfpkey-asfoverheadperframeproperty.md) должно иметь значение 0. Это значение не является значением по умолчанию.

    Сведения о настройке потоков с VBR см. [в разделе Использование кодирования VBR](usingvbrencoding.md).

2.  Настройте структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) для типа входных данных или, если вы используете Media Foundation SDK, используйте функцию [**мфинитмедиатипефромвидеоинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Используйте структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , описывающую несжатое входное содержимое. Кодек не изменяет размер видео или не преобразует цветовое пространство.
3.  Задайте тип входных данных с помощью [**имедиаобжект:: сетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) или [**Имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Настройте тип выходных данных для кодировщика. После установки входного типа кодировщик перечисляет типы выходных данных, которые завершаются, за исключением элемента **двбитрате** структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или атрибута с [**\_ \_ средним \_ скоростью MF MT**](mf-mt-avg-bitrate-attribute.md) в интерфейсе [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Если перед настройкой входного типа получен тип вывода, то у доставленной структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) не будет связанного **видеоинфохеадер**.
5.  Извлеките частные данные кодека и добавьте их в структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , которая передается в структуру [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) или в [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype). Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).
6.  Задайте тип выходных данных, вызвав метод [**имедиаобжект:: сетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) или [**Имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Либо передайте [**структуру \_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) с завершенной структурой [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (включая добавленные закрытые данные), на которую ссылается член **пбформат** , либо создайте [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , вызвав [**мфинитмедиатипефромвидеоинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> Объект кодировщика видео поддерживает два выхода. Второй выход предназначен для кодировщика "POST View". Он предоставляет несжатые образцы, так как они будут доставлены из декодера. Это позволяет отслеживать качество кодирования, не дожидаясь обработки всего потока. Эти выходные данные являются необязательными. Если вы хотите использовать его, настройте его тип, который следует за тем же процессом, который использовался для задания типа входных данных кодировщика.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 
