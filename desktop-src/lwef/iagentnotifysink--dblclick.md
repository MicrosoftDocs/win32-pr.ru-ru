---
title: Иажентнотифисинк DblClick
description: Иажентнотифисинк DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120927"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="a6d61-103">Иажентнотифисинк::D Блкликк</span><span class="sxs-lookup"><span data-stu-id="a6d61-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="a6d61-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6d61-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="a6d61-105">Уведомляет клиентское приложение, когда пользователь дважды щелкает символ.</span><span class="sxs-lookup"><span data-stu-id="a6d61-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="a6d61-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a6d61-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a6d61-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="a6d61-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a6d61-108">Идентификатор символа двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="a6d61-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="a6d61-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="a6d61-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a6d61-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="a6d61-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a6d61-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="a6d61-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="a6d61-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a6d61-112">Value</span></span>  | <span data-ttu-id="a6d61-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a6d61-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="a6d61-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="a6d61-114">0x0001</span></span> | <span data-ttu-id="a6d61-115">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="a6d61-115">Left Button</span></span>                                    |
| <span data-ttu-id="a6d61-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="a6d61-116">0x0010</span></span> | <span data-ttu-id="a6d61-117">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="a6d61-117">Middle Button</span></span>                                  |
| <span data-ttu-id="a6d61-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="a6d61-118">0x0002</span></span> | <span data-ttu-id="a6d61-119">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="a6d61-119">Right Button</span></span>                                   |
| <span data-ttu-id="a6d61-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="a6d61-120">0x0004</span></span> | <span data-ttu-id="a6d61-121">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="a6d61-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="a6d61-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="a6d61-122">0x0008</span></span> | <span data-ttu-id="a6d61-123">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="a6d61-123">Control Key Down</span></span>                               |
| <span data-ttu-id="a6d61-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="a6d61-124">0x0020</span></span> | <span data-ttu-id="a6d61-125">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="a6d61-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="a6d61-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="a6d61-126">0x1000</span></span> | <span data-ttu-id="a6d61-127">Событие произошло на значке панели задач "символ"</span><span class="sxs-lookup"><span data-stu-id="a6d61-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="a6d61-128"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a6d61-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a6d61-129">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="a6d61-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a6d61-130"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="a6d61-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a6d61-131">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="a6d61-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="a6d61-132">Это событие отправляется клиенту input-Active для символа.</span><span class="sxs-lookup"><span data-stu-id="a6d61-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="a6d61-133">Если ни один из клиентов символа не является входным, сервер уведомляет об активном клиенте символа.</span><span class="sxs-lookup"><span data-stu-id="a6d61-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="a6d61-134">Если символ является видимым, сервер также делает ввод клиента активным и отправляет [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="a6d61-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="a6d61-135">Если символ скрыт, он также автоматически отображается.</span><span class="sxs-lookup"><span data-stu-id="a6d61-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 




