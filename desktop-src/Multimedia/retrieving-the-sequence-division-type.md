---
title: Получение типа деления последовательности
description: Получение типа деления последовательности
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Цифровой интерфейс MIDI, тип деления последовательности
- MIDI (цифровой интерфейс музыкального инструмента), тип деления последовательности
- Секвенсор MIDI MCI, тип деления
- Команда MCI_STATUS
- Тип деления последовательности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986426"
---
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="0b3d4-108">Получение типа деления последовательности</span><span class="sxs-lookup"><span data-stu-id="0b3d4-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="0b3d4-109">*Тип деления* для последовательности MIDI определяет промежуток времени между событиями MIDI в последовательности.</span><span class="sxs-lookup"><span data-stu-id="0b3d4-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="0b3d4-110">Чтобы определить тип деления последовательности, используйте команду [**MCI \_ Status**](mci-status.md) и присвойте элементу **двитем** [**\_ состояния MCI \_ пармс**](mci-status-parms.md) структуры значение MCI \_ Seq \_ Status \_ дивтипе.</span><span class="sxs-lookup"><span data-stu-id="0b3d4-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="0b3d4-111">Если команда **" \_ состояние MCI** " выполнена успешно, элемент **двретурн** структуры **\_ \_ пармс "состояние MCI** " будет содержать одно из следующих значений для указания типа деления.</span><span class="sxs-lookup"><span data-stu-id="0b3d4-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="0b3d4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0b3d4-112">Value</span></span>                        | <span data-ttu-id="0b3d4-113">Тип деления</span><span class="sxs-lookup"><span data-stu-id="0b3d4-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="0b3d4-114">MCI \_ Seq \_ div \_ ппкн</span><span class="sxs-lookup"><span data-stu-id="0b3d4-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="0b3d4-115">ППКН (штук на четверть заметки)</span><span class="sxs-lookup"><span data-stu-id="0b3d4-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="0b3d4-116">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="0b3d4-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="0b3d4-117">SMPTE, 24 кадра кадров/с (кадров в секунду)</span><span class="sxs-lookup"><span data-stu-id="0b3d4-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="0b3d4-118">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="0b3d4-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="0b3d4-119">SMPTE, 25 кадров/с</span><span class="sxs-lookup"><span data-stu-id="0b3d4-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="0b3d4-120">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="0b3d4-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="0b3d4-121">SMPTE, 30 кадров/с</span><span class="sxs-lookup"><span data-stu-id="0b3d4-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="0b3d4-122">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="0b3d4-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="0b3d4-123">SMPTE, 30 кадров с раскрывающимся кадром</span><span class="sxs-lookup"><span data-stu-id="0b3d4-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="0b3d4-124">Необходимо иметь представление о типе деления последовательности для изменения или запроса его темп.</span><span class="sxs-lookup"><span data-stu-id="0b3d4-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="0b3d4-125">Невозможно изменить тип деления последовательности с помощью средства Sequencer MCI.</span><span class="sxs-lookup"><span data-stu-id="0b3d4-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




