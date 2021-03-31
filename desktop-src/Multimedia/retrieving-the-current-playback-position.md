---
title: Получение текущей позицией воспроизведения
description: Получение текущей позицией воспроизведения
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- звуковая волна, текущая позицией воспроизведения
- волна-Audio Interface, текущее расположение воспроизведения
- Воспроизведение аудио-файлов, Текущая заданная позицией воспроизведения
- Функция Вавеаутжетпоситион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336860"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="de5b5-107">Получение текущей позицией воспроизведения</span><span class="sxs-lookup"><span data-stu-id="de5b5-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="de5b5-108">С помощью функции [**вавеаутжетпоситион**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) можно отслеживать текущую позицией воспроизведения в файле, пока воспроизводится звуковая волна.</span><span class="sxs-lookup"><span data-stu-id="de5b5-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="de5b5-109">Для устройств с аудио-волнами образцами является предпочтительный формат времени, в котором следует представить текущую точку.</span><span class="sxs-lookup"><span data-stu-id="de5b5-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="de5b5-110">Таким образом, текущее расположение устройства аудио-аудио указывается как количество выборок для одного канала с начала аудио-файла.</span><span class="sxs-lookup"><span data-stu-id="de5b5-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="de5b5-111">Чтобы выполнить запрос к текущему положению устройства аудио-аудио, установите для элемента **wType** структуры [**ммтиме**](/previous-versions//dd757347(v=vs.85)) значения Time \_ Samples и передайте эту структуру **вавеаутжетпоситион**.</span><span class="sxs-lookup"><span data-stu-id="de5b5-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="de5b5-112">Структура **ммтиме** может представлять время в одном или нескольких различных форматах, включая миллисекунды, примеры, SMPTE (общество инженеров движения и телевизионных специалистов) и форматы указателей MIDI Song.</span><span class="sxs-lookup"><span data-stu-id="de5b5-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="de5b5-113">Элемент **wType** указывает формат, используемый для представления времени.</span><span class="sxs-lookup"><span data-stu-id="de5b5-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="de5b5-114">Перед вызовом функции, использующей структуру **ммтиме** , необходимо задать **wType** , чтобы указать запрошенный формат времени.</span><span class="sxs-lookup"><span data-stu-id="de5b5-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="de5b5-115">Не забудьте проверить **wType** после вызова, чтобы узнать, поддерживается ли запрошенный формат времени.</span><span class="sxs-lookup"><span data-stu-id="de5b5-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="de5b5-116">Если запрошенный формат времени не поддерживается, драйвер устройства определяет время в альтернативном формате времени и изменяет элемент **wType** на выбранный формат времени.</span><span class="sxs-lookup"><span data-stu-id="de5b5-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="de5b5-117">Дополнительные сведения о структуре **ммтиме** см. в разделе [мультимедийные таймеры](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="de5b5-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 