---
title: Типы событий MIDI
description: Типы событий MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Цифровой интерфейс MIDI, типы событий
- MIDI (цифровой интерфейс музыкального инструмента), типы событий
- Структура МИДИЕВЕНТ
- буферы потоков, типы событий MIDI
- Типы событий MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069983"
---
# <a name="midi-event-types"></a><span data-ttu-id="55bab-108">Типы событий MIDI</span><span class="sxs-lookup"><span data-stu-id="55bab-108">MIDI Event Types</span></span>

<span data-ttu-id="55bab-109">Элемент **двевент** структуры [**МИДИЕВЕНТ**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) описывает событие MIDI, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="55bab-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="55bab-110">Короткие события полностью помещаются в этот элемент.</span><span class="sxs-lookup"><span data-stu-id="55bab-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="55bab-111">Для длинных событий требуется одно или несколько значений даублеворд в дополнение к элементу **двевент** для хранения описаний событий.</span><span class="sxs-lookup"><span data-stu-id="55bab-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="55bab-112">Старший байт элемента **двевент** содержит сведения о том, является ли событие длинным или коротким и о том, создается ли обратный вызов вместе с событием.</span><span class="sxs-lookup"><span data-stu-id="55bab-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="55bab-113">Кроме того, этот байт используется для описания типа события.</span><span class="sxs-lookup"><span data-stu-id="55bab-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="55bab-114">Оставшиеся 24 бита элемента **двевент** используются либо для хранения параметров события (для коротких сообщений), либо для хранения длительности параметров события (для длинных сообщений).</span><span class="sxs-lookup"><span data-stu-id="55bab-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="55bab-115">Чтобы извлечь сведения из члена **двевент** , используйте макросы [**Мевт \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) и [**мевт \_ евентпарм**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .</span><span class="sxs-lookup"><span data-stu-id="55bab-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="55bab-116">Описание предопределенных типов событий см. в справочном материале по структуре **мидиевент** .</span><span class="sxs-lookup"><span data-stu-id="55bab-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 