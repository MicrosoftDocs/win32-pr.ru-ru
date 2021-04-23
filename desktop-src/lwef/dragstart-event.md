---
title: Событие Драгстарт
description: Событие Драгстарт
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067951"
---
# <a name="dragstart-event"></a><span data-ttu-id="8b9e2-103">Событие Драгстарт</span><span class="sxs-lookup"><span data-stu-id="8b9e2-103">DragStart Event</span></span>

<span data-ttu-id="8b9e2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b9e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8b9e2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="8b9e2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8b9e2-106">Происходит, когда пользователь начинает перетаскивать символ.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-106">Occurs when the user begins dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="8b9e2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8b9e2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8b9e2-108"> *Подагент\ *\ *\ * \_ драгстарт*\ *  **(ByVal** *чарактерид*, **(** *кнопка* ByVal, **(ByVal** *SHIFT*, **(** ByVal *X*, **(ByVal** *Y\ * *)**</span><span class="sxs-lookup"><span data-stu-id="8b9e2-108">**Sub** *agent\*\*\*\_DragStart*\* **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="8b9e2-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="8b9e2-109">Part</span></span>          | <span data-ttu-id="8b9e2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8b9e2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9e2-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="8b9e2-111">*CharacterID*</span></span> | <span data-ttu-id="8b9e2-112">Возвращает идентификатор нажатого символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8b9e2-113">*Кнопка*</span><span class="sxs-lookup"><span data-stu-id="8b9e2-113">*Button*</span></span>      | <span data-ttu-id="8b9e2-114">Возвращает целое число, определяющее кнопку, которая была нажата и была вызвана для события.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="8b9e2-115">Аргумент Button — это битовое битовое значение, соответствующее левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="8b9e2-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="8b9e2-116">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="8b9e2-117">Задан только один из битов, указывающий кнопку, вызвавшую событие.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8b9e2-118">*Сдвиг*</span><span class="sxs-lookup"><span data-stu-id="8b9e2-118">*Shift*</span></span>       | <span data-ttu-id="8b9e2-119">Возвращает целое число, соответствующее состоянию клавиш SHIFT, CTRL и ALT при нажатии или отпускании кнопки, заданной в аргументе Button.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="8b9e2-120">Если ключ не работает, устанавливается бит.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-120">A bit is set if the key is down.</span></span> <span data-ttu-id="8b9e2-121">Аргумент сдвига является битовым битом с наименьшими значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="8b9e2-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="8b9e2-122">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="8b9e2-123">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="8b9e2-124">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="8b9e2-125">Например, при нажатии клавиш CTRL и ALT значение Shift будет равно 6.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="8b9e2-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="8b9e2-126">*X,Y*</span></span>         | <span data-ttu-id="8b9e2-127">Возвращает целое число, указывающее текущее положение указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="8b9e2-128">Значения X и Y всегда выражаются в пикселях относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8b9e2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b9e2-129">Remarks</span></span>

<span data-ttu-id="8b9e2-130">Это событие отправляется только клиенту ввода-активного клиента символа.</span><span class="sxs-lookup"><span data-stu-id="8b9e2-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="8b9e2-131">Когда пользователь перетаскивает символ без ввода активного клиента, сервер устанавливает последний входной и активный клиент как текущий клиент ввода-активности, отправляя событие [**активатеинпут**](activateinput-event.md) этому клиенту, а затем отправляя событие **драгстарт** .</span><span class="sxs-lookup"><span data-stu-id="8b9e2-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **DragStart** event.</span></span>

### <a name="see-also"></a><span data-ttu-id="8b9e2-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="8b9e2-132">See Also</span></span>

[<span data-ttu-id="8b9e2-133">**Событие Драгкомплете**</span><span class="sxs-lookup"><span data-stu-id="8b9e2-133">**DragComplete event**</span></span>](dragcomplete-event.md)


 

 




