---
title: Структуры XAudio2
description: В этом разделе содержатся сведения о структурах, предоставляемых Microsoft XAudio2 API.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817657"
---
# <a name="xaudio2-structures"></a>Структуры XAudio2

В этом разделе содержатся сведения о структурах, предоставляемых Microsoft XAudio2 API.



| Структура                                                                                 | Описание                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_БУФЕР XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Представляет буфер звуковых данных.<br/>                                                                                                    |
| [**\_БУФЕР XAUDIO2 \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Представляет буфер данных WMA Audio.<br/>                                                                                                 |
| [**\_Конфигурация отладки \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Задает новую глобальную конфигурацию отладки для XAudio2 при использовании функции Сетдебугконфигуратион.                                             |
| [**\_ \_ Цепочка эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Определяет цепочку эффектов.<br/>                                                                                                            |
| [**\_Дескриптор XAUDIO2 Effect \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Определяет действие.<br/>                                                                                                                  |
| [**\_Параметры фильтра \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Определяет параметры фильтра для исходного голоса.<br/>                                                                                       |
| [**\_Данные производительности \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Получает сведения о производительности.<br/>                                                                                                  |
| [**\_Дескриптор отправки \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Описывает назначение для отправки голоса.<br/>                                                                                                 |
| [**\_Сведения о голосовом XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Содержит сведения о флагах создания, входных каналах и частоте выборки голоса.<br/>                                          |
| [**\_Отправка голоса \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Определяет набор голосов для получения данных из одного выходного голоса.<br/>                                                                 |
| [**XAUDIO2 \_ голосовое \_ состояние**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Возвращает текущее состояние голоса и данные о положении курсора.<br/>                                                                         |
| [**\_Параметры I3DL2 ПЕРЕглагола XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Описание параметров I3DL2 (интерактивных правил рендеринга 3D Audio, уровень 2,0) для использования в функции ReverbConvertI3DL2ToNative.           |
| [**\_Параметры ПЕРЕглагола XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Описывает параметры для использования в переглаголной API.                                                                                                |
| [**XAUDIO2FX \_ волумеметер \_ уровни**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Описание параметров для использования с счетчиком тома API.                                                                                        |
| [**КСАПО \_ локкфорпроцесс \_ \_ Параметры буфера**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Определяет параметры буфера, которые остаются постоянными, когда КСАПО заблокирован.<br/>                                                             |
| [**\_ \_ Параметры буфера процесса \_ ксапо**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Определяет параметры буфера, которые могут меняться от одного вызова к следующему.<br/>                                                                |
| [**\_Свойства регистрации \_ ксапо**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Описывает общие характеристики КСАПО.<br/>                                                                                       |
| [**ФКСЕЧО \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Параметры инициализации для использования с параметром ФКСЕЧО КСАПО.<br/>                                                                             |
| [**\_Параметры фксечо**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Параметры для использования с параметром ФКСЕЧО КСАПО.<br/>                                                                                            |
| [**\_Параметры фксек**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Параметры для использования с параметром ФКСЕК КСАПО.<br/>                                                                                              |
| [**\_Параметры фксмастеринглимитер**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Параметры для использования с параметром Фксмастеринглимитер КСАПО.<br/>                                                                                |
| [**\_Параметры фксреверб**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Параметры для использования с параметром Фксреверб КСАПО.<br/>                                                                                          |
| [**X3DAUDIO \_ конус**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Указывает направленность для многоканального включения в ненизкочастотный режим путем масштабирования поведения DSP в отношении ориентации передатчика.<br/>    |
| [**\_ \_ Кривая расстояния X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Определяет явную кусочно-кривую, состоящие из линейных сегментов, непосредственно определяющих поведение DSP в отношении нормализованного расстояния.<br/> |
| [**\_ \_ Точка кривой расстояния \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Определяет параметр DSP по заданному нормализованному расстоянию.<br/>                                                                               |
| [**\_Параметры X3DAUDIO DSP \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Получает результаты из вызова X3DAudioCalculate.<br/>                                                                              |
| [**X3DAUDIO \_ передатчик**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Определяет одиночный или многоточечный 3D-звук, используемый с произвольным числом звуковых каналов.<br/>                                    |
| [**\_Прослушиватель X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Определяет точку приема трехмерного звука.<br/>                                                                                              |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по программированию](programming-reference.md)
</dt> </dl>

 

 




