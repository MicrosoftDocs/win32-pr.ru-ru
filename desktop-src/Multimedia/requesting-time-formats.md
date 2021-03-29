---
title: Запрос форматов времени
description: Запрос форматов времени
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), форматы времени
- MIDI (цифровой интерфейс музыкального инструмента), форматы времени
- Службы MIDI, форматы времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789756"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="937f6-106">Запрос форматов времени</span><span class="sxs-lookup"><span data-stu-id="937f6-106">Requesting Time Formats</span></span>

<span data-ttu-id="937f6-107">В Windows используется структура [**ммтиме**](/previous-versions//dd757347(v=vs.85)) для представления времени в одном или нескольких различных форматах, включая миллисекунды, примеры, SMPTE и форматы указателей MIDI Song.</span><span class="sxs-lookup"><span data-stu-id="937f6-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="937f6-108">Элемент **wType** указывает формат времени.</span><span class="sxs-lookup"><span data-stu-id="937f6-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="937f6-109">Функция [**мидистреампоситион**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) использует структуру **ммтиме** .</span><span class="sxs-lookup"><span data-stu-id="937f6-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="937f6-110">Перед вызовом этой функции необходимо задать элемент **wType** , чтобы указать запрошенный формат времени.</span><span class="sxs-lookup"><span data-stu-id="937f6-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="937f6-111">Чтобы узнать, поддерживается ли запрошенный формат времени, проверьте **wType** после вызова.</span><span class="sxs-lookup"><span data-stu-id="937f6-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="937f6-112">Если запрошенный формат времени не поддерживается, время указывается в альтернативном формате времени, выбранном драйвером устройства, а элемент **wType** изменяется для указания выбранного формата времени.</span><span class="sxs-lookup"><span data-stu-id="937f6-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="937f6-113">Дополнительные сведения о структуре **ммтиме** см. в разделе [мультимедийные таймеры](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="937f6-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="937f6-114">См. также</span><span class="sxs-lookup"><span data-stu-id="937f6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="937f6-115">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="937f6-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 