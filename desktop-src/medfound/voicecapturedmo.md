---
description: Объект, инкапсулирующий несколько DSP, связанных с захватом голоса.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP для записи голоса (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d05eb6d3f97f748d5c82d8fa566ee25a3a01ce225ab76e84d73f0a86b132afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972553"
---
# <a name="voice-capture-dsp"></a>DSP для записи речи

Объект, инкапсулирующий несколько DSP, связанных с захватом голоса.

## <a name="clsid"></a>CLSID

\_КВМАУДИОАЕК CLSID

## <a name="interfaces"></a>Интерфейсы

-   [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **ипропертисторе**

## <a name="properties"></a>Свойства



| Свойство                                                                                     | Описание                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [\_ \_ индексы устройств мфпкэй вмааекма \_](mfpkey-wmaaecma-device-indexesproperty.md)              | указывает, какие звуковые устройства DMO использовать для записи и подготовки к просмотру звука.                     |
| [МФПКЭЙ \_ вмааекма \_ девицепаир \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Определяет комбинацию звуковых устройств, которые в настоящее время используются приложением.              |
| [мфпкэй \_ вмааекма \_ DMO \_ исходный \_ режим](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | указывает, использует ли DMO режим исходного кода или режима фильтра.                                        |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | указывает, сколько раз DMO выполняет подавление акустического эха (AES) на остаточном сигнале. |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ АГК](mfpkey-wmaaecma-featr-agcproperty.md)                        | указывает, выполняет ли DMO автоматический контроль усиления.                                        |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ \_](mfpkey-wmaaecma-featr-center-clipproperty.md)       | указывает, выполняет ли DMO вырезание по центру.                                               |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Длина эхо](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Указывает длительность эха, который может обрабатывать алгоритм отмены акустических эха (AEC).    |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Задает размер звукового кадра.                                                                   |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | указывает, какой образ используется DMO для обработки массива микрофона.                                |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | указывает, как DMO выполняет обработку массива микрофона.                                       |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | указывает, выполняет ли DMO предварительную обработку массива микрофонов.                                |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ , \_ Заливка шума](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | указывает, выполняет ли DMO заполнение шума.                                                 |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | указывает, выполняет ли DMO подавление шума.                                             |
| [МФПКЭЙ \_ вмааекма \_ феатр \_ Вад](mfpkey-wmaaecma-featr-vadproperty.md)                        | указывает тип обнаружения действий речи, выполняемых DMO.                             |
| [\_ \_ режим компонента мфпкэй \_ вмааекма](mfpkey-wmaaecma-feature-modeproperty.md)                  | Позволяет приложению переопределять параметры по умолчанию для различных свойств.                   |
| [МФПКЭЙ \_ вмааекма \_ для \_ усиления микрофона \_](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | указывает, применяет ли DMO границы усиления микрофона.                                       |
| [МФПКЭЙ \_ вмааекма \_ микаррай \_ дескптр](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Задает геометрию массива микрофона.                                                          |
| [\_ \_ метрики качества мфпкэй вмааекма \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Получает метрики качества для контекста AEC.                                                                |
| [МФПКЭЙ \_ вмааекма \_ Получение \_ \_ статистики TS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | указывает, сохраняет ли DMO статистику штампа времени в реестре.                           |
| [МФПКЭЙ \_ вмааекма \_ \_ режим системы](mfpkey-wmaaecma-system-modeproperty.md)                    | Задает режим обработки.                                                                         |



 

## <a name="remarks"></a>Remarks

в отличие от других dsp, объект записи голоса инкапсулирует несколько dsp в один объект, а объект является только DMOным объектом (он не реализует [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). DMO записи голоса содержит следующие компоненты DSP:

-   Отмена акустического эха (AEC)
-   Обработка массива микрофона
-   Подавление шумов
-   Автоматическое усиление контроля
-   Определение действий речи

Приложения могут включать и отключать каждый компонент отдельно.

запись голоса DMO поддерживает два режима работы: режим *фильтрации* и *исходный* режим. в режиме фильтрации приложение отправляет звуковые примеры с микрофона и из линии динамика в DMO, а DMO выдает выходные данные.

В режиме исходного кода приложению не нужно доставлять образцы в DMO. вместо этого DMO управляет всеми операциями на звуковых устройствах, включая инициализацию устройств, запись и синхронизацию звуковых потоков, вычисление штампов времени и получение геометрии массива микрофона. при использовании исходного режима приложение просто настраивает DMO, а выходные данные DMO — это чистый, обработанный сигнал микрофона. Режим исходного кода значительно проще в использовании, чем режим фильтрации, и рекомендуется для большинства приложений.

в настоящее время запись голоса DMO поддерживает только одноканальное устранение акустического эха (AEC), поэтому выходные данные из строки динамика должны быть одноканальными. Если обработка массива микрофона отключена, многоканальный вход будет сложен в один канал для обработки AEC. Если включены обе операции обработки и обработки AEC для массива микрофонов, то AEC выполняется для каждого элемента микрофона перед обработкой массива микрофона.

### <a name="microphone-array-processing"></a>Обработка массива микрофона

Массив микрофона — это набор тесно позиционированных микрофонов. Для массивов микрофонов важна направленность, чем у одного микрофона, так как акустические волны поступают на каждый микрофон в несколько разные временные интервалы. дополнительные сведения о массивах микрофонов см. в статье [поддержка массивов микрофонов в Windows Vista](/windows-hardware/design/component-guidelines/audio) и [создание и использование массивов микрофона для Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Использование схемы DSP для записи голоса

Чтобы использовать DSP для записи голоса, выполните следующие действия.

### <a name="1-initialize-the-dmo"></a>1. Инициализация DMO

создайте DMO записи речи, вызвав [**cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью clsid **clsid \_ квмаудиоаек**. Запись голоса ДСДП предоставляет только интерфейсы [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) и [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , поэтому ее можно использовать только в качестве DMO.

DMO по умолчанию принимает исходный режим. чтобы выбрать режим фильтрации, присвойте свойству [мфпкэй \_ вмааекма \_ DMO \_ SOURCE \_ mode](mfpkey-wmaaecma-dmo-source-modeproperty.md) значение **VARIANT \_ FALSE**.

затем настройте внутренние свойства DMO с помощью интерфейса [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Единственное свойство, которое должно быть задано приложением, — это свойство [ \_ \_ системного \_ режима мфпкэй вмааекма](mfpkey-wmaaecma-system-modeproperty.md) . Это свойство настраивает конвейер обработки в DMO. Другие свойства являются необязательными.

### <a name="2-set-the-input-and-output-formats"></a>2. Задание форматов входных и выходных данных

если вы используете DMO в режиме фильтрации, задайте формат входных данных, вызвав [**имедиаобжект:: сетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). Входной формат может быть практически любым допустимым несжатым типом данных PCM или с плавающей запятой IEEE-Point. если входной формат не соответствует выходному формату, DMO автоматически выполняет преобразование выборки.

если вы используете DMO в режиме исходного кода, не устанавливайте входной формат. DMO автоматически настраивает входной формат на основе звуковых устройств.

В любом режиме задайте формат вывода, вызвав [**имедиаобжект:: сетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). DMO может принимать следующие форматы выходных данных:

-   Подтип: **медиасубтипе \_ PCM** или **медиасубтипе \_ IEEE \_ float**
-   Блок формата: [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat) или [**вавеформатекс**](/previous-versions/dd757713(v=vs.85))
-   Выборок в секунду: 8 000; 11 025; 16 000; или 22 050
-   Каналы: 1 для режима только AEC, 2 или 4 для обработки массива микрофона
-   Бит на выборку: 16

Следующий код задает для типа выходных данных 16-битный звук PCM с одним каналом:


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. обработка данных

Перед обработкой любых данных рекомендуется вызвать метод [**имедиаобжект:: аллокатестреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Этот метод выделяет ресурсы, используемые внутри DMO. Вызовите **аллокатестреамингресаурцес** после перечисленных выше шагов, а не до. если этот метод не вызывается, DMO автоматически выделяет ресурсы при начале обработки данных.

при использовании DMO в режиме фильтрации необходимо передать входные данные в DMO, вызвав [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Звуковые данные с микрофона переходят в поток 0, а звуковые данные из линии динамика — в поток 1. при использовании DMO в режиме исходного кода не нужно вызывать **ProcessInput**.

Чтобы получить выходные данные из DSP, выполните следующие действия.

1.  Создайте объект buffer для хранения выходных данных. Объект buffer должен реализовывать интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . Размер буфера зависит от требований приложения. Выделение большего буфера может снизить вероятность возникновения сбоев.
2.  объявите [**структуру \_ \_ \_ буфера выходных данных DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) и задайте элемент **pBuffer** , чтобы он указывал на объект BUFFER.
3.  передайте [**структуру \_ \_ \_ буфера выходных данных DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) в метод [**имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) .
4.  продолжайте вызывать этот метод до тех пор, пока у DMO есть выходные данные. DSP сообщает о том, что у него больше выходных данных, установив флаг **DMO \_ output \_ DATA \_ буфферф \_ неполный** в элементе **dwstatus устанавливается** структуры [**\_ \_ \_ буфера выходных данных DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
