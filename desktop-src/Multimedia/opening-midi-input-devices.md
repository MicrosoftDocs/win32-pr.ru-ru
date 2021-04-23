---
title: Открытие устройств ввода MIDI
description: Открытие устройств ввода MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Цифровой интерфейс MIDI, устройства ввода
- MIDI (цифровой интерфейс музыкального инструмента), устройства ввода
- запись аудио MIDI, устройств ввода
- Устройства ввода MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), открытие устройств ввода
- MIDI (цифровой интерфейс музыкального инструмента), открытие устройств ввода
- запись звука MIDI, открытие устройств ввода
- Открытие устройств ввода MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790890"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="a5f77-111">Открытие устройств ввода MIDI</span><span class="sxs-lookup"><span data-stu-id="a5f77-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="a5f77-112">Чтобы открыть входное устройство MIDI для записи, используйте функцию [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="a5f77-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="a5f77-113">Эта функция открывает устройство, связанное с указанным идентификатором устройства, и возвращает маркер открытого устройства путем записи маркера в указанное место в памяти.</span><span class="sxs-lookup"><span data-stu-id="a5f77-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="a5f77-114">Если вы используете \_ флаг состояния ввода-вывода MIDI \_ с **мидиинопен**, система использует сообщение [**MIM \_ MOREDATA**](mim-moredata.md) , чтобы предупредить функцию обратного вызова приложения, если она не обрабатывает данные MIDI достаточно быстро, чтобы не допустить входного драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="a5f77-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="a5f77-115">(Сообщение [**mm \_ MIM \_ MOREDATA**](mm-mim-moredata.md) выполняет то же задание с обратными вызовами окна.</span><span class="sxs-lookup"><span data-stu-id="a5f77-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="a5f77-116">Однако по соображениям производительности большинство приложений будет использовать функции обратного вызова вместо обратных вызовов окна.) Если приложение обрабатывает данные MIDI в отдельном потоке, повышение приоритета потока может оказать значительное влияние на способность приложения поддерживать поток данных.</span><span class="sxs-lookup"><span data-stu-id="a5f77-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f77-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a5f77-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f77-118">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="a5f77-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 