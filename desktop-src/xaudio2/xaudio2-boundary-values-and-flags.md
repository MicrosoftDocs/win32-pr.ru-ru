---
description: Константы XAudio2, которые указывают параметры по умолчанию, максимальные значения и флаги.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: XAudio2 граничные значения и флаги (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718101"
---
# <a name="xaudio2-boundary-values-and-flags"></a>XAudio2 граничные значения и флаги

Константы XAudio2, которые указывают параметры по умолчанию, максимальные значения и флаги.

**XAudio2 граничные значения**



| Константа                                                                                                                                                                                                     | Описание                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**\_Максимальный \_ Размер буфера ( \_ байт) XAUDIO2**</dt> </dl>             | Максимально допустимое значение [**для \_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). Аудиобитес.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**XAUDIO2 \_ Максимальное число \_ \_ буферов в очереди**</dt> </dl>       | Максимальное число буферов, разрешенных в очереди голоса.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**XAUDIO2 \_ Максимальное число \_ буферов в \_ системе**</dt> </dl>       | Максимальное число буферов, разрешенных для системных потоков (только для Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**\_Максимальное число \_ звуковых \_ каналов XAUDIO2**</dt> </dl>       | Максимальное значение, допустимое для **вавеформатекс. нчаннелс**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**\_ \_ Частота выборки XAUDIO2 min \_**</dt> </dl>                | Минимальная поддерживаемая частота дискретизации звука.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**\_ \_ Частота выборки XAUDIO2 максимум \_**</dt> </dl>                | Максимальная поддерживаемая частота дискретизации звука.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**\_Максимальный \_ уровень ГРОМКости \_ XAUDIO2**</dt> </dl>             | Максимально допустимый уровень громкости.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**\_Отношение мин \_ FREQ \_ XAUDIO2**</dt> </dl>                   | Коэффициент минимальной частоты, допустимый в исходном голоса.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ Max \_ FREQ \_**</dt> </dl>                   | Допустимое отношение максимальной частоты в исходном голоса.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**\_Отношение FREQ XAUDIO2 по умолчанию \_ \_**</dt> </dl>       | Значение по умолчанию для аргумента **Максфрекуенциратио** [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ Max \_ Filter \_ онеоверк**</dt> </dl>    | Максимальное значение для [**\_ \_ параметров фильтра XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Онеоверк**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**\_Максимальная \_ Частота фильтра \_ XAUDIO2**</dt> </dl> | Максимальное значение для [**\_ \_ параметров фильтра XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Частота**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**XAUDIO2 \_ Максимальное \_ число циклов \_**</dt> </dl>                   | Максимальное значение, которое не будет считаться бесконечным циклом для [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Лупкаунт**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**\_Максимальное число \_ экземпляров XAUDIO2**</dt> </dl>                       | Максимальное число одновременных экземпляров XAudio2, разрешенных на Xbox 360.<br/>                                                                       |



**XAudio2 значения с особым значением**



| Константа                                                                                                                                                                                              | Описание                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ зафиксировать \_ сейчас**</dt> </dl>                         | Используется в качестве параметра для методов с аргументом Operations. Дополнительные сведения см. в разделе [XAudio2 Operation Sets](xaudio2-operation-sets.md) .<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ зафиксировать \_ все**</dt> </dl>                         | Используется в качестве параметра в [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ недопустимое \_ опсет**</dt> </dl>                | Указывает недопустимое значение для аргументов Operations. Дополнительные сведения см. в разделе [XAudio2 Operation Sets](xaudio2-operation-sets.md) .<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ без \_ \_ области цикла**</dt> </dl>            | Указывает отсутствие области цикла, используемой [**в \_ буфере XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Лупкаунт**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**\_Бесконечный цикл XAUDIO2 \_**</dt> </dl>                | Указывает бесконечное зацикливание, используемое в [**\_ буфере XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Лупкаунт**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**XAUDIO2 \_ каналы по умолчанию \_**</dt> </dl>       | Указывает число каналов по умолчанию для текущей платформы, используемое в [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**XAUDIO2 \_ по умолчанию \_ SAMPLERATE**</dt> </dl> | Указывает частоту выборки по умолчанию для текущей платформы, используемую в [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Флаги XAudio2**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что вместо версии выпуска следует использовать отладочную или проверенную версию обработчика звука. См. <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Этот флаг не поддерживается в Windows 8 и Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что исходный голос не будет использовать сдвиг на шаг, см. раздел <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: креатесаурцевоице</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что для исходного голоса не доступно преобразование частоты выборки, выходные данные голоса должны иметь одинаковую частоту выборки. См. раздел <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: креатесаурцевоице</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что результат фильтра должен быть доступен на голоса. См. раздел <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: креатесаурцевоице</strong></a> and <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2:: креатесубмиксвоице</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что голосовое действие должно продолжать выводить выходные данные после его остановки. См. раздел <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice:: останавливаться</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Указывает последний буфер в потоке. См. <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Флаги</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что обработчик звука должен останавливаться, когда не запускаются исходные голоса и запускается при запуске голоса. См. <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что фильтр следует использовать для отправки голоса. См. <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Флаги</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Указывает такт обработки, не установленный по умолчанию, 21,33 мс (1024 образцов по адресу 48KHz). См. <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Указывает, что виртуальный аудио-клиент использовать не следует. См. раздел <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2:: креатемастерингвоице</strong></a>.<br/>
<blockquote>
[!Note]<br />
На устройствах в семействе мобильных устройств всегда используется виртуальный звуковой клиент, независимо от того, используется ли этот флаг.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**XAudio2 параметры по умолчанию для встроенного голоса Filter**



| Константа                                                                                                                                                                                                                 | Описание                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_Тип фильтра по умолчанию XAUDIO2 \_ \_**</dt> </dl>                | Указывает тип фильтра по умолчанию, используемый при передаче голоса и голоса.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**\_Частота фильтров по умолчанию XAUDIO2 \_ \_**</dt> </dl> | Указывает частоту фильтрации по умолчанию, используемую при передаче голоса и голоса.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ Фильтр по умолчанию \_ \_ онеоверк**</dt> </dl>    | Указывает частоту фильтрации по умолчанию Decay для использования с голосовыми и голосовыми отправками.<br/> |



## <a name="remarks"></a>Комментарии

### <a name="platform-requirements"></a>Требования к платформе

Windows 10 (Ксаудио 2.9); Windows 8, Windows Phone 8 (Ксаудио 2,8); Пакет SDK для DirectX (Ксаудио 2,7)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[XAudio2:: константы](constants.md)
</dt> </dl>

 

 
