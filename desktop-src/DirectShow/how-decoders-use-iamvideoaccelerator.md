---
description: Использование IAMVideoAccelerator в декодерах
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Использование IAMVideoAccelerator в декодерах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989902"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Использование IAMVideoAccelerator в декодерах

Интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) обеспечивает универсальные операции ускорения видео, включая ускорение видео DirectX (ва). Для ускорения, отличного от DirectX, декодер и видеодрайвер должны соответствовать стандартному протоколу.

В этом разделе описывается общий порядок операций, которым должен следовать любой декодер при использовании этого интерфейса. Дополнительные сведения об декодерах, поддерживающих DirectX, можно найти в подокне [сопоставление видео DirectX с иамвидеоакцелератор](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> Этот интерфейс доступен в Windows 2000 и более поздних версиях.

 

Интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) предоставляется во входном закрепления [микшера наложения](overlay-mixer-filter.md) или микширования видео (VMR). Интерфейс [**иамвидеоакцелераторнотифи**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) предоставляется на выходном ПИН-коде декодера. Последовательность событий для соединения с контактами фильтра выглядит следующим образом:

1.  Диспетчер графов фильтров вызывает [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) на выходном ПИН-коде фильтра декодера. [**\_ \_ Тип носителя AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) является необязательным параметром.
    -   [**AM \_ \_Тип носителя**](/windows/win32/api/strmif/ns-strmif-am_media_type) — это структура данных, описывающая тип носителя. Он содержит идентификатор GUID мажортипе (который в нашем случае должен быть видео типа MEDIATYPE \_ ), идентификатор GUID подтипа (который в нашем случае должен быть GUID ускорителя) и множество других вещей. Одно из этих действий — идентификатор GUID типа, содержащий сведения о носителе, в том числе в нашем примере ширина и высота несжатого видеоизображения, скорее всего, в структуре [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo), [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
    -   Структура [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , если она есть, предписывает декодеру работать с использованием указанного типа носителя, который может быть "полностью указан" или "частично указан". Если параметр полностью указан, декодер обычно просто пытается работать с этим типом носителя. Если указано частичное значение, будет предпринята попытка найти "полностью заданный" режим работы, который можно использовать для подключения способом, согласованным с "частично указанным" типом носителя.
    -   Обычным способом поиска "полностью определенного" типа носителя, используемого для соединения, является простое выполнение по списку всех "полностью определенных" типов носителей, поддерживаемых выходным закреплением, который совместим с "частично заданным" типом носителя и пытается подключиться к ним до тех пор, пока они не будут успешными. Как правило, процесс будет похож \_ \_ , если в вызове [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) не содержится тип носителя am, но с выходным закреплением необходимо проверить все типы носителей.
2.  Если декодеру требуется проверить, поддерживается ли указанный [**\_ \_ тип носителя AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) (включая GUID ускорителя), с помощью последующего входного ПИН-кода, он может вызвать [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (с идентификатором GUID ускорителя в качестве подтипа для **\_ \_ типа носителя AM**), или же можно просто попытаться подключиться к этому ПИН-коду, как описано в элементе 5 ниже.
3.  Если декодер не знает, какие идентификаторы GUID ускорителя входных данных поддерживаются, и не желает предложить только некоторый конкретный идентификатор GUID ускорителя видео путем вызова [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept), декодер может вызвать [**Иамвидеоакцелератор:: жетвидеоакцелераторгуидс**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) , чтобы получить список идентификаторов GUID ускорителей, поддерживаемых ПИН-кодом.
4.  Для некоторых определенных идентификаторов GUID ускорителя можно вызвать [**иамвидеоакцелератор:: жетункомпформатссуппортед**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) , чтобы получить список форматов пикселей **ддпикселформат** , которые можно использовать для визуализации определенного идентификатора GUID ускорителя видео. Возвращаемый список должен рассматриваться в порядке убывания приоритета (т. е. с наиболее предпочтительным форматом, указанным первым).
5.  Декодер вызывает [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), передавая ему [**\_ \_ тип носителя AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) с правильным идентификатором GUID ускорителя в качестве подтипа для типа мультимедиа. Таким образом настраивается соединение для операции, включая создание несжатых выходных областей вывода (которые выделяются с использованием ширины и высоты, находящихся в **\_ \_ типе носителя AM**), а также число выводимых поверхностей, найденных с помощью вызова, описанного ниже, и других сведений, доступных для использования видео-ускорителем, например самого GUID ускорителя видео. Если последующий входной ПИН-код отклоняет идентификатор GUID ускорителя видео или другой аспект подключения, это может привести к сбою **Ипин:: рецеивеконнектион** . Если **Ипин:: рецеивеконнектион** завершается ошибкой, это указывается в возвращенном значении **HRESULT**, и декодер может попытаться снова выполнить вызов, например с новым идентификатором GUID ускорителя в структуре **\_ \_ типа мультимедиа** .
    -   [!Note]  
        > Это еще один способ (и самый оптимальный способ), с помощью которого декодер определяет, что поддерживается нисходящим входным закреплением — просто вызывая [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) и пытаясь подключиться, а затем проверяя, была ли попытка соединения успешной.

         

    -   Во время выполнения [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)средство визуализации вызывает [**Иамвидеоакцелераторнотифи:: жетункомпсурфацесинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)декодера, передавая ему GUID ускорителя и структуру [**амваункомпбуфферинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) , чтобы определить, сколько несжатых поверхностей следует выделить. Декодер заполняет и возвращает структуру, которая содержит минимальное и максимальное количество поверхностей, выделяемых для конкретного типа, и структуру **ддпикселформат** , описывающую формат пикселей для выделяемых поверхностей.
    -   [!Note]  
        > Ничто не передается декодеру в вызове [**иамвидеоакцелераторнотифи:: жетункомпсурфацесинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) , отличном от GUID ускорителя видео.

         

6.  Модуль подготовки отчетов вызывает метод [**иамвидеоакцелераторнотифи:: сетункомпсурфацесинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)декодера, передавая декодеру фактическое количество выделенных несжатых поверхностей.
7.  Модуль подготовки отчетов вызывает [**иамвидеоакцелераторнотифи:: жеткреатевидеоакцелератордата**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) декодера для получения любых данных, необходимых для инициализации видео Accelerator.
8.  Декодер вызывает [**иамвидеоакцелератор:: жеткомпбуфферинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo), передавая ему GUID ускорителя видео, структуру [**амваункомпдатаинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) и число типов сжатых буферов, чтобы возвратить набор структур данных [**амвакомпбуфферинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , один из которых соответствует каждому типу сжатого буфера данных, используемого идентификатором GUID ускорителя видео.
    -   Структура [**амваункомпдатаинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) содержит ширину и высоту декодированных несжатых данных (в пикселях) и ддпикселформат несжатого изображения.
    -   Возвращаемые структуры данных [**амвакомпбуфферинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) содержат:
        -   Количество сжатых буферов, необходимых для конкретного типа.
        -   Ширина и высота создаваемой области (поля, которые могут или не имеют фактического значения).
            > [!Note]  
            > В настоящее время операция выделения памяти на устройстве DirectDraw для сжатых буферов не обеспечивает ширину или высоту этих поверхностей, которая должна быть больше или равна 2 ^ 15, хотя вызов выделения поверхности может не овертлися, если это ограничение нарушено. Таким образом, драйвер может структурировать запросы к сжатой буферной памяти, чтобы избежать таких крайних размеров. Например, вместо запроса буфера с Width = "1" и Height = "65536" драйвер должен запросить буфер Width = "1024" и Height = "64".

             

        -   Общее число байтов, используемых поверхностью.
        -   Структура типа **DDSCAPS2** , определяющая объект директдравсурфаце, описывающий возможности создания поверхностей для хранения сжатых данных.
        -   ДДПИКСЕЛФОРМАТ, описывающий формат пикселей, используемый для создания поверхностей для хранения сжатых данных (поле, которое может иметь или не иметь никакого фактического значения).

> [!Note]  
> Вызовы средства визуализации к некоторым методам интерфейса [**иамвидеоакцелераторнотифи**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) декодера могут (и обычно) происходить внутри вызова декодера [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection). В частности, это относится к следующим параметрам:
>
> -   [**Иамвидеоакцелераторнотифи:: жетункомпсурфацесинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**Иамвидеоакцелераторнотифи:: сетункомпсурфацесинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)и
> -   [**Иамвидеоакцелераторнотифи:: жеткреатевидеоакцелератордата**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Для поддержки изменений динамического формата декодер также может вызвать [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) и другие методы в описании, когда фильтры подключены и выполняются. Эта возможность предусмотрена для поддержки динамических изменений формата (хотя и не в H. 263, приложение P, имеет смысл, так как все наборы данных запускаются снова с нуля и все сведения о справочных изображениях теряются).

 

Ниже приведено описание использования [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) во время операции после инициализации.

1.  Для каждой несжатой поверхности декодер вызывает [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , чтобы начать обработку, чтобы создать выходной рисунок. При этом декодер отправляет структуру [**амвабегинфрамеинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) .
    -   Структура [**амвабегинфрамеинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) содержит индекс для буфера назначения, указатель на некоторые данные для последующей отправки и указатель на место, где ускоритель может поместить некоторые данные для чтения декодера.
    -   Примечание 1. в действительности ускоритель не получает индекс буфера назначения, так как он преобразуется модулем подготовки отчетов перед переходом к нисходящему.
    -   Примечание 2. [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) можно вызывать несколько раз между вызовами [**Иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   Примечание 3. в операции интерфейса нет предположения, что [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) и [**Иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) необходимо вызывать для обработки каждого отдельного изображения в битовый поток.

        Что делает [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , что касается интерфейса, создает ассоциацию внутри модуля подготовки отчетов между индексом и несжатой поверхностью. Он также предоставляет средства для вызова определенной функции в драйвере устройства (с поддержкой передачи произвольных данных между декодером и драйвером устройства).

        (Однако в операции DirectX ва требуется вызывать [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) и [**Иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) для обработки каждого отдельного изображения в битовый поток.)

2.  Для отправки несжатых данных в ускоритель вызовов декодера вызывает:
    -   [**Иамвидеоакцелератор:: куерирендерстатус**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) , чтобы определить, является ли буфер надежным для чтения или записи в.
    -   [**Иамвидеоакцелератор::-buffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) блокируется и получает доступ к указанному буферу (если он ранее не вызывал этот объект для получения доступа). Для получения копии содержимого последнего несжатого выходного изображения, для которого была вызвана [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , также можно использовать метод « **buffer** », предоставляя [**иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) для этого индекса буфера назначения. Если DDI возвращает состояние отрисовки ДДЕРР \_ васстиллдравинг для запрошенного буфера, то цикл сна будет работать в методе- **buffer** до тех пор, пока не будет сброшено это условие. Чтобы вызвать метод **buffer**, декодеру потребуется определенная информация из структуры данных [**амвакомпбуфферинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , полученной путем вызова [**иамвидеоакцелератор:: жеткомпбуфферинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**Иамвидеоакцелератор:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) для указания того, что данные в наборе сжатых буферов, как указано в массиве структур данных [**амвабуфферинфо**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) , должны быть обработаны. Код функции Двфунктион передается драйверу в этом вызове. Указатель Лпприватеинпутдата также передается в некоторые данные для последующей отправки, а указатель Лпприватеаутпутдата передается в место, где нисходящий процесс может поместить некоторые данные для чтения декодера.
    -   [**Иамвидеоакцелератор:: релеасебуффер**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) указывает, что декодер завершил использование указанного буфера в течение некоторого времени и больше не требует блокированного доступа к буферу. (Если декодер хочет продолжать использовать буфер, он может просто не вызывать **иамвидеоакцелератор:: релеасебуффер** , что позволяет избежать необходимости вызывать [**иамвидеоакцелератор::-buffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) , пока не будет действительно больше не использовать буфер.) Декодер не должен записывать в буфер после вызова [**EXECUTE**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) , пока [**куерирендерстатус**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) указывает, что буфер является защищенным для записи.
3.  Чтобы завершить обработку выходных данных для буфера назначения, декодер вызывает [**иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Он может передать некоторые произвольные данные с помощью этого вызова, и это все, что происходит в результате этого вызова. Он не отправляет индекс буфера назначения в этом вызове, поэтому он не может указать сочетанию клавиш, что конечный буфер завершается, если эта индикация не содержится во всех передаваемых данных.
4.  Чтобы отобразить кадр, декодер вызывает [**иамвидеоакцелератор::D исплайфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) с индексом отображаемого кадра и структурой [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , содержащей метки времени начала и окончания и соответствующие флаги, такие как **двтипеспеЦификфлагс** в структуре [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) , и **двинтерлацефлагс** в структуре [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Декодер должен убедиться, что все операции распаковки, влияющие на содержимое кадра, завершены перед вызовом **дисплайфраме**.
5.  Наконец, после завершения всей обработки декодер должен указывать на завершение всех оставшихся выходных кадров, вызывая [**иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) и освобождая все заблокированные буферы путем вызова [**Иамвидеоакцелератор:: релеасебуффер**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) для каждого неосвобожденного буфера.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы и спецификации декодера](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



