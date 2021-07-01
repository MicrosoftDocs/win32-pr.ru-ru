---
title: Иажентнотифисинк щелкните
description: Иажентнотифисинк щелкните
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120907"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="0519b-103">Иажентнотифисинк:: Click</span><span class="sxs-lookup"><span data-stu-id="0519b-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="0519b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0519b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="0519b-105">Уведомляет клиентское приложение, когда пользователь щелкает значок символа или символа на панели задач.</span><span class="sxs-lookup"><span data-stu-id="0519b-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="0519b-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0519b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="0519b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="0519b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="0519b-108">Идентификатор нажатого символа.</span><span class="sxs-lookup"><span data-stu-id="0519b-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="0519b-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="0519b-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="0519b-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="0519b-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="0519b-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="0519b-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="0519b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0519b-112">Value</span></span>  | <span data-ttu-id="0519b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0519b-113">Description</span></span>                                    |
|--------|------------------------------------------------|
| <span data-ttu-id="0519b-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="0519b-114">0x0001</span></span> | <span data-ttu-id="0519b-115">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="0519b-115">Left Button</span></span>                                    |
| <span data-ttu-id="0519b-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="0519b-116">0x0010</span></span> | <span data-ttu-id="0519b-117">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="0519b-117">Middle Button</span></span>                                  |
| <span data-ttu-id="0519b-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="0519b-118">0x0002</span></span> | <span data-ttu-id="0519b-119">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="0519b-119">Right Button</span></span>                                   |
| <span data-ttu-id="0519b-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="0519b-120">0x0004</span></span> | <span data-ttu-id="0519b-121">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="0519b-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="0519b-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="0519b-122">0x0008</span></span> | <span data-ttu-id="0519b-123">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="0519b-123">Control Key Down</span></span>                               |
| <span data-ttu-id="0519b-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="0519b-124">0x0020</span></span> | <span data-ttu-id="0519b-125">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="0519b-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="0519b-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="0519b-126">0x1000</span></span> | <span data-ttu-id="0519b-127">Событие произошло на значке панели задач "символ"</span><span class="sxs-lookup"><span data-stu-id="0519b-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="0519b-128"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0519b-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="0519b-129">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="0519b-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="0519b-130"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="0519b-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="0519b-131">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="0519b-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="0519b-132">Это событие отправляется клиенту input-Active для символа.</span><span class="sxs-lookup"><span data-stu-id="0519b-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="0519b-133">Если ни один из клиентов символа не является входным, сервер уведомляет об активном клиенте символа.</span><span class="sxs-lookup"><span data-stu-id="0519b-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="0519b-134">Если символ является видимым, сервер также делает ввод клиента активным и отправляет [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="0519b-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="0519b-135">Если символ скрыт, также автоматически отображается символ.</span><span class="sxs-lookup"><span data-stu-id="0519b-135">If the character hidden, the character is also automatically shown.</span></span>

 

 




