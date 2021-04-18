---
title: Событие Player. Плайстатечанже
description: Событие Плайстатечанже возникает при изменении свойства Плайстате.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Проигрыватель Windows Media Event Плайстатечанже
- Проигрыватель Windows Media Event Плайстатечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Плайстатечанже
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704199"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="8907a-106">Событие Player. Плайстатечанже</span><span class="sxs-lookup"><span data-stu-id="8907a-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="8907a-107">Событие **плайстатечанже** возникает при изменении свойства **плайстате** .</span><span class="sxs-lookup"><span data-stu-id="8907a-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8907a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8907a-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="8907a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8907a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8907a-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="8907a-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="8907a-111">Число (**Long**), которое указывает новый **плайстате**.</span><span class="sxs-lookup"><span data-stu-id="8907a-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="8907a-112">См. [плайстате](player-playstate.md) для таблицы возможных значений.</span><span class="sxs-lookup"><span data-stu-id="8907a-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8907a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8907a-113">Return value</span></span>

<span data-ttu-id="8907a-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8907a-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8907a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8907a-115">Remarks</span></span>

<span data-ttu-id="8907a-116">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8907a-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="8907a-117">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="8907a-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="8907a-118">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="8907a-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="8907a-119">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="8907a-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="8907a-120">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="8907a-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="8907a-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="8907a-121">Examples</span></span>

<span data-ttu-id="8907a-122">В следующем примере показан обработчик событий для *проигрывателя*. событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="8907a-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="8907a-123">Текстовый элемент HTML с именем «myText» отображает новое состояние воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8907a-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="8907a-124">Объект Player создан с ИДЕНТИФИКАТОРом "Player".</span><span class="sxs-lookup"><span data-stu-id="8907a-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="8907a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8907a-125">Requirements</span></span>



| <span data-ttu-id="8907a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8907a-126">Requirement</span></span> | <span data-ttu-id="8907a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8907a-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8907a-128">Версия</span><span class="sxs-lookup"><span data-stu-id="8907a-128">Version</span></span><br/> | <span data-ttu-id="8907a-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8907a-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8907a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8907a-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="8907a-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8907a-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8907a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8907a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8907a-133">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="8907a-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8907a-134">**Player. Плайстате**</span><span class="sxs-lookup"><span data-stu-id="8907a-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





