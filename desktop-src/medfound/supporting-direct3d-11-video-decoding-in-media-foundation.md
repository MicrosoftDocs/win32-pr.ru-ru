---
description: В этом разделе описывается поддержка Microsoft Direct3D 11 в Microsoft Media Foundation декодере.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Поддержка декодирования видео Direct3D 11 в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542f7244922dc7947f22e4d33027fdcac1962fe5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664823"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Поддержка декодирования видео Direct3D 11 в Media Foundation

В этом разделе описывается поддержка Microsoft Direct3D 11 в Microsoft Media Foundation декодере. В частности, он описывает взаимодействие между декодером и модулем подготовки видео. В этом разделе не описывается, как реализовать операции декодирования.

-   [Обзор](#overview)
-   [Открытие маркера устройства](#open-a-device-handle)
-   [Поиск конфигурации декодера](#find-a-decoder-configuration)
-   [Откат к декодированию программного обеспечения](#fallback-to-software-decoding)
-   [Выделение несжатых буферов](#allocating-uncompressed-buffers)
-   [Декодирование](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [См. также](#related-topics)

## <a name="overview"></a>Обзор

В оставшейся части этого раздела используются следующие термины:

-   **Программный декодер**. Программный декодер — это Media Foundation преобразование (MFT), которое получает сжатые образцы видео и выводит несжатые видеокадры.
-   **Устройство декодера**. Устройство декодера — это ускоритель видео, который реализуется графическим драйвером. Устройство декодера выполняет операции декодирования с ускоренной декодированием.
-   **Конвейер**. В конвейере размещается программный декодер и доставляются буферы в программный декодер и из него. В зависимости от приложения конвейер может быть [сеансом мультимедиа](media-session.md), [модулем чтения исходного](source-reader.md)кода или кодом приложения, который непосредственно вызывает таблицу MFT.

Чтобы выполнить декодирование с помощью Direct3D 11, программный декодер должен иметь указатель на устройство Direct3D 11. Устройство Direct3D 11 создается извне программного декодера. В сценарии [сеанса мультимедиа](media-session.md) модуль подготовки видео создает устройство Direct3D 11. В сценарии [модуля чтения исходного кода](source-reader.md) обычно приложение создает устройство Direct3D 11.

Диспетчер устройств DXGI используется для совместного использования компонентов Direct3D 11 между компонентами. Диспетчер устройств DXGI предоставляет интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Конвейер устанавливает указатель **имфдксгидевицеманажер** на программном декодере, отправляя сообщение MFT с указанием сообщения [**\_ \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) .

На следующей схеме показана связь между программным декодером, Direct3D 11 и конвейером.

![Схема, на которой показан программный декодер и Диспетчер устройств DXGI.](images/d3d11video01.png)

Ниже приведены основные шаги, которые должен выполнить программный декодер для поддержки Direct3D 11 в Media Foundation.

1.  Откройте обработчик для устройства Direct3D 11.
2.  Найдите конфигурацию декодера.
3.  Выделение несжатых буферов.
4.  Декодирование кадров.

Эти действия более подробно описаны в оставшейся части этого раздела.

## <a name="open-a-device-handle"></a>Открытие маркера устройства

В MFT для декодера используется диспетчер устройств DXGI для получения маркера на устройство Direct3D 11. Чтобы открыть маркер устройства, выполните следующие действия.

1.  В MFT декодера необходимо предоставить атрибуту [MF \_ SA \_ D3D11 с \_ поддержкой](mf-sa-d3d11-aware.md) значение **true**.
2.  Загрузчик топологии запрашивает этот атрибут путем вызова [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Значение **true** указывает, что MFT поддерживает Direct3D 11.
3.  Загрузчик топологии вызывает [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением из [**таблицы \_ MFT \_ Set \_ D3D Message \_ Manager**](mft-message-set-d3d-manager.md) . Параметр *улпарам* — это указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) на диспетчер устройств DXGI. Запросите этот указатель для интерфейса [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Вызовите [**имфдксгидевицеманажер:: опендевицехандле**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) , чтобы получить маркер устройства Direct3D 11.
5.  Чтобы получить указатель на устройство Direct3D 11, вызовите [**имфдксгидевицеманажер:: жетвидеосервице**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Передайте маркер устройства и значение **IID \_ ID3D11Device**. Метод возвращает указатель на интерфейс [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .
6.  Чтобы получить указатель на ускоритель видео, вызовите [**имфдксгидевицеманажер:: жетвидеосервице**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) еще раз. На этот раз передайте маркер устройства и значение **IID \_ ID3D11VideoDevice**. Метод возвращает указатель на интерфейс [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
7.  Вызовите [**ID3D11Device:: жетиммедиатеконтекст**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) , чтобы получить указатель [**ссылку ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) .
8.  Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для [**ссылку ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) , чтобы получить указатель [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) .
9.  Рекомендуется использовать многопотоковую защиту в контексте устройства, чтобы избежать проблем взаимоблокировки, которые иногда могут возникнуть при вызове [**ID3D11VideoContext:: жетдекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) или [**ID3D11VideoContext:: релеаседекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Чтобы установить защиту с несколькими потоками, сначала вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) , чтобы получить указатель [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) . Затем вызовите [**ID3D10Multithread:: сетмултисреадпротектед**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), передав **значение true** для *бмтпротект*.

## <a name="find-a-decoder-configuration"></a>Поиск конфигурации декодера

Чтобы выполнить декодирование, программный декодер должен найти совместимую конфигурацию, поддерживаемую устройством декодера, включая формат целевого объекта подготовки к просмотру. Этот шаг выполняется внутри метода [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , как показано ниже.

1.  Проверьте тип входного носителя. Если тип отклонен, пропустите оставшиеся шаги и возвратите код ошибки.
2.  Вызовите [**ID3D11VideoDevice:: жетвидеодекодерпрофилекаунт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) , чтобы получить количество поддерживаемых профилей.
3.  Вызовите метод [**ID3D11VideoDevice:: жетвидеодекодерпрофиле**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) , чтобы перечислить профили и получить идентификаторы GUID профиля.
4.  Найдите идентификатор GUID профиля, который соответствует формату видео и возможностям программного декодера. Например, декодер MPEG-2 будет искать в **D3D11 \_ декодера \_ \_ MPEG2 \_ мокомп**, D3D11,**\_ профиль кодирования \_ \_ MPEG2 \_ идкт** и D3D11 декодера с многоформатным кодировщиком **\_ \_ \_ MPEG2 \_ ВЛД**.
5.  Если найден подходящий GUID декодера, проверьте выходной формат, вызвав метод [**ID3D11VideoDevice:: чекквидеодекодерформат**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) . Передайте GUID декодера и значение **\_ формата DXGI** , которое указывает формат целевого объекта подготовки к просмотру.
6.  Затем найдите подходящую конфигурацию для декодера.
    1.  Вызовите [**ID3D11VideoDevice:: жетвидеодекодерконфигкаунт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) , чтобы получить количество конфигураций декодера. Передайте тот же GUID устройства декодера вместе с структурой [**D3D11 \_ \_ видеодекодера \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) , описывающей предложенный формат целевого объекта рендеринга.
    2.  Вызовите [**ID3D11VideoDevice:: жетвидеодекодерконфиг**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) , чтобы перечислить конфигурации декодера.

В методе [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) Возвращает формат видео без сжатия, основанный на предложенном формате целевого объекта подготовки к просмотру.

В методе [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Проверьте тип носителя в соответствии с форматом целевого объекта прорисовки.

## <a name="fallback-to-software-decoding"></a>Откат к декодированию программного обеспечения

Возможно, MFT не удается найти конфигурацию. Например, графический драйвер может не поддерживать правильные возможности. В этом случае MFT должно возвращаться к программному декодированию, как показано ниже.

1.  Методы [**сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) и [**сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) должны возвращать **MF \_ E \_ неподдерживаемого \_ \_ типа D3D**.
2.  В ответ загрузчик топологии будет отправлять сообщение MFT с указанием значения **null** для параметра *улпарам* . [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)
3.  Основная таблица освобождает указатель на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Загрузчик топологии повторно согласовывает тип носителя.

На этом этапе MFT может использовать программное декодирование.

## <a name="allocating-uncompressed-buffers"></a>Выделение несжатых буферов

Декодер отвечает за выделение текстур Direct3D 11 для использования в качестве несжатых буферов видео. Атрибут [ \_ \_ счетчика с минимальным \_ \_ \_ количеством выходных данных для SA](mf-sa-minimum-output-sample-count.md) по протоколу MF в атрибутах выходного потока (см.[**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) используется для определения количества поверхностей, выделяемых декодером для использования модулем подготовки видео для дечередования. Декодер должен использовать это значение, привязанное к некоторым разумным верхним и нижним ограничениям, например 3-32. Последовательное содержимое см. в разделе [ \_ \_ минимальное \_ \_ \_ число \_ выборок для учетных данных MF SA](mf-sa-minimum-output-sample-count-progressive.md).

В методе [**имфтрансформ:: жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) Задайте флаг **\_ \_ \_ \_ Samples в выходной поток** MFT в структуре [**\_ \_ \_ сведений потока вывода MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) . Этот флаг уведомляет сеанс мультимедиа о том, что MFT выделяет свои собственные выходные примеры. Чтобы выделить выходные образцы, MFT выполняет следующие действия:

1.  Создайте массив двумерных текстур, вызвав [**ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). В структуре [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) задайте **размера массива** равным количеству поверхностей, которое требуется декодеру. В том числе:
    -   Поверхности для кадров ссылок.
    -   Поверхности для разчередования (три поверхности).
    -   Поверхности, необходимые декодеру для буферизации.

    Флаги привязки (**биндфлагс**) должны включать флаг **\_ \_ декодера привязки D3D11** и все флаги привязки, заданные с помощью атрибута [MF \_ SA \_ D3D11 \_ биндфлагс](mf-sa-d3d11-bindflags.md) в атрибутах потока вывода.
2.  Для каждой поверхности в массиве текстуры вызовите [**ID3D11VideoDevice:: креатевидеодекодераутпутвиев**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) , чтобы создать представление вывода видеодекодера. Во время декодирования эти представления вывода будут переданы методу [**ID3D11VideoContext::D екодербегинфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) .
3.  Для каждой поверхности в массиве текстуры создайте пример носителя, как показано ниже.
    1.  Создайте буфер мультимедиа DXGI, вызвав функцию [**мфкреатедксгисурфацебуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) . Передайте указатель [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) и смещение для каждого элемента в массиве текстуры. Функция возвращает указатель [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
    2.  Создайте пустой образец носителя, вызвав функцию [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . Установите параметр *пунксурфаце* равным **null**. Функция возвращает указатель [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
    3.  Вызовите [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) , чтобы добавить буфер мультимедиа в образец.

Следует уничтожить все созданные текстуры одновременно, а не только некоторые и продолжить использовать напоминание.

## <a name="decoding"></a>Декодирование

Чтобы создать устройство декодера, вызовите метод [**ID3D11VideoDevice:: креатевидеодекодер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). Метод возвращает указатель на интерфейс [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) . Декодирование должно происходить внутри метода [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . В каждом кадре вызовите [**имфдксгидевицеманажер:: тестдевице**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) , чтобы проверить доступность DXGI. Если устройство изменилось, программный декодер должен повторно создать устройство декодера следующим образом:

1.  Закройте обработчик устройства, вызвав [**имфдксгидевицеманажер:: клоседевицехандле**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Освободите все ресурсы, связанные с предыдущим устройством Direct3D 11, включая интерфейсы [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder), [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext), [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)и [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) .
3.  Откройте новый маркер устройства.
4.  Согласование новой конфигурации декодера, как описано выше в разделе [Поиск конфигурации декодера](#find-a-decoder-configuration). Этот шаг необходим, так как возможности устройства могли измениться.
5.  Создайте новое устройство декодера.

Предполагая, что маркер устройства является допустимым, процесс декодирования работает следующим образом:

1.  Получить доступную поверхность, которая сейчас не используется. Изначально доступны все поверхности.
2.  Запросите пример носителя для интерфейса [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Вызовите метод [**имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) и укажите указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . (Этот интерфейс должен быть реализован программным декодером.) Когда модуль подготовки видео освобождает пример, будет вызван обратный вызов. Используйте этот обратный вызов, чтобы отследить, какие образцы доступны в настоящее время и какие из них используются.
4.  Вызовите [**ID3D11VideoContext::D екодербегинфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Передайте указатели на интерфейс [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) для устройства декодера и интерфейс [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) для представления выходных данных.
5.  Сделайте следующее или несколько раз:
    1.  Вызовите метод [**ID3D11VideoContext:: жетдекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) , чтобы получить буфер.
    2.  Заполните буфер.
    3.  Вызовите [**ID3D11VideoContext:: релеаседекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Вызовите [**ID3D11VideoContext:: субмитдекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Этот метод указывает устройству декодера выполнить операции декодирования в кадре.
6.  Вызовите [**ID3D11VideoContext::D екодерендфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) , чтобы сообщить о завершении декодирования для текущего кадра.

Direct3D 11 использует те же структуры данных, что и ДКСВА 2,0 для операций декодирования. Для исходного набора профилей ДКСВА (для H. 261, H. 263 и MPEG-2) эти структуры данных описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Внутри каждой пары вызовов [**декодербегинфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) и [**субмитдекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) вы можете вызывать [**жетдекодербуффер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) несколько раз, но только один раз для каждого типа буфера. Если один и тот же тип буфера дважды используется без вызова **субмитдекодербуффер**, данные в буфере будут перезаписаны.

## <a name="related-topics"></a>См. также

<dl> <dt>

[API-интерфейсы видео Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Ускорение видео DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
