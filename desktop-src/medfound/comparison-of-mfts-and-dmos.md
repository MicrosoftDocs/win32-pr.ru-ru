---
description: Media Foundation преобразований (МФТС) — это эволюция модели преобразования, впервые представленной в DirectX Media Objects (дмос).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Сравнение преобразований MFT и объектов DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072577"
---
# <a name="comparison-of-mfts-and-dmos"></a>Сравнение преобразований MFT и объектов DMO

Media Foundation преобразований (МФТС) — это эволюция модели преобразования, впервые представленной в DirectX Media Objects (дмос). В этом разделе перечислены основные способы, в которых МФТС отличается от дмос. Прочтите этот раздел, если вы уже знакомы с интерфейсами DMO или хотите преобразовать существующий объект DMO в таблицу MFT.

В этом разделе содержатся следующие подразделы.

-   [Число потоков](#number-of-streams)
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
-   [Создание гибридных объектов DMO/MFT](#creating-hybrid-dmomft-objects)
-   [См. также](#related-topics)

## <a name="number-of-streams"></a>Число потоков

Объект DMO имеет фиксированное число потоков, а Таблица MFT может поддерживать динамическое число потоков. Клиент может добавлять входные потоки, и MFT может добавлять новые выходные потоки во время обработки. Однако МФТС не требуются для поддержки динамических потоков. Таблица MFT может иметь фиксированное число потоков, как и DMO.

Для поддержки динамических потоков в таблице MFT используются следующие методы:

-   [**Имфтрансформ:: Аддинпутстреамс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**Имфтрансформ::D Елетеинпутстреам**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**Имфтрансформ:: Жетстреамидс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**Имфтрансформ:: Жетстреамлимитс**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Кроме того, метод [**имфтрансформ::P роцессаутпут**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) определяет поведение при добавлении или удалении выходных потоков.

Так как дмос имеют фиксированные потоки, потоки в DMO идентифицируются с помощью значений индекса, начинающегося с нуля. МФТС, с другой стороны, используют идентификаторы потоков, которые не обязательно соответствуют значениям индекса. Это связано с тем, что количество потоков в таблице MFT может измениться. Например, поток 0 может быть удален, что покидает поток 1 в качестве первого потока. Однако MFT с фиксированным числом потоков должно учитывать то же соглашение, что и дмос, и использовать значения индекса для идентификаторов потоков.

## <a name="format-negotiation"></a>Формат согласования

МФТС. Используйте интерфейс [**имфмедиатипе**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) для описания типов мультимедиа. В противном случае форматирование согласования с МФТС работает с теми же основными принципами, что и в дмос. В следующей таблице перечислены методы согласования формата для дмос и соответствующие методы для МФТС.



| Метод DMO                                                                        | MFT, метод                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Имедиаобжект:: Жетинпуткурренттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**Имфтрансформ:: Жетинпуткурренттипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**Имедиаобжект:: Жетинпутмакслатенци**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**Имфтрансформ:: Жетинпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Имедиаобжект:: Жетинпутсизеинфо**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**Имфтрансформ:: Жетинпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Имедиаобжект:: Жетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**Имфтрансформ:: Жетинпутаваилаблетипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**Имедиаобжект:: Жетаутпуткурренттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**Имфтрансформ:: Жетаутпуткурренттипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**Имедиаобжект:: Жетаутпутсизеинфо**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**Имфтрансформ:: Жетаутпутстреаминфо**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**Имедиаобжект:: Жетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**Имфтрансформ:: Жетаутпутаваилаблетипе**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Потоковая передача

Как и дмос, МФТС обрабатывать данные с помощью вызовов методов [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) и [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Ниже приведены основные различия между процессами DMO и MFT при потоковой передаче данных.

### <a name="allocating-resources"></a>Выделение ресурсов

МФТС не имеют методов [**имедиаобжект:: аллокатестреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) и [**Имедиаобжект:: фристреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) , используемых с DMOs. Чтобы эффективно обрабатывать распределение и освобождение ресурсов, MFT может отвечать на следующие сообщения в методе [**имфтрансформ::P роцессмессаже**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**\_ \_ уведомление о \_ начале \_ ПОТОКовой передачи сообщения MFT**](mft-message-notify-begin-streaming.md)
-   [**\_ \_ уведомление о \_ начале \_ потока в \_ сообщении MFT**](mft-message-notify-start-of-stream.md)

Кроме того, клиент может сообщить начало и конец потока, вызвав [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) со следующими сообщениями:

-   [**\_уведомление об \_ \_ окончании \_ \_ потока в сообщении MFT**](mft-message-notify-end-of-stream.md)
-   [**\_ \_ уведомление о \_ завершении \_ ПОТОКовой передачи сообщения MFT**](mft-message-notify-end-streaming.md)

Эти два сообщения не имеют точной эквивалента DMO.

### <a name="processing-data"></a>Обработка данных

МФТС используют примеры носителей для хранения входных и выходных данных. Примеры носителей предоставляют интерфейс [**имфсампле**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) и содержат следующие данные:

-   Метка времени и длительность.
-   Атрибуты, содержащие сведения о каждой из образцов. Список атрибутов см. в разделе [Sample Attributes](sample-attributes.md).
-   Ноль или более буферов мультимедиа. Каждый буфер мультимедиа предоставляет интерфейс [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

Интерфейс [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) аналогичен интерфейсу DMO **имедиабуффер** . Чтобы получить доступ к базовому буферу памяти, вызовите [**имфмедиабуффер:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Этот метод примерно эквивалентен [**имедиабуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) для дмос.

Для несжатых данных видео буфер мультимедиа может также поддерживать интерфейс [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Файл MFT, который обрабатывает несжатое видео (как входные, так и выходные данные), должен быть подготовлен к использованию интерфейса **IMF2DBuffer** , если он предоставляет буфер. Дополнительные сведения см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

Media Foundation предоставляет некоторые стандартные реализации [**имфмедиабуффер**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), поэтому обычно нет необходимости писать собственную реализацию. Чтобы создать буфер DMO из буфера Media Foundation, вызовите [**мфкреателегацимедиабуфферонмфмедиабуффер**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Очистки

МФТС не имеют метода [**flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Чтобы очистить MFT, вызовите [**имфтрансформ::P роцессмессаже**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением о [**\_ \_ команде \_ очистки сообщения MFT**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Прекращение работы потока

МФТС не имеют метода [**прекращения поддержки**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Чтобы сообщить о ненепрерывности в потоке, установите атрибут [**мфсампликстенсион для \_ небесперебойной**](mfsampleextension-discontinuity-attribute.md) работы в образце входных данных.

## <a name="miscellaneous-differences"></a>Прочие различия

Ниже приведены некоторые дополнительные незначительные отличия между МФТС и дмос.

-   Для следующих методов DMO нет эквивалентов MFT:
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

В следующих таблицах перечислены различные флаги DMO и их эквиваленты в MFT. Каждый раз, когда флаг DMO сопоставляется непосредственно с флагом MFT, оба флага имеют одинаковое числовое значение. Однако некоторые флаги DMO не имеют точных эквивалентов MFT и наоборот.

### <a name="processinput-flags"></a>Флаги ProcessInput

Дмос: присвоено перечисление [**\_ \_ \_ \_ \_ флагов буфера входных данных DMO**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) .

МФТС: нет эквивалентного перечисления.



| Флаг DMO                                  | Флаг MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_входные \_ данные DMO \_ буфферф \_ точки**  | Нет эквивалентного флага. Вместо этого задайте атрибут [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) в образце. |
| **\_ \_ \_ время буфферф ВХОДных данных DMO \_**       | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: сетсамплетиме**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) в примере.                                  |
| **\_входные \_ данные DMO \_ буфферф \_ тимеленгс** | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: сетсампледуратион**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) в примере.                          |



 

### <a name="processoutput-flags"></a>Флаги ProcessOutput

Дмос: перечисление [**\_ \_ \_ \_ флагов вывода процесса DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) .

МФТС: перечисление [**\_ \_ \_ \_ флагов вывода процесса MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| Флаг DMO                                            | Флаг MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_отбросить \_ выходные данные процесса DMO \_ \_ при \_ отсутствии \_ буфера** | **выходные данные процесса MFT отменяются \_ \_ \_ \_ при \_ отсутствии \_ буфера** |



 

Дмос: перечисление [**\_ \_ \_ \_ \_ флагов буфера выходных данных DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) .


МФТС: перечисление [**\_ \_ \_ \_ \_ флагов буфера выходных данных MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| Флаг DMO                                   | Флаг MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ буфферф точки выходных данных \_ DMO**  | Нет эквивалентного флага. Вместо этого проверьте атрибут [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) в образце. |
| **\_ \_ \_ время БУФФЕРФ выходных данных \_ DMO**       | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: жетсамплетиме**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) в примере.                                        |
| **\_ \_ \_ буфферф ТИМЕЛЕНГС выходных данных \_ DMO** | Нет эквивалентного флага. Вместо этого вызовите [**имфсампле:: жетсампледуратион**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) в примере.                                |
| **\_буфферф выходных \_ данных DMO не \_ \_ завершен** | **\_Буфер выходных \_ данных \_ MFT \_ неполон**                                                                                                           |
| Нет эквивалентного флага.                        | **\_ \_ \_ \_ изменение формата буфера выходных данных \_ MFT**                                                                                                       |
| Нет эквивалентного флага.                        | **\_ \_ \_ \_ конечный поток буфера выходных данных \_ MFT**                                                                                                          |
| Нет эквивалентного флага.                        | **\_Буфер выходных \_ данных \_ MFT \_ без \_ примера**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Флаги Жетинпутстатус

Дмос: перечисление **\_ \_ \_ \_ флагов состояния ввода DMO** .

МФТС: перечисление [**\_ \_ \_ \_ флагов состояния входных файлов MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| Флаг DMO                              | Флаг MFT                             |
|---------------------------------------|--------------------------------------|
| **\_входные \_ \_ данные Accept \_ статусф для DMO** | **\_входные \_ данные состояния входной \_ \_ таблицы MFT** |



 

### <a name="getoutputstatus-flags"></a>Флаги Жетаутпутстатус

Дмос: нет эквивалентного перечисления.

МФТС: перечисление [**\_ \_ \_ \_ флагов состояния вывода MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| Флаг DMO            | Флаг MFT                               |
|---------------------|----------------------------------------|
| Нет эквивалентного флага. | **\_образец состояния выходных файлов MFT \_ \_ \_ готов** |



 

### <a name="getinputstreaminfo-flags"></a>Флаги Жетинпутстреаминфо

Дмос: данные перечисления [**\_ \_ \_ \_ \_ flags входного потока DMO**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) .

МФТС: сведения о перечислении [**\_ \_ \_ \_ \_ флагов сведений о входном потоке MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) .



| Флаг DMO                                             | Флаг MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_ \_ \_ все примеры ВХОДных стреамф DMO \_**              | **\_ \_ \_ все примеры ВХОДного потока MFT \_**              |
| **\_Вход DMO \_ стреамф \_ один \_ Выбор \_ на \_ буфер** | **\_ \_ один пример входного потока MFT \_ \_ \_ на \_ буфер** |
| **\_ \_ \_ фиксированный \_ \_ Размер образца входных данных DMO стреамф**         | **\_ \_ \_ фиксированный \_ \_ Размер образца входного потока MFT**         |
| **\_входные \_ стреамф DMO \_ содержат \_ буферы**              | **\_входной \_ поток MFT \_ содержит \_ буферы**              |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ \_ не выполняет \_ ADDREF**           |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ съемный**                   |
| Нет эквивалентного флага.                                  | **\_входной \_ поток MFT \_ необязательный**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Флаги Жетаутпутстреаминфо

Дмос: перечисление [**\_ \_ \_ \_ \_ флагов сведений о выходных потоках DMO**](/previous-versions/ms806053(v=msdn.10)) .

МФТС: перечисление [**\_ \_ \_ \_ \_ флагов сведений о потоках вывода MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) .



| Флаг DMO                                              | Флаг MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_ \_ \_ все примеры выходных данных DMO стреамф \_**              | **\_ \_ \_ все примеры выходных потоков \_ MFT**              |
| **\_выходные данные DMO \_ стреамф \_ один \_ Выбор \_ на \_ буфер** | **\_ \_ один пример потока вывода MFT \_ \_ \_ на \_ буфер** |
| **\_ \_ \_ фиксированный \_ Размер выборки выходных данных DMO стреамф \_**         | **\_ \_ \_ фиксированный \_ Размер образца потока выходных файлов MFT \_**         |
| **\_выходные данные DMO \_ стреамф \_ удалены**                 | **\_выходной \_ поток MFT \_ удален**                 |
| **\_стреамф выходных данных DMO \_ \_ необязательно**                    | **\_выходной \_ поток MFT \_ необязателен**                    |
| Нет эквивалентного флага.                                   | **\_поток вывода \_ MFT \_ содержит \_ примеры**           |
| Нет эквивалентного флага.                                   | **\_поток вывода \_ MFT \_ может \_ предоставлять \_ образцы**       |
| Нет эквивалентного флага.                                   | **\_поток вывода MFT с \_ \_ отложенным \_ чтением**                  |
| Нет эквивалентного флага.                                   | **\_поток вывода MFT, \_ \_ съемный**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Флаги Сетинпуттипе и Сетаутпуттипе

Дмос: перечисление [**\_ \_ \_ \_ флагов типа Set DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) .

МФТС: перечисление [**\_ \_ \_ \_ флагов типов набора MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| Флаг DMO                        | Флаг MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO \_ Set \_ типеф \_ \_ только тест** | **\_набор MFT \_ \_ только проверка \_ типа**                                                       |
| **DMO \_ Set \_ типеф \_ clear**      | Нет эквивалентного флага. Вместо этого задайте для типа носителя **значение NULL** , чтобы очистить тип носителя. |



 

## <a name="error-codes"></a>Коды ошибок

В следующей таблице показано, как сопоставлять коды ошибок DMO с кодами ошибок MFT. Гибридный объект MFT/DMO должен возвращать коды ошибок DMO из методов [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) и коды ошибок MFT из методов [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . Коды ошибок DMO определены в файле заголовка Медиаерр. h. Коды ошибок MFT определены в файле заголовка мферрор. h.



| Код ошибки DMO                  | Код ошибки MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ инвалидтипе**         | **MF \_ E \_ инвалидтипе**               |
| **DMO \_ E \_ инвалидстреаминдекс**  | **MF \_ E \_ инвалидстреамнумбер**       |
| **DMO \_ E \_ нотакцептинг**        | **MF \_ E \_ нотакцептинг**              |
| **DMO. больше \_ \_ \_ \_ элементов нет**     | **MF \_ E \_ больше \_ \_ типов**           |
| **\_тип DMO \_ E \_ не \_ принят** | **MF \_ E \_ инвалидмедиатипе**          |
| **\_тип DMO \_ E \_ не \_ задан**      | **\_ \_ тип преобразования MF \_ E \_ не \_ задан** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Создание гибридных объектов DMO/MFT

Интерфейс [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) слабо основан на [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), который является основным интерфейсом для объектов мультимедиа DirectX (дмос). Можно создавать объекты, предоставляющие оба интерфейса. Однако это может привести к конфликтам имен, так как интерфейсы имеют некоторые методы с одинаковыми именами. Решить эту проблему можно одним из двух способов.

Решение 1. Включите следующую строку в начало любого CPP файла, содержащего функции MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Это изменяет объявление интерфейса [**имфтрансформ**](/windows/win32/api/mftransform/nn-mftransform-imftransform) , чтобы большинство имен методов были префиксом MFT. Таким образом, [**имфтрансформ::P роцессинпут**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) преобразуется в **Имфтрансформ:: Мфтпроцессинпут**, а [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) сохраняет свое исходное имя. Этот метод наиболее удобен при преобразовании существующего объекта DMO в гибридные объекты DMO или MFT. Вы можете добавить новые методы MFT, не изменяя методы DMO.

Решение 2. Использование синтаксиса C++ для неоднозначности имен, унаследованных от более чем одного интерфейса. Например, объявите версию MFT для [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) следующим образом:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Объявите версию DMO для [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) следующим образом:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

При выполнении внутреннего вызова метода в объекте можно использовать этот синтаксис, но это приведет к переопределению виртуального состояния метода. Для вызова внутри объекта лучше всего использовать следующие объекты:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Таким образом, если вы наследуете от **кмихибридобжект** другой класс и переопределяете метод кмихибридобжект:: имедиаобжект::P роцессинпут, вызывается правильный виртуальный метод. Интерфейсы DMO описаны в документации по пакету SDK для DirectShow.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
