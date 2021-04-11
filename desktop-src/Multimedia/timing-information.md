---
title: Сведения о времени
description: Сведения о времени
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), сведения о времени
- MIDI (цифровой интерфейс музыкального инструмента), сведения о времени
- буферы потока, сведения о времени
- Структура МИДИЕВЕНТ
- буферы потоков, формат SMPTE
- буферы потока, время квартала
- буферы потоков, такты
- Формат SMPTE
- время четвертого заметок
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133723"
---
# <a name="timing-information"></a><span data-ttu-id="9e273-113">Сведения о времени</span><span class="sxs-lookup"><span data-stu-id="9e273-113">Timing Information</span></span>

<span data-ttu-id="9e273-114">Сведения о времени для события MIDI хранятся в элементе **двделтатиме** структуры [**мидиевент**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="9e273-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="9e273-115">Время указывается в тактах, как определено в *стандартной спецификации MIDI-файлов 1,0* .</span><span class="sxs-lookup"><span data-stu-id="9e273-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="9e273-116">Длина такта определяется форматом времени и, возможно, темп, связанным с потоком.</span><span class="sxs-lookup"><span data-stu-id="9e273-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="9e273-117">Дополнительные сведения о потоках см. в разделе [MIDI Streams](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="9e273-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="9e273-118">Такт выражается либо в микросекундах в квартал, либо в виде импульсов SMPTE (обществом инженеров и телевизоров движения).</span><span class="sxs-lookup"><span data-stu-id="9e273-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="9e273-119">Приложения, которые отправляют сообщения MIDI по отдельности или используют необработанные сообщения MIDI, используют время квартала и темп сведения для определения длительности такта.</span><span class="sxs-lookup"><span data-stu-id="9e273-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="9e273-120">Приложения, которые предварительно обрабатывают сообщения MIDI, могут хранить затраченное время как количество используемых единиц SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9e273-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="9e273-121">Время в заметке "квартал" обозначается нулевым значением (бит 15) слова "время деления".</span><span class="sxs-lookup"><span data-stu-id="9e273-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="9e273-122">Оставшаяся часть слова содержит тактовые импульсы за квартал.</span><span class="sxs-lookup"><span data-stu-id="9e273-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="9e273-123">Темп, связанный с потоком данных MIDI, хранится в единицах (в микросекундах в четвертом заметке), которые соответствуют *стандартным спецификациям MIDI-файлов 1,0* .</span><span class="sxs-lookup"><span data-stu-id="9e273-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="9e273-124">Например, четвертая заметка в 4/4 времени, использующая темп из 500 000 микросекунд в квартал, будет воспроизводиться с частотой 120 в минуту.</span><span class="sxs-lookup"><span data-stu-id="9e273-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="9e273-125">SMPTE. форматы деления времени полностью задают длину такта без необходимости в сведениях о темп.</span><span class="sxs-lookup"><span data-stu-id="9e273-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="9e273-126">При использовании форматов времени SMPTE можно синхронизировать последовательности MIDI с другими событиями SMPTE, такими как видео или чередующийся звук.</span><span class="sxs-lookup"><span data-stu-id="9e273-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="9e273-127">Время SMPTE указывается с 1 в битовом высоком порядке (бит 15) слова деления времени.</span><span class="sxs-lookup"><span data-stu-id="9e273-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="9e273-128">Оставшаяся часть наиболее значимого байта указывает, что формат SMPTE используется в качестве отрицательных значений.</span><span class="sxs-lookup"><span data-stu-id="9e273-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="9e273-129">Поддерживаемыми форматами SMPTE и соответствующими значениями (в круглых скобках) являются 24 (-24), 25 (-25), 30 (-30) и 30 Drop (-29).</span><span class="sxs-lookup"><span data-stu-id="9e273-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="9e273-130">Младший байт слова времени деления указывает количество тактов на кадр SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9e273-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 