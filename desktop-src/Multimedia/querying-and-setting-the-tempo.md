---
title: Запрос и установка темп
description: Запрос и установка темп
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- Цифровой интерфейс MIDI, темп
- MIDI (цифровой интерфейс музыкального инструмента), темп
- Секвенсор MIDI MCI, темп
- Команда MCI_STATUS
- темп последовательности
- темп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780114"
---
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="06821-109">Запрос и установка темп</span><span class="sxs-lookup"><span data-stu-id="06821-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="06821-110">Чтобы получить темп последовательности, используйте команду [**MCI \_ Status**](mci-status.md) и присвойте элементу **двитем** [**\_ состояния MCI \_ пармс**](mci-status-parms.md) структуры значение MCI \_ Seq \_ Status \_ темп.</span><span class="sxs-lookup"><span data-stu-id="06821-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="06821-111">Если команда **" \_ состояние MCI** " выполнена успешно, элемент **двретурн** структуры **\_ \_ пармс "состояние MCI** " содержит текущую темп.</span><span class="sxs-lookup"><span data-stu-id="06821-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="06821-112">Чтобы изменить темп, используйте команду [**MCI \_ Set**](mci-set.md) в структуре [**MCI \_ Seq \_ Set \_ пармс**](mci-seq-set-parms.md) , указав флаг MCI \_ Seq \_ Set \_ темп и установив для элемента **двтемпо** структуры требуемый темп.</span><span class="sxs-lookup"><span data-stu-id="06821-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="06821-113">Способ представления темп зависит от типа деления последовательности.</span><span class="sxs-lookup"><span data-stu-id="06821-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="06821-114">Если тип деления — ППКН, темп представляется в виде ритма в минуту.</span><span class="sxs-lookup"><span data-stu-id="06821-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="06821-115">Если тип деления является одним из типов деления SMPTE, темп представляется в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="06821-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="06821-116">Дополнительные сведения об определении типа деления последовательности см. [в разделе Получение типа деления последовательности](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="06821-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




