---
description: В этой статье содержатся общие рекомендации по использованию API-интерфейсов видео Direct3D 12.
ms.assetid: ''
title: Видеообзор Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 561ceba8a3110d6aa7e9a336430c0a14ddb45bc5707c650588a08c391cd65863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828324"
---
# <a name="direct3d-12-video-overview"></a>Видеообзор Direct3D 12

В этой статье содержатся общие рекомендации по использованию API-интерфейсов видео Direct3D 12.

## <a name="about-direct3d-12-video"></a>Видео о Direct3D 12

Видеоинтерфейс Direct3D 12 предоставляет приложениям новый способ реализации декодирования и обработки видео. Интерфейс Direct3D 12 отличается от предыдущего интерфейса Direct3D 11, так как он спроектирован так, чтобы соответствовать принципам и стилю Direct3D 12, включая следующие:

- Предоставление разработчикам дополнительных возможностей управления
 - Выделение памяти, доступной для оборудования
 - Потоки ЦП, используемые для создания команд отправки &
   - Независимое поколение и отправка
   - Неблокирующий
 - Планирование работы оборудования
- В этой статье рассматриваются существующие функциональные возможности, включая большинство функций видео Direct3D 11, но в то же время обеспечивает простоту и простоту использования.
- Питание и производительность основных приложений Direct3D 12, которые равны или более чем Direct3D 11
- Согласованность с другими API-интерфейсами Direct3D 12
- Взаимодействие с существующими API графических интерфейсов


## <a name="video-decoding"></a>Декодирование видео

В следующих разделах описаны некоторые задачи, связанные с реализацией декодирования видео Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Запрос возможностей декодирования

Вызовите [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , чтобы проверить сведения о поддержке для операций декодирования видео Direct3D 12. Передайте значение из перечисления [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) , чтобы указать компонент, для которого запрашиваются сведения о поддержке.

### <a name="create-the-video-decoder"></a>Создание видеодекодера

Вызовите метод [ID3D12VideoDevice:: креатевидеодекодер](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) , чтобы создать экземпляр интерфейса [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) . Декодер содержит состояние сеанса декодирования, включая данные, связанные со ссылками, такие как векторы движения.  В случае изменения разрешения или [максдекодепиктуребуфферкаунт](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) объект декодера создается повторно. Ширина и высота декодирования укажите собственное разрешение потока перед любым масштабом.  В поле Максимальное число раскодированных буферов рисунков (ДПБ) указано наибольшее число ДПБ, которое можно использовать без повторного создания видеодекодера.

Декодер может использоваться для записи команд из нескольких списков команд, но может быть связан только с одним списком команд за раз.  Приложение отвечает за синхронизацию доступа к декодеру.

### <a name="create-the-video-decoder-heap"></a>Создание кучи видеодекодера 

Вызовите метод [ID3D12VideoDevice:: креатевидеодекодерхеап](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) , чтобы создать экземпляр интерфейса [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) . Этот объект содержит ресурсы и состояние драйвера, зависящие от разрешения.

### <a name="decoding-a-frame"></a>Декодирование кадра

Все входные и выходные параметры для операций обработки видео организованы в структуру входных параметров, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)и структуру выходного параметра [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
Приложение управляет эталонными кадрами и, таким образом, должно задать опорные кадры для каждой операции декодирования.
Когда список команд записывается правильно, вызовите [ID3D12CommandQueue:: ексекутекоммандлистс](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) в очереди команд видео, чтобы отправить кадр в код GPU.


### <a name="enabling-decoder-output-conversions"></a>Включение преобразования выходных данных декодера
Если декодер поддерживает преобразование, включите необходимые преобразования, правильно заполнив структуру [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) . Формат и разрешение требуемых выходных данных и собственных выходных данных декодера передаются через различия в цветовых пространствах и разрешениях, указанных в параметрах преобразования.

##  <a name="querying-decoding-status"></a>Запрос состояния декодирования 
Используйте методы [ID3D12VideoDecodeCommandList:: бегинкуери](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) и [ID3D12VideoDecodeCommandList:: ендкуери](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) для запроса состояния операции декодирования.

Структура [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) используется для описания статистики видеорасшифровки. Чтобы получить экземпляр этой структуры, необходимо вызвать [ID3D12VideoDecodeCommandList:: ендкуери](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), передав значение типа запроса кучи, равное [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Обратите внимание, что этот запрос не использует [ID3D12VideoDecodeCommandList:: бегинкуери](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Обработка видео

API-интерфейсы видео Direct3D 12 используют упрощенный подход к обработке видео, устраняя возможности Direct3D 11, которые не использовались широко, и удаляют проверки возможностей для компонентов, которые являются обязательными на разных устройствах. Процесс перечисления для обработки видео исключен. Вместо этого вызовите [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , который позволяет приложению обнаруживать возможности обработчика видео. Требуемое видео, чересстрочную развертку, форматы стерео и скорости предоставляются в качестве входных данных для **чеккфеатуресуппорт**.

### <a name="removed-capabilities"></a>Удаленные возможности

Следующие возможности Direct3D 11 не поддерживаются при обработке видео Direct3D 12:
- Настраиваемые тарифы.  Вместо этого существует скорость ввода и вывода, заданная во время записи команды [ID3D12VideoProcessCommandList::P роцессфрамес](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) .
- Теперь доступны только два режима разчередования: [Bob](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) и [Custom](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). Другие режимы были исключены. CUSTOM — это высококачественный режим с чередованием, предоставляемый поставщиком оборудования.
- Все необязательные форматы стерео в [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) больше не поддерживаются. Вместо этого [Ноно](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [горизонтальные](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [вертикальные](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)и [отдельные](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) являются обязательными для всех аппаратных устройств, если поддерживается стерео.
- Для [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) или [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps)не существует эквивалента. Вместо этого входные и выходные форматы являются аргументами для создания видеопроцессора и в это время должны быть известны, если обработчик видео может или не может выполнить операцию с заданным форматом. [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) используется, чтобы указать, доступны ли функции автоматической обработки.
- Для [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)не существует эквивалента.
- Для [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)не существует эквивалента.
- При преобразовании из стерео в Mono предполагается, что базовое представление равно 0.
- Видео-обработка Direct3D 12 не поддерживает преобразование Mono в стерео и не поддерживает смещение Mono. 


### <a name="creating-a-video-processor"></a>Создание видеопроцессора

Вызовите метод [ID3D12VideoDevice:: креатевидеопроцессор](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) , чтобы создать экземпляр [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). Обработчик видео содержит состояние сеанса обработки видео, включая требуемую промежуточную память, кэшированные данные обработки или другое временное рабочее пространство. Аргументы создания видеопроцессора указывают, какие операции выполняются или доступны в [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) Time.  Выделение драйвера для выполнения операции видеопроцесса (например, промежуточные) выделяется во время создания видеопроцессора.  Чтобы заранее определить размер выделения видеопроцессора, используйте [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) .

Обработчик видео может использоваться только для записи команд из нескольких списков команд, но может быть связан только с одним списком команд за раз.  Приложение отвечает за синхронизацию доступа к обработчику видео.  Приложение также должно записывать команды обработки видео в прокоессор видео в том порядке, в котором они выполняются на GPU.

Все входные и выходные аргументы для операций обработки видео организованы в структуру входных аргументов, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)и структуру выходного аргумента [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). Приложение должно вызвать [ID3D12VideoProcessCommandList::P роцессфрамес](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) , чтобы записать операцию обработки видео, которую нужно выполнить. 

Когда список команд записывается, вызовите [ID3D12CommandQueue:: ексекутекоммандлистс](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) в очереди команд видео, чтобы отправить кадровую обработку в GPU.


## <a name="tiers"></a>Уровни

Видео Direct3D 12 определяет уровни, которые группируют возможности аппаратных устройств, чтобы у приложения было меньше путей кода для работы с различными аппаратными средствами. Уровни указываются с помощью перечисления [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) .

На всех уровнях будут доступны следующие возможности:

- Нет необходимости в воспроизведении декодера при изменениях разрешения. При изменении разрешения необходимо повторно создать только кучу декодера.
- Все фреймы ссылок будут управляться приложением. Это позволяет системе экономить память, поскольку нам не нужно выделять максимальное количество Дпбс на время создания декодера на некоторых уровнях и обеспечивает гибкость приложений в сценариях изменения разрешения.

Обратите внимание, что уровни являются наборами. Приложение может принять решение об уровне 1 и не использовать функции более высокого уровня, которые являются допустимыми, но могут не предоставлять оптимальные производительности. Дополнительные сведения о возможностях, связанных с различными уровнями уровней, см. в разделе [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Опорные кадры

В видеоролике Direct3D 12 ссылочные кадры передаются явным образом. Это позволяет очищать использование массива текстур или массивов текстур при декодировании кадров. Приложению не обязательно передавать тот же самый маркер ресурса при использовании его в качестве ссылки; Например, можно скопировать один ресурс в другой, а затем передать копию вместо исходной. Индексы ДКСВА *реффрамелист* и *куррпик* по-прежнему используются драйвером для хранения релевантных данных для каждого декодированного кадра.


## <a name="directx-12-fences"></a>Ограждения DirectX 12

В DirectX 12 приложение отвечает за синхронизацию доступа к своим буферам. В случае декодирования потребуется добавить ограждения во входные буферы и в выходные буферы. С каждой ограждением связано значение и используются для синхронизации ПРОЦЕССОРов и аппаратных ядер. Дополнительные сведения см. [в статье использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Типичная реализация будет иметь ограждение для каждого входного буфера. В случае входных буферов возможно, что буфер может быть доступен до завершения всего процесса декодирования. Система игнорирует этот случай и предполагает, что входной буфер будет доступен при декодировании.
Реализация также обычно имеет ограждение для каждого выходного буфера. Например, при отправке выходных данных в компоновщик требуется ограждение, сообщающее о том, что эта презентация в конечном итоге выполняется, указывая, что выходные данные снова доступны для декодера.


## <a name="related-topics"></a>Связанные темы

<dl> <dt>
[API-интерфейсы](direct3d-12-video-apis.md) 
 видео Direct3D 12 [Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> </dl>

 

 
