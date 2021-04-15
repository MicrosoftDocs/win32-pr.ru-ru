---
description: В этом разделе описано, как создать топологию перекодирования в Топоедит.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Создание топологии перекодирования с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539638"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Создание топологии перекодирования с помощью Топоедит

В этом разделе описано, как создать топологию перекодирования в Топоедит.

> [!Note]  
> Для этого компонента требуется Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Создание топологии перекодирования

1.  В меню **файл** выберите команду **отобразить преобразование кода**.

2.  В диалоговом окне **Выбор источника носителя** выберите исходный файл для перекодировки.
3.  Нажмите кнопку **Открыть**.
4.  В диалоговом окне **Выбор профиля** для преобразования выберите один из профилей кодирования из раскрывающегося списка.
    > [!Note]  
    > Профили загружаются из файла TranscodeProfiles.xml.

     

5.  В диалоговом окне **Выбор целевого файла** выберите имя выходного файла.
6.  Топоедит создает топологию перекодирования и отображает узлы топологии в главном окне приложения.
7.  Нажмите кнопку **Воспроизведение** на панели инструментов, чтобы запустить сеанс мультимедиа. Дождитесь завершения кодирования.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

Топоедит загружает профили кодировки из файла TranscodeProfiles.xml. Этот файл находится в каталоге bin Windows SDK.

Файл начинается с элемента **тедтранскодепрофилес** . Каждый профиль начинается с элемента **тедтранскодепрофиле** . Каждый профиль состоит из набора значений формата `<VALUE_NAME Value="VALUE"/>` . Определены следующие значения:



| Значение                                                                                                                                                                                                    | Описание                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**аудиоавгбитесперсеконд**<br/>                                         | Среднее число байтов в секунду для аудиопотока. Эквивалентно [**\_ \_ среднему числу \_ \_ байтов \_ в \_ секунду**](mf-mt-audio-avg-bytes-per-second-attribute.md) в атрибуте MF.<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**аудиобитсперсампле**<br/>                                                         | Количество битов на выборку для аудиопотока. Эквивалентно [**\_ \_ звуковой бит MF \_ MT \_ на атрибут \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**аудиоблоккалигнмент**<br/>                                                     | Выравнивание блока для аудиопотока. Эквивалентно атрибуту [**\_ \_ \_ \_ выравнивания звукового блока MF MT**](mf-mt-audio-block-alignment-attribute.md) .<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**аудиоенкодингпрофиле**<br/>                                                 | Зависящее от кодека значение, определяющее звуковой профиль. Эквивалентно атрибуту [ \_ \_ ЕНКОДИНГПРОФИЛЕ, перекодированию MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**аудиоформат**<br/>                                                                                     | Закодированный звуковой подтип. Эквивалентно атрибуту [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**аудионумчаннелс**<br/>                                                                 | Число каналов в потоке аудио. Эквивалентно атрибуту [**MF \_ \_ Audio \_ NUM \_ channels**](mf-mt-audio-num-channels-attribute.md) .<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**аудиосамплесперсеконд**<br/>                                             | Частота дискретизации звукового потока в примерах в секунду. Эквивалентно [**\_ \_ аудио \_ выборки MF в \_ \_ секунду**](mf-mt-audio-samples-per-second-attribute.md) для атрибута.<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**контаинертипе**<br/>                                                                             | Тип контейнера файлов. Эквивалентно атрибуту [ \_ \_ КОНТАИНЕРТИПЕ, перекодированию MF](mf-transcode-containertype.md) . <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | Отображаемое имя профиля.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**скипметадататрансфер**<br/>                                                 | Укажите 1, если метаданные не должны передаваться в выходной файл, или 0, если необходимо передать метаданные. Эквивалентно [передаваемой атрибуту MF \_ \_ пропуска \_ метаданных \_ ](mf-transcode-skip-metadata-transfer.md) .<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**видеобитрате**<br/>                                                                                 | Средняя скорость видео. Эквивалентно атрибуту с [**\_ \_ средним \_ скоростью MF MT**](mf-mt-avg-bitrate-attribute.md) . <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**видеоенкодекомплексити**<br/>                                             | Зависящее от коде значение, определяющее качество кодирования. Эквивалентно атрибуту [ \_ \_ КУАЛИТИВССПИД, перекодированию MF](mf-transcode-qualityvsspeed.md) . <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**видеоенкодингпрофиле**<br/>                                                 | Зависящее от кодека значение, определяющее профиль видео. Эквивалентно атрибуту [ \_ \_ ЕНКОДИНГПРОФИЛЕ, перекодированию MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**видеоформат**<br/>                                                                                     | Подтип закодированного видео. Эквивалентно атрибуту [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**видеофрамехеигхт**<br/>                                                                 | Высота выходного видео. Эквивалентно атрибуту [**\_ \_ \_ размера пакета MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**видеофрамератеденоминатор**<br/>                             | Знаменатель частоты кадров выходного видео. Эквивалентно атрибуту [**\_ \_ \_ частоты кадров MF MT**](mf-mt-frame-rate-attribute.md) .<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**видеофрамератенумератор**<br/>                                     | Числитель частоты кадров выходного видео. Эквивалентно атрибуту [**\_ \_ \_ частоты кадров MF MT**](mf-mt-frame-rate-attribute.md) .<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**видеофрамевидс**<br/>                                                                     | Ширина выходного видео. Эквивалентно атрибуту [**\_ \_ \_ размера пакета MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**видеопикселаспектратиоденоминатор**<br/> | Знаменатель (номинал) выходного видео. Эквивалентно атрибуту пропорции [**MF \_ MT \_ пикселей \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**видеопикселаспектратионумератор**<br/>         | Числитель НОМИНАЛа выходного видео. Эквивалентно атрибуту пропорции [**MF \_ MT \_ пикселей \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[топоедит](topoedit.md)
</dt> </dl>

 

 




