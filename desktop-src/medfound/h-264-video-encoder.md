---
description: 'Кодировщик видео Microsoft Media Foundation H. 264 — это преобразование Media Foundation, которое поддерживает следующие профили H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Кодировщик видео H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467531"
---
# <a name="h264-video-encoder"></a>Кодировщик видео H. 264

Кодировщик видео Microsoft Media Foundation H. 264 — это [преобразование Media Foundation](media-foundation-transforms.md) , которое поддерживает следующие профили H. 264:

-   Базовый профиль
-   Профиль Main
-   Высокий профиль (требуется Windows 8)

Кодировщик видео H. 264 предоставляет следующие интерфейсы:

-   [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Типы входных данных

Входной тип носителя должен иметь один из следующих подтипов:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).

Тип выходных данных должен быть задан перед входным типом. Пока тип выходных данных не задан, метод [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) кодировщика возвращает **MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Типы вывода

Кодировщик поддерживает один выходной подтип:

-   **MFVideoFormat_H264**

Задайте следующие атрибуты для выходного типа носителя.




| attribute | Описание | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Основной тип. Необходимо <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Подтип видео. Необходимо <strong>MFVideoFormat_H264</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Средняя скорость кодирования (бит в секунду). Должен быть больше нуля. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Частота кадров. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Размер кадра. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Режим чередования. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | Профиль кодирования H. 264.<br /> Поддерживаются такие значения:<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (по умолчанию)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (требуется Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Необязательный элемент. Задает уровень кодирования H. 264.<br /> Значение по умолчанию равно – 1, что означает, что кодировщик выбирает уровень кодирования.<br /> Не рекомендуется задавать уровень в типе носителя и разрешать кодировщику выбирать уровень. Кодировщик может наследовать соответствующий уровень для данного видеопотока, учитывая ограничения формата и характеристики видео. Дополнительные сведения об ограничениях профиля и уровня см. в приложении A из ITU-T H. 264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Необязательный элемент. Задает пропорцию в пикселях. Значение по умолчанию — 1:1. | 




 

После установки типа выходных данных кодировщик видео обновляет тип, добавляя атрибут [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) . Этот атрибут содержит заголовок последовательности.

## <a name="codec-properties"></a>Свойства кодека

Кодировщик H. 264 реализует интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) для установки параметров кодирования. Он поддерживает следующие свойства:

Требования к кодеку для ХКК кодировщика см. в разделе " **сертифицированный аппаратный кодировщик** " ниже.

в Windows 7 поддерживаются следующие свойства.



| Свойство                                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Задает режим управления скоростью. См. заметки. Режим по умолчанию — это неограниченная переменная с битовой скоростью (VBR).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Задает уровень качества. Это свойство применяется, когда режим управления скоростью имеет значение VBR на основе качества (**eAVEncCommonRateControlMode_Quality**). Допустимый диапазон: 1 – 100. Значение по умолчанию — 70. <br/> Чтобы задать этот параметр, задайте свойство перед вызовом [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> чтобы задать этот параметр в Windows 7, задайте свойство перед вызовом [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Кодировщик игнорирует изменения после установки типа выходных данных. <br/> в Windows 8 это свойство можно задать в любое время во время кодирования. Изменения применяются, начиная со следующего входного кадра. <br/> Внутренне кодировщик преобразует это свойство в значение [авенквидеоенкодекп](codecapi-avencvideoencodeqp.md) . <br/> |



 

Для следующих свойств требуется Windows 8.




| Свойство | Описание | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Задает режим адаптивной кодировки. Кодировщик H. 264 поддерживает следующие режимы в Windows 8:<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Адаптивная кодировка отсутствует. (по умолчанию).</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Адаптивное изменение частоты кадров.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Задает размер буфера (в байтах) для кодирования с постоянной скоростью (CBR).<br /> Допустимый диапазон: [1... 2 ³ ² – 1]. <br /> Требуется Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Для кодирования с ограниченным числом VBR указывает скорость, с которой происходит сток "поврежденных сегментов", в битах в секунду. Это свойство применяется, когда режим управления скоростью <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br /> Допустимый диапазон: [1... 2 ³ ² – 1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Задает среднюю скорость потока в битах в секунду. Это свойство не учитывается, если режим управления скоростью имеет значение <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> Допустимый диапазон: [1... 2 ³ ² – 1]. <br /> В режимах CBR и неограниченных VBR средняя скорость определяет конечный размер файла. В режиме CBR средняя скорость потока — это также скорость, с которой сжатые биты преобразуются из "сегмента утечки". (Дополнительные сведения см. <a href="the-leaky-bucket-buffer-model.md">в разделе Модель буфера для сегмента утечки</a>.) <br /> в Windows 7 средняя скорость потока определяется атрибутом <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> для типа носителя. <br /> в Windows 8 можно задать среднюю скорость потока с помощью атрибута <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> или свойства <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> . Если заданы оба значения, CODECAPI_AVEncCommonMeanBitRate переопределений. в Windows 8 можно задать среднюю скорость потока во время кодирования. При изменении частоты разрядов кодировщик использует адаптивную кодировку.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Задает компромисс качества и скорости. Допустимый диапазон:<ul><li>0 – 33: низкая сложность</li><li>34 – 66: средняя сложность (по умолчанию)</li><li>67 – 100: высокая сложность</li></ul><br /> Это значение влияет на то, как кодировщик выполняет различные операции кодирования, такие как компенсация движения. На более высоких уровнях сложности кодировщик работает медленнее, но обеспечивает лучшее качество с той же скоростью.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Включает или отключает кабак (Адаптивное двоичное арифметическое кодирование) для H. 264-кода энтропии. Значение по умолчанию — <strong>VARIANT_FALSE</strong>. <br /> Кабак не используется для базового профиля.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Задает значение <strong>seq_parameter_set_id</strong> в ЕДИНИЦЕ SPS NAL для H. 264 битовый поток. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Задает максимальное число последовательных кадров B в выходном битовый поток. Допустимые значения:<ul><li>0: не использовать кадры B (по умолчанию).</li><li>1. Используйте один кадр B.</li><li>2: используйте два кадра B.</li></ul>Чтобы задать этот параметр, задайте свойство перед вызовом <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>имфтрансформ:: сетаутпуттипе</strong></a>. <br /> Для базового профиля число кадров B всегда равно нулю. Кодировщик будет переопределять ненулевые значения.<br /> Для других профилей H. 264, если это свойство не равно нулю, шаблон кодировки — ИББПББП, где максимальное число последовательных кадров B равно <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Задает число изображений из одного заголовка GOP к следующему, включая начальную привязку, но не следующую. <br /> Допустимый диапазон: [0... 2 ³ ² – 1]. Если значение равно нулю, кодировщик выбирает размер GOP. Значение по умолчанию равно нулю. <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Задает число рабочих потоков, используемых кодировщиком.<br /> Допустимый диапазон — 0 – 16. Если значение равно нулю, кодировщик выбирает число потоков. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Указывает тип видеосодержимого.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Допустимый диапазон: 16 – 51. Значение по умолчанию — 24. <br /> Это свойство применяется, когда режим управления скоростью <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> Это свойство настраивает тот же параметр кодировки, что и <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>авенккоммонкуалити</strong></a>. Однако <a href="codecapi-avencvideoencodeqp.md">авенквидеоенкодекп</a> позволяет приложению напрямую ЗАДАВАТЬ значение QP. Если заданы оба свойства, Авенквидеоенкодекп переопределяет. <br /> Значение по умолчанию, равное 24, соответствует значению по умолчанию 70 для параметра <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>авенккоммонкуалити</strong></a> .<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Заставляет кодировщик кодировать следующий кадр как ключевой кадр.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Допустимый диапазон: 0 – 51. Значение по умолчанию — 0. <br /> Это свойство применяется ко всем режимам управления скоростью. Кодировщик не должен создавать значение QP ниже, чем указано в свойстве <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Включает или отключает режим низкой задержки. См. раздел «многопоточность» в разделе «Примечания».<br /> | 




 

## <a name="remarks"></a>Комментарии

Кодировщик поддерживает следующие режимы управления скоростью.



| Режим                                  | Константа                                            | Описание                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Постоянная скорость (CBR)               | **eAVEncCommonRateControlMode_CBR**                | Кодировщик пытается достичь постоянной скорости потока, используя модель "сегмент утечки". Целевая скорость потока задается свойством [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . <br/> Требуется Windows 8. <br/> |
| Переменная с ограничением скорости (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | Кодировщик использует модель "сегмент утечки" с пиковой скоростью. Скорость очистки для сегмента утечки задается свойством [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) . <br/> Требуется Windows 8. <br/>     |
| Битовая скорость переменной на основе качества (VBR) | **eAVEncCommonRateControlMode_Quality**            | Кодировщик пытается достичь постоянного уровня качества, заданного свойством [**авенккоммонкуалити**](../directshow/avenccommonquality-property.md) .                                                                                                           |
| Неограниченная VBR                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | Кодировщик пытается достичь скорости назначения, заданной атрибутом [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) в выходном типе носителя. Это режим по умолчанию.                                                              |



 

Для CBR и режима с ограничением VBR требуется Windows 8.

в Windows 8 кодировщик устанавливает следующие атрибуты в выходных данных:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> предыдущая версия документации неправильно объявила, что кодировщик поддерживается на Windows Server 2008 R2.

 

### <a name="multithreading"></a>Многопоточность

в Windows 8 кодировщик поддерживает два режима кодирования:

-   **Кодирование фрагмента.** В этом режиме срезы кодируются параллельно. Каждый срез кодируется в другом потоке. Этот режим имеет низкую задержку, так как один рисунок кодируется параллельно. Однако этот подход не масштабируется по мере увеличения числа ядер, так как количество срезов ограничено количеством макроблокк строк во входном изображении.
-   **Многокадровая кодировка.** В этом режиме кодировщик принимает несколько кадров входных данных и кодирует их параллельно. Этот режим лучше масштабируется в многоядерной среде, но в нем появились дополнительные задержки.

Кодировщик по умолчанию кодирует кодирование, чтобы максимально сокращать задержку. Чтобы включить многокадровое кодирование, задайте для свойства [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) значение **VARIANT_FALSE**.

Чтобы задать число рабочих потоков, используемых кодировщиком, задайте свойство [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .

в Windows 7 кодировщик всегда использует кодирование среза.

### <a name="certified-hardware-encoder"></a>Сертифицированный аппаратный кодировщик

Если имеется сертифицированный аппаратный кодировщик, он обычно используется вместо кодировщика системы входящей почты для Media Foundation связанных сценариев. Сертифицированные кодировщики требуются для поддержки определенного набора свойств **икодекапи** и могут дополнительно поддерживать другой набор свойств. Процесс сертификации должен гарантировать, что требуемые свойства должным образом поддерживались, и, если необязательное свойство поддерживается, оно также должно поддерживаться надлежащим образом.

Ниже приведен набор обязательных и необязательных свойств **икодекапи** для кодировщиков, которые проходят сертификацию кодировщика ХКК.

требуются следующие свойства Windows 8 и Windows 8.1 **икодекапи** :

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

следующие свойства Windows 8.1 **икодекапи** являются необязательными, но проверяются в хкк, если они поддерживаются.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (динамический)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

следующие свойства Windows 8 и Windows 8.1 **икодекапи** являются необязательными, но проверяются в хкк, если они поддерживаются.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (статический)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Следующие свойства **икодекапи** являются необязательными. Они не проверяются в ХКК.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                               |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Поддержка MPEG-4 в Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> </dl>

 

 
