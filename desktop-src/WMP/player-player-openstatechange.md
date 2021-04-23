---
title: Событие Player. Опенстатечанже
description: Событие Опенстатечанже возникает при изменении значения свойства Опенстате. | Событие Player. Опенстатечанже
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Проигрыватель Windows Media Event Опенстатечанже
- Проигрыватель Windows Media Event Опенстатечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Опенстатечанже
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704242"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="a1d57-107">Событие Player. Опенстатечанже</span><span class="sxs-lookup"><span data-stu-id="a1d57-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="a1d57-108">Событие **опенстатечанже** возникает при изменении значения свойства **опенстате** .</span><span class="sxs-lookup"><span data-stu-id="a1d57-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d57-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1d57-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="a1d57-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1d57-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d57-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="a1d57-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d57-112">**Число** (**длинное**), указывающее новое состояние открытия.</span><span class="sxs-lookup"><span data-stu-id="a1d57-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="a1d57-113">См. раздел [опенстате](player-openstate.md) для таблицы Values.</span><span class="sxs-lookup"><span data-stu-id="a1d57-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d57-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1d57-114">Return value</span></span>

<span data-ttu-id="a1d57-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a1d57-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d57-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1d57-116">Remarks</span></span>

<span data-ttu-id="a1d57-117">Проигрыватель Windows Media может пройти несколько открытых состояний при попытке открыть сетевой файл, например найти сервер, подключиться к серверу и, наконец, открыть файл.</span><span class="sxs-lookup"><span data-stu-id="a1d57-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="a1d57-118">Это событие будет срабатывать каждый раз при изменении состояния открытия.</span><span class="sxs-lookup"><span data-stu-id="a1d57-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="a1d57-119">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a1d57-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a1d57-120">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="a1d57-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a1d57-121">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="a1d57-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="a1d57-122">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="a1d57-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="a1d57-123">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="a1d57-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d57-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a1d57-124">Requirements</span></span>



| <span data-ttu-id="a1d57-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a1d57-125">Requirement</span></span> | <span data-ttu-id="a1d57-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a1d57-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d57-127">Версия</span><span class="sxs-lookup"><span data-stu-id="a1d57-127">Version</span></span><br/> | <span data-ttu-id="a1d57-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a1d57-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1d57-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a1d57-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1d57-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d57-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d57-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1d57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d57-132">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="a1d57-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a1d57-133">**Player. Опенстате**</span><span class="sxs-lookup"><span data-stu-id="a1d57-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





