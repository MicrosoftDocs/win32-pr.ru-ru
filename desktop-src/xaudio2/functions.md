---
title: Функции XAudio2
description: В этом разделе содержатся сведения о функциях, предоставляемых Microsoft XAudio2 API.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b950ce33f55a4b834f3ee7a068f613e144c2e30633c67e887b8a24789140a618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109654"
---
# <a name="xaudio2-functions"></a>Функции XAudio2

В этом разделе содержатся сведения о функциях, предоставляемых Microsoft XAudio2 API.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                       | Описание                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатефкс**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Создает экземпляр запрошенного [ксапофксного](xapofx-overview.md) действия.<br/>                                                                                                                                                         |
| [**креатехртфапо**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Создает экземпляр интерфейса [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) для обработки, связанной с функцией пересылки (хртф).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Встроенная функция, преобразующая параметры I3DL2 (Interactive 3D Audio, рекомендации уровня 2,0) в собственные параметры XAudio2.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Вычисляет параметры DSP по отношению к трехмерным параметрам.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Задает все глобальные трехмерные константы аудио.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Встроенная функция, преобразующая значение коэффициента амплитуды в значение шкала.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Создает новый объект **XAudio2** и возвращает указатель на его интерфейс [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Создает новый объект для обработки звуковых аудиозаписей (API) и возвращает указатель на него.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Создает новый объект обработки звука для отслеживания громкости (API) и возвращает указатель на него.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Встроенная функция, преобразующая частоту отсечения фильтра, выраженную в герцах, в коэффициенты фильтрации, используемые с элементом **Frequency** структуры [**\_ \_ параметров фильтра XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Встроенная функция, преобразующая частоту отсечения фильтра, выраженную в герцах, в значения частоты радиан, используемые в элементе **Frequency** структуры [**\_ \_ параметров фильтра XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Встроенная функция, преобразующая значение шкала в значение коэффициента амплитуды.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Встроенная функция, преобразующая значение коэффициента частоты в значение полтона.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Встроенная функция, преобразующая частоту радиан, используемую [**в \_ \_ параметрах фильтра XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) , к абсолютным частотам в герцах.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Встроенная функция, преобразующая значение полтона в значение коэффициента частоты.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[XAudio2: Справочник по:P рограмминг](programming-reference.md)
</dt> </dl>

 

 




