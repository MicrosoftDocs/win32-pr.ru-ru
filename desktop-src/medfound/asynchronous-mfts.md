---
description: В этом разделе описывается асинхронная обработка данных для Media Foundation преобразований (МФТС).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: Асинхронный МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cab2ef683ef22fd22a911c045a1a744f1c0d561b3e8e66d46ca2cf6c6f0ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959524"
---
# <a name="asynchronous-mfts"></a>Асинхронный МФТС

В этом разделе описывается асинхронная обработка данных для Media Foundation преобразований (МФТС).

> [!Note]  
> этот раздел относится к Windows 7 и более поздних версий.

 

-   [Об асинхронном МФТС](#about-asynchronous-mfts)
-   [Общие требования](#general-requirements)
-   [События](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Очистки](#draining)
-   [Очистки](#flushing)
-   [Метки](#markers)
-   [Изменения формата](#format-changes)
-   [Атрибуты](#attributes)
-   [Разблокировка асинхронного МФТС](#unlocking-asynchronous-mfts)
-   [Завершение работы MFT](#shutting-down-the-mft)
-   [Регистрация и перечисление](#registration-and-enumeration)
-   [Связанные темы](#related-topics)

## <a name="about-asynchronous-mfts"></a>Об асинхронном МФТС

когда мфтс был введен в Windows Vista, API был разработан для *синхронной* обработки данных. В этой модели MFT всегда ожидает получения входных данных или ожидания получения выходных данных.

Рассмотрим типичный видеодекодер. Чтобы получить декодированный кадр, клиент вызывает [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Если у декодера достаточно данных для декодирования кадра, **ProcessOutput** блокируется, пока MFT декодирует кадр. В противном случае **ProcessOutput** возвращает **MF_E_TRANSFORM_NEED_MORE_INPUT**, что означает, что клиент должен вызвать [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Эта модель хорошо работает, если декодер выполняет все операции декодирования в одном потоке. Но предположим, что декодер использует несколько потоков для параллельного декодирования кадров. Для лучшей производительности декодер должен получить новые входные данные всякий раз, когда поток декодирования переходит в состояние бездействия. Но скорость, с которой потоки завершают операции декодирования, не будет точно согласована с вызовами клиента [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) и [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), что приведет к потокам, ожидающим работы.

в Windows 7 реализована *асинхронная* обработка на основе событий для мфтс. В этой модели каждый раз, когда таблица MFT требует ввода или вывода данных, она отправляет клиенту событие.

## <a name="general-requirements"></a>Общие требования

В этом разделе описывается, как асинхронные МФТС отличаются от синхронных файлов MFT. За исключением случаев, оговоренных в этом разделе, две модели обработки одинаковы. (В частности, согласование формата одинаково.)

Асинхронная Таблица MFT должна реализовывать следующие интерфейсы:

-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**имфшутдовн**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>События

Асинхронная MFT использует следующие события для сигнализации состояния обработки данных:



| Событие                                                    | Описание                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [метрансформнидинпут](metransformneedinput.md)         | Посылается, когда MFT может принимать больше входных данных.                          |
| [метрансформхавеаутпут](metransformhaveoutput.md)       | Посылается, когда файл MFT содержит выходные данные.                                     |
| [метрансформдраинкомплете](metransformdraincomplete.md) | Посылается после завершения операции очистки. См. раздел [сток](#draining). |
| [метрансформмаркер](metransformmarker.md)               | Посылается, когда маркер обрабатывается. См. раздел [маркеры](#markers).           |



 

Эти события отправляются по внешнему каналу. Важно понимать разницу между внешними и внешними событиями в контексте MFT.

Исходная структура MFT поддерживает события *с чередованием* . Событие с чередованием содержит сведения о потоке данных, например сведения об изменении формата. Клиент отправляет события в основном файле MFT, вызывая [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Таблица MFT может отправить события с внутренним каналом обратно клиенту в методе [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . (В частности, события передаются в элемент **певентс** структуры [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .)

MFT отправляет события внешнего вида через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) следующим образом:

1.  MFT реализует интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , как описано в статье [генераторы событий мультимедиа](media-event-generators.md).
2.  Клиент вызывает **IUnknown:: QueryInterface** в MFT для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Асинхронный MFT должен предоставлять этот интерфейс. Синхронный МФТС не должен предоставлять этот интерфейс.
3.  Клиент вызывает [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) и [**Имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) для получения событий, находящихся вне диапазона, из MFT.

## <a name="processinput"></a>ProcessInput

Метод [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) изменяется следующим образом:

1.  При запуске потоковой передачи клиент отправляет сообщение [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
2.  Во время потоковой передачи MFT запрашивает данные, отправляя событие [метрансформнидинпут](metransformneedinput.md) . Данные события являются идентификатором потока.
3.  Для каждого события [метрансформнидинпут](metransformneedinput.md) клиент вызывает метод [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) для указанного потока.
4.  По завершении потоковой передачи клиент может вызвать [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .

Примечания по реализации:

-   Таблица MFT не должна отсылать никаких событий [метрансформнидинпут](metransformneedinput.md) , пока не получит сообщение [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
-   Во время потоковой передачи MFT может отправить события [метрансформнидинпут](metransformneedinput.md) в любое время.
-   MFT должно поддерживать количество ожидающих событий [метрансформнидинпут](metransformneedinput.md) . Любой вызов метода [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , который не соответствует событию метрансформнидинпут, должен возвращать **MF_E_NOTACCEPTING**.
-   Когда MFT получает сообщение [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) , оно сбрасывает число ожидающих событий [метрансформнидинпут](metransformneedinput.md) в ноль.
-   Таблица MFT не должна отсылать никаких событий [метрансформнидинпут](metransformneedinput.md) после получения сообщения [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .
-   Если метод [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) вызывается до [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) или после [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), он должен возвращать **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

Метод [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) изменяется следующим образом:

1.  Каждый раз, когда файл MFT имеет выходные данные, он отправляет событие [метрансформхавеаутпут](metransformhaveoutput.md) .
2.  Для каждого события [метрансформхавеаутпут](metransformhaveoutput.md) клиент вызывает [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Примечания по реализации:

-   Если клиент вызывает [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в любое другое время, метод возвращает **E_UNEXPECTED**.
-   Асинхронная Таблица MFT не должна возвращать **MF_E_TRANSFORM_NEED_MORE_INPUT** из метода [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Если таблица MFT требует больше входных данных, она отправляет событие [метрансформнидинпут](metransformneedinput.md) .

## <a name="draining"></a>Очистки

Очистка MFT приводит к тому, что MFT создает как можно больше выходных данных, так как это может быть уже отправленные входные данные. Сток асинхронной MFT работает следующим образом:

1.  Клиент отправляет сообщение [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) .
2.  Таблица MFT продолжит отсылать события [метрансформхавеаутпут](metransformhaveoutput.md) , пока не будет больше данных для обработки. В течение этого времени события [метрансформнидинпут](metransformneedinput.md) не отправляются.
3.  После того как MFT отправляет Последнее событие [метрансформхавеаутпут](metransformhaveoutput.md) , оно отправляет событие [метрансформдраинкомплете](metransformdraincomplete.md) .

После завершения очистки Таблица MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока не получит сообщение [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) от клиента.

## <a name="flushing"></a>Очистки

Клиент может очистить MFT, отправив сообщение [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) . MFT удаляет все входные и выходные примеры, которые он удерживает.

Таблица MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока не получит сообщение [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) от клиента.

## <a name="markers"></a>Метки

Клиент может пометить точку в потоке, отправив сообщение [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) . Основная таблица MFT реагирует следующим образом:

1.  MFT создает столько выходных образцов, сколько можно из существующих входных данных, отправляя событие [метрансформхавеаутпут](metransformhaveoutput.md) для каждого выходного примера.
2.  После создания всех выходных данных MFT отправляет событие [метрансформмаркер](metransformmarker.md) . Это событие должно быть отправлено после всех событий [метрансформхавеаутпут](metransformhaveoutput.md) .

Например, предположим, что у декодера достаточно входных данных для создания четырех выходных образцов. Если клиент отправляет [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) сообщение, файл MFT будет ставить в очередь четыре [метрансформхавеаутпут](metransformhaveoutput.md) события (по одному на каждый пример вывода), за которыми следует событие [метрансформмаркер](metransformmarker.md) .

Сообщение маркера похоже на сообщение стока. Однако сток считается перерывом в потоке, а маркер — нет. Сток и маркеры имеют следующие отличия.

Очистки

-   При стоке MFT не отправляет события [метрансформнидинпут](metransformneedinput.md) .
-   MFT удаляет все входные данные, которые не могут быть использованы для создания образца выходных данных.
-   Некоторые МФТС создают "хвост" в конце данных. Например, звуковые эффекты, такие как переглаголы или эхо, создают дополнительные данные после остановки входных данных. Таблица MFT, которая создает хвост, должна сделать это в конце операции очистки.
-   После завершения очистки MFT помечает следующий выходной пример атрибутом [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) , чтобы указать на ненепрерывность потока.

Фломастер

-   Таблица MFT продолжит отправлять события [метрансформнидинпут](metransformneedinput.md) перед отправкой события маркера.
-   Таблица MFT не удаляет входные данные. Если имеются частичные данные, они должны обрабатываться после точки маркера.
-   MFT не создает хвост в точке маркера.
-   Таблица MFT не устанавливает флаг небесперебойности после точки маркера.

## <a name="format-changes"></a>Изменения формата

Асинхронная Таблица MFT должна поддерживать динамические изменения формата, как описано в разделе [Обработка изменений потока](handling-stream-changes.md).

## <a name="attributes"></a>Атрибуты

Асинхронная Таблица MFT должна реализовывать метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , возвращающий допустимое хранилище атрибутов. К асинхронному МФТС применяются следующие атрибуты:



| attribute                                                                                    | Описание                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | MFT должен присвоить этому атрибуту **значение true** (1). Клиент может запросить этот атрибут, чтобы определить, является ли MFT асинхронным. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | MFT должен присвоить этому атрибуту **значение true** (1). Клиент может предположить, что этот атрибут задан.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Разблокировка асинхронного МФТС

Асинхронные МФТС несовместимы с исходной моделью обработки данных MFT. Чтобы избежать нарушения работы асинхронных МФТС, определяется следующий механизм:

<dl> Клиент вызывает <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">имфтрансформ:: OutAttribute</a> для MFT.  
Клиент запрашивает для этого атрибута <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> . Для асинхронной MFT значение этого атрибута равно **true**.  
Чтобы разблокировать MFT, клиент должен присвоить атрибуту <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> **значение true**.  
</dl>

Пока клиент не разблокирует MFT, все методы [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) должны возвращать **MF_E_TRANSFORM_ASYNC_LOCKED**, за исключением следующих:

-   [**Имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (все асинхронные МФТС)
-   [**Имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (все асинхронные МФТС)
-   [**Имфтрансформ:: жетаутпуткурренттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (только кодировщики)
-   [**Имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (только кодировщики)
-   [**Имфтрансформ:: жетстреамкаунт**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (все асинхронные МФТС)
-   [**Имфтрансформ:: жетстреамидс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (все асинхронные МФТС)

В следующем коде показано, как разблокировать асинхронную таблицу MFT:


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Завершение работы MFT

Асинхронный МФТС должен реализовывать интерфейс [**имфшутдовн**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) .

-   [**Завершение работы**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). Таблица MFT должна завершить свою очередь событий. При использовании стандартной очереди событий вызовите [**имфмедиаевенткуеуе:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Кроме того, MFT может освободить другие ресурсы. Клиент не должен использовать MFT после вызова метода **Shutdown**.
-   [**Жетшутдовнстатус**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): после [**завершения работы**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) вызывается Таблица MFT, которая должна возвращать значение **MFSHUTDOWN_COMPLETED** в параметре *пстатус* . Он не должен возвращать значение **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Регистрация и перечисление

Чтобы зарегистрировать асинхронную таблицу MFT, вызовите функцию [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) и установите флаг **MFT_ENUM_FLAG_ASYNCMFT** в параметре *flags* . (Ранее этот флаг зарезервирован.)

Чтобы перечислить асинхронные МФТС, вызовите функцию [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) и установите флаг **MFT_ENUM_FLAG_ASYNCMFT** в параметре *flags* . Для обратной совместимости функция [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) не перечисляет асинхронные МФТС. В противном случае установка асинхронной таблицы MFT на компьютере пользователя может нарушить работу существующих приложений.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



