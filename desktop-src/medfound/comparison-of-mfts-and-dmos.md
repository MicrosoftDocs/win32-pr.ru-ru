---
description: Media Foundation преобразований (МФТС) — это эволюция модели преобразования, впервые представленной в DirectX Media Objects (дмос).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Сравнение преобразований MFT и объектов DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958984"
---
# <a name="comparison-of-mfts-and-dmos"></a>Сравнение преобразований MFT и объектов DMO

Media Foundation преобразований (МФТС) — это эволюция модели преобразования, впервые представленной в DirectX Media Objects (дмос). В этом разделе перечислены основные способы, в которых МФТС отличается от дмос. прочтите этот раздел, если вы уже знакомы с интерфейсами DMO или хотите преобразовать существующий DMO в таблицу MFT.

Этот раздел состоит из следующих подразделов.

-   [число Потоки](#number-of-streams)
-   [Формат согласования](#format-negotiation)
-   [Потоковая передача](#streaming)
    -   [Выделение ресурсов](#allocating-resources)
    -   [Обработка данных](#processing-data)
    -   [Очистки](#flushing)
    -   [Прекращение работы потока](#stream-discontinuities)
-   [Прочие различия](#miscellaneous-differences)
-   [Флаги](#flags)
    -   [Флаги ProcessInput](#processinput-flags)
    -   [Флаги ProcessOutput](#processoutput-flags)
    -   [Флаги Жетинпутстатус](#getinputstatus-flags)
    -   [Флаги Жетаутпутстатус](#getoutputstatus-flags)
    -   [Флаги Жетинпутстреаминфо](#getinputstreaminfo-flags)
    -   [Флаги Жетаутпутстреаминфо](#getoutputstreaminfo-flags)
    -   [Флаги Сетинпуттипе и Сетаутпуттипе](#setinputtypesetoutputtype-flags)
-   [Код ошибки](#error-codes)
-   [создание гибридных DMO объектов/мфт](#creating-hybrid-dmomft-objects)
-   [Связанные темы](#related-topics)

## <a name="number-of-streams"></a>число Потоки

DMO имеет фиксированное число потоков, тогда как MFT может поддерживать динамическое количество потоков. Клиент может добавлять входные потоки, и MFT может добавлять новые выходные потоки во время обработки. Однако МФТС не требуются для поддержки динамических потоков. Таблица MFT может иметь фиксированное число потоков, точно так же, как DMO.

Для поддержки динамических потоков в таблице MFT используются следующие методы:

-   [**Имфтрансформ:: Аддинпутстреамс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**Имфтрансформ::D Елетеинпутстреам**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**Имфтрансформ:: Жетстреамидс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**Имфтрансформ:: Жетстреамлимитс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Кроме того, метод [**имфтрансформ::P роцессаутпут**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) определяет поведение при добавлении или удалении выходных потоков.

так как дмос имеют фиксированные потоки, потоки на DMO определяются с помощью значений индекса, начинающегося с нуля. МФТС, с другой стороны, используют идентификаторы потоков, которые не обязательно соответствуют значениям индекса. Это связано с тем, что количество потоков в таблице MFT может измениться. Например, поток 0 может быть удален, что покидает поток 1 в качестве первого потока. Однако MFT с фиксированным числом потоков должно учитывать то же соглашение, что и дмос, и использовать значения индекса для идентификаторов потоков.

## <a name="format-negotiation"></a>Формат согласования

МФТС. Используйте интерфейс [**имфмедиатипе**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) для описания типов мультимедиа. В противном случае форматирование согласования с МФТС работает с теми же основными принципами, что и в дмос. В следующей таблице перечислены методы согласования формата для дмос и соответствующие методы для МФТС.



| метод DMO                                                                        | MFT, метод                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Имедиаобжект:: Жетинпуткурренттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**Имфтрансформ:: Жетинпуткурренттипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**Имедиаобжект:: Жетинпутмакслатенци**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**Имфтрансформ:: Жетинпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Имедиаобжект:: Жетинпутсизеинфо**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**Имфтрансформ:: Жетинпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Имедиаобжект:: Жетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**Имфтрансформ:: Жетинпутаваилаблетипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**Имедиаобжект:: Жетаутпуткурренттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**Имфтрансформ:: Жетаутпуткурренттипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**Имедиаобжект:: Жетаутпутсизеинфо**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**Имфтрансформ:: Жетаутпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**Имедиаобжект:: Жетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**Имфтрансформ:: Жетаутпутаваилаблетипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Потоковая передача

Как и дмос, МФТС обрабатывать данные с помощью вызовов методов [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) и [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . ниже приведены основные различия между процессами DMO и MFT при потоковой передаче данных.

### <a name="allocating-resources"></a>Выделение ресурсов

МФТС не имеют методов [**имедиаобжект:: аллокатестреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) и [**Имедиаобжект:: фристреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) , используемых с DMOs. Чтобы эффективно обрабатывать распределение и освобождение ресурсов, MFT может отвечать на следующие сообщения в методе [**имфтрансформ::P роцессмессаже**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**\_ \_ уведомление о \_ начале \_ ПОТОКовой передачи сообщения MFT**](mft-message-notify-begin-streaming.md)
-   [**\_ \_ уведомление о \_ начале \_ потока в \_ сообщении MFT**](mft-message-notify-start-of-stream.md)

Кроме того, клиент может сообщить начало и конец потока, вызвав [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) со следующими сообщениями:

-   [**\_уведомление об \_ \_ окончании \_ \_ потока в сообщении MFT**](mft-message-notify-end-of-stream.md)
-   [**\_ \_ уведомление о \_ завершении \_ ПОТОКовой передачи сообщения MFT**](mft-message-notify-end-streaming.md)

эти два сообщения не имеют точного DMO эквивалента.

### <a name="processing-data"></a>Обработка данных

МФТС используют примеры носителей для хранения входных и выходных данных. Примеры носителей предоставляют интерфейс [**имфсампле**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) и содержат следующие данные:

-   Метка времени и длительность.
-   Атрибуты, содержащие сведения о каждой из образцов. Список атрибутов см. в разделе [Sample Attributes](sample-attributes.md).
-   Ноль или более буферов мультимедиа. Каждый буфер мультимедиа предоставляет интерфейс [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

интерфейс [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) похож на интерфейс DMO **имедиабуффер** . Чтобы получить доступ к базовому буферу памяти, вызовите [**имфмедиабуффер:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Этот метод примерно эквивалентен [**имедиабуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) для дмос.

Для несжатых данных видео буфер мультимедиа может также поддерживать интерфейс [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Файл MFT, который обрабатывает несжатое видео (как входные, так и выходные данные), должен быть подготовлен к использованию интерфейса **IMF2DBuffer** , если он предоставляет буфер. Дополнительные сведения см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

Media Foundation предоставляет некоторые стандартные реализации [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), поэтому обычно нет необходимости писать собственную реализацию. чтобы создать буфер DMO из буфера Media Foundation, вызовите [**мфкреателегацимедиабуфферонмфмедиабуффер**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Очистки

МФТС не имеют метода [**flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Чтобы очистить MFT, вызовите [**имфтрансформ::P роцессмессаже**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением о [**\_ \_ команде \_ очистки сообщения MFT**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Прекращение работы потока

МФТС не имеют метода [**прекращения поддержки**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Чтобы сообщить о ненепрерывности в потоке, установите атрибут [**мфсампликстенсион для \_ небесперебойной**](mfsampleextension-discontinuity-attribute.md) работы в образце входных данных.

## <a name="miscellaneous-differences"></a>Прочие различия

Ниже приведены некоторые дополнительные незначительные отличия между МФТС и дмос.

-   нет эквивалентов для следующих методов DMO:
    -   [**Имедиаобжект:: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**Имедиаобжект:: Сетинпутмакслатенци**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   МФТС не требуется для поддержки агрегирования.
-   МФТС поддерживает операцию, называемую *стоком*. Целью этого является обработка всех данных, остающихся в MF, без предоставления дополнительных входных данных в MFT (например, в конце потока). Чтобы очистить MFT, вызовите [**имфтрансформ::P роцессмессаже**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением о [**\_ \_ \_ стоке команды сообщения MFT**](mft-message-command-drain.md) . Дополнительные сведения см. в разделе [Базовая модель обработки MFT](basic-mft-processing-model.md).
-   МФТС могут иметь атрибуты, включая атрибуты для каждого потока. Используйте следующие методы для получения атрибутов из MFT:

    -   [**Имфтрансформ:: OutAttribute**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**Имфтрансформ:: Жетинпутстреаматтрибутес**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**Имфтрансформ:: Жетаутпутстреаматтрибутес**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   МФТС может обрабатывать события. Чтобы отправить событие в таблицу MFT, вызовите [**имфтрансформ::P роцессевент**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). MFT может отправить событие клиенту через метод [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Дополнительные сведения см. в разделе [Базовая модель обработки MFT](basic-mft-processing-model.md).

## <a name="flags"></a>Флаги

в следующих таблицах перечислены различные флаги DMO и их эквиваленты в MFT. каждый раз, когда флаг DMO сопоставляется непосредственно с флагом MFT, оба флага имеют одинаковое числовое значение. однако некоторые флаги DMO не имеют точных эквивалентов MFT и наоборот.

### <a name="processinput-flags"></a>Флаги ProcessInput

дмос: DMO перечисление [**\_ \_ \_ \_ \_ флагов буфера входных данных**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) .

МФТС: нет эквивалентного перечисления.



| флаг DMO                                  | Флаг MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO \_ ВХОДные \_ данные \_ буфферф \_ точки**  | Нет эквивалентного флага. Вместо этого задайте атрибут [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) в образце. |
| **DMO \_ \_ \_ время буфферф входных данных \_**       | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: сетсамплетиме**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) в примере.                                  |
| **DMO \_ ВХОДные \_ данные \_ буфферф \_ тимеленгс** | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: сетсампледуратион**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) в примере.                          |



 

### <a name="processoutput-flags"></a>Флаги ProcessOutput

дмос: перечисление [**\_ \_ \_ \_ флагов вывода процесса DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) .

МФТС: перечисление [**\_ \_ \_ \_ флагов вывода процесса MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| флаг DMO                                            | Флаг MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **DMO \_ Обработка \_ выходных \_ данных \_ при \_ отсутствии \_ буфера** | **выходные данные процесса MFT отменяются \_ \_ \_ \_ при \_ отсутствии \_ буфера** |



 

дмос: перечисление [**\_ \_ \_ \_ \_ флагов буфера выходных данных DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) .


МФТС: перечисление [**\_ \_ \_ \_ \_ флагов буфера выходных данных MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| флаг DMO                                   | Флаг MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO \_ OUTPUT \_ Data \_ буфферф \_ точки**  | Нет эквивалентного флага. Вместо этого проверьте атрибут [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) в образце. |
| **DMO \_ \_ \_ время буфферф выходных \_ данных**       | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: жетсамплетиме**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) в примере.                                        |
| **DMO \_ OUTPUT \_ Data \_ буфферф \_ тимеленгс** | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: жетсампледуратион**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) в примере.                                |
| **DMO \_ ВЫХОДНЫЕ \_ данные \_ буфферф \_ неполны** | **\_Буфер выходных \_ данных \_ MFT \_ неполон**                                                                                                           |
| Нет эквивалентного флага.                        | **\_ \_ \_ \_ изменение формата буфера выходных данных \_ MFT**                                                                                                       |
| Нет эквивалентного флага.                        | **\_ \_ \_ \_ конечный поток буфера выходных данных \_ MFT**                                                                                                          |
| Нет эквивалентного флага.                        | **\_Буфер выходных \_ данных \_ MFT \_ без \_ примера**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Флаги Жетинпутстатус

дмос: перечисление **\_ \_ \_ \_ флагов состояния ввода DMO** .

МФТС: перечисление [**\_ \_ \_ \_ флагов состояния входных файлов MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| флаг DMO                              | Флаг MFT                             |
|---------------------------------------|--------------------------------------|
| **DMO \_ ВХОДные \_ \_ данные приема статусф \_** | **\_входные \_ данные состояния входной \_ \_ таблицы MFT** |



 

### <a name="getoutputstatus-flags"></a>Флаги Жетаутпутстатус

Дмос: нет эквивалентного перечисления.

МФТС: перечисление [**\_ \_ \_ \_ флагов состояния вывода MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| флаг DMO            | Флаг MFT                               |
|---------------------|----------------------------------------|
| Нет эквивалентного флага. | **\_образец состояния выходных файлов MFT \_ \_ \_ готов** |



 

### <a name="getinputstreaminfo-flags"></a>Флаги Жетинпутстреаминфо

дмос: DMO перечисление [**\_ \_ \_ \_ \_ флагов сведений о входном потоке**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) .

МФТС: сведения о перечислении [**\_ \_ \_ \_ \_ флагов сведений о входном потоке MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) .



| флаг DMO                                             | Флаг MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **DMO \_ ВХОДные \_ стреамф \_ целые \_ примеры**              | **\_ \_ \_ все примеры ВХОДного потока MFT \_**              |
| **DMO \_ ВХОДНОЙ \_ стреамф \_ один \_ Выбор \_ на \_ буфер** | **\_ \_ один пример входного потока MFT \_ \_ \_ на \_ буфер** |
| **DMO \_ ВХОДНОЙ \_ стреамф \_ фиксированный \_ Размер выборки \_**         | **\_ \_ \_ фиксированный \_ \_ Размер образца входного потока MFT**         |
| **DMO \_ ВХОДНОЙ \_ стреамф \_ содержит \_ буферы**              | **\_входной \_ поток MFT \_ содержит \_ буферы**              |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ \_ не выполняет \_ ADDREF**           |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ съемный**                   |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ необязательный**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Флаги Жетаутпутстреаминфо

дмос: перечисление [**\_ \_ \_ \_ \_ флагов сведений о потоке вывода DMO**](/previous-versions/ms806053(v=msdn.10)) .

МФТС: перечисление [**\_ \_ \_ \_ \_ флагов сведений о потоках вывода MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) .



| флаг DMO                                              | Флаг MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **DMO \_ ВЫХОДНЫЕ \_ стреамф \_ целые \_ примеры**              | **\_ \_ \_ все примеры выходных потоков \_ MFT**              |
| **DMO \_ ВЫВОД \_ стреамф \_ одного \_ образца \_ на \_ буфер** | **\_ \_ один пример потока вывода MFT \_ \_ \_ на \_ буфер** |
| **DMO \_ ВЫХОДНОЙ \_ стреамф \_ фиксированный \_ Размер выборки \_**         | **\_ \_ \_ фиксированный \_ Размер образца потока выходных файлов MFT \_**         |
| **DMO \_ ВЫХОДНОЙ \_ стреамф \_ отклоняется**                 | **\_выходной \_ поток MFT \_ удален**                 |
| **DMO \_ OUTPUT \_ стреамф ( \_ необязательно)**                    | **\_выходной \_ поток MFT \_ необязателен**                    |
| Нет эквивалентного флага.                                   | **\_поток вывода \_ MFT \_ содержит \_ примеры**           |
| Нет эквивалентного флага.                                   | **\_поток вывода \_ MFT \_ может \_ предоставлять \_ образцы**       |
| Нет эквивалентного флага.                                   | **\_поток вывода MFT с \_ \_ отложенным \_ чтением**                  |
| Нет эквивалентного флага.                                   | **\_поток вывода MFT, \_ \_ съемный**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Флаги Сетинпуттипе и Сетаутпуттипе

дмос: перечисление [**\_ \_ \_ \_ флагов типа набора DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) .

МФТС: перечисление [**\_ \_ \_ \_ флагов типов набора MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| флаг DMO                        | Флаг MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO \_ ЗАДАТЬ \_ \_ только тест \_ типеф** | **\_набор MFT \_ \_ только проверка \_ типа**                                                       |
| **DMO \_ ЗАДАТЬ \_ типеф \_ clear**      | Нет эквивалентного флага. Вместо этого задайте для типа носителя **значение NULL** , чтобы очистить тип носителя. |



 

## <a name="error-codes"></a>Коды ошибок

в следующей таблице показано, как сопоставлять коды ошибок, DMO коды ошибок MFT. гибридный объект MFT/DMO должен возвращать коды ошибок DMO из методов [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) и коды ошибок MFT из методов [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . коды ошибок DMO определены в файле заголовка медиаерр. h. Коды ошибок MFT определены в файле заголовка мферрор. h.



| код ошибки DMO                  | Код ошибки MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ инвалидтипе**         | **MF \_ E \_ инвалидтипе**               |
| **DMO \_ E \_ инвалидстреаминдекс**  | **MF \_ E \_ инвалидстреамнумбер**       |
| **DMO \_ E \_ нотакцептинг**        | **MF \_ E \_ нотакцептинг**              |
| **DMO \_ больше \_ \_ элементов нет \_**     | **MF \_ E \_ больше \_ \_ типов**           |
| **DMO \_ \_Тип E \_ не \_ принят** | **MF \_ E \_ инвалидмедиатипе**          |
| **DMO \_ \_Тип E \_ не \_ задан**      | **\_ \_ тип преобразования MF \_ E \_ не \_ задан** |



 

## <a name="creating-hybrid-dmomft-objects"></a>создание гибридных DMO объектов/мфт

Интерфейс [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) слабо основан на [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), который является основным интерфейсом для объектов мультимедиа DirectX (дмос). Можно создавать объекты, предоставляющие оба интерфейса. Однако это может привести к конфликтам имен, так как интерфейсы имеют некоторые методы с одинаковыми именами. Решить эту проблему можно одним из двух способов.

Решение 1. Включите следующую строку в начало любого CPP файла, содержащего функции MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Это изменяет объявление интерфейса [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) , чтобы большинство имен методов были префиксом MFT. Таким образом, [**имфтрансформ::P роцессинпут**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) преобразуется в **Имфтрансформ:: Мфтпроцессинпут**, а [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) сохраняет свое исходное имя. этот метод наиболее удобен при преобразовании существующего DMO в гибридную DMO/мфт. вы можете добавить новые методы MFT, не изменяя методы DMO.

Решение 2. Использование синтаксиса C++ для неоднозначности имен, унаследованных от более чем одного интерфейса. Например, объявите версию MFT для [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) следующим образом:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

объявите DMO версию [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) следующим образом:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

При выполнении внутреннего вызова метода в объекте можно использовать этот синтаксис, но это приведет к переопределению виртуального состояния метода. Для вызова внутри объекта лучше всего использовать следующие объекты:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Таким образом, если вы наследуете от **кмихибридобжект** другой класс и переопределяете метод кмихибридобжект:: имедиаобжект::P роцессинпут, вызывается правильный виртуальный метод. интерфейсы DMO описаны в документации по пакету SDK для DirectShow.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
