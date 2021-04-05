---
title: Иажентнотифисинк щелкните
description: Иажентнотифисинк щелкните
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d1dccd838152503c603d158f043a0279d4b5c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068168"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="73829-103">Иажентнотифисинк:: Click</span><span class="sxs-lookup"><span data-stu-id="73829-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="73829-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73829-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="73829-105">Уведомляет клиентское приложение, когда пользователь щелкает значок символа или символа на панели задач.</span><span class="sxs-lookup"><span data-stu-id="73829-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="73829-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="73829-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="73829-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="73829-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="73829-108">Идентификатор нажатого символа.</span><span class="sxs-lookup"><span data-stu-id="73829-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="73829-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="73829-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="73829-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="73829-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="73829-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="73829-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="73829-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="73829-112">0x0001</span></span> | <span data-ttu-id="73829-113">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="73829-113">Left Button</span></span>                                    |
| <span data-ttu-id="73829-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="73829-114">0x0010</span></span> | <span data-ttu-id="73829-115">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="73829-115">Middle Button</span></span>                                  |
| <span data-ttu-id="73829-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="73829-116">0x0002</span></span> | <span data-ttu-id="73829-117">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="73829-117">Right Button</span></span>                                   |
| <span data-ttu-id="73829-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="73829-118">0x0004</span></span> | <span data-ttu-id="73829-119">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="73829-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="73829-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="73829-120">0x0008</span></span> | <span data-ttu-id="73829-121">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="73829-121">Control Key Down</span></span>                               |
| <span data-ttu-id="73829-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="73829-122">0x0020</span></span> | <span data-ttu-id="73829-123">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="73829-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="73829-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="73829-124">0x1000</span></span> | <span data-ttu-id="73829-125">Событие произошло на значке панели задач "символ"</span><span class="sxs-lookup"><span data-stu-id="73829-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="73829-126"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="73829-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="73829-127">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="73829-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="73829-128"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="73829-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="73829-129">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="73829-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="73829-130">Это событие отправляется клиенту input-Active для символа.</span><span class="sxs-lookup"><span data-stu-id="73829-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="73829-131">Если ни один из клиентов символа не является входным, сервер уведомляет об активном клиенте символа.</span><span class="sxs-lookup"><span data-stu-id="73829-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="73829-132">Если символ является видимым, сервер также делает ввод клиента активным и отправляет [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="73829-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="73829-133">Если символ скрыт, также автоматически отображается символ.</span><span class="sxs-lookup"><span data-stu-id="73829-133">If the character hidden, the character is also automatically shown.</span></span>

 

 




