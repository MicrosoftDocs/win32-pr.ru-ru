---
title: Событие Player. Модечанже
description: Событие Модечанже возникает при изменении режима проигрывателя Windows Media. | Событие Player. Модечанже
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Проигрыватель Windows Media Event Модечанже
- Проигрыватель Windows Media Event Модечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Модечанже
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704177"
---
# <a name="playermodechange-event"></a><span data-ttu-id="197dc-107">Событие Player. Модечанже</span><span class="sxs-lookup"><span data-stu-id="197dc-107">Player.ModeChange event</span></span>

<span data-ttu-id="197dc-108">Событие **модечанже** возникает при изменении режима проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="197dc-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="197dc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="197dc-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="197dc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="197dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197dc-111">*моденаме*</span><span class="sxs-lookup"><span data-stu-id="197dc-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="197dc-112">**Строка** , указывающая режим, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="197dc-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="197dc-113">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="197dc-113">Contains one of the following values.</span></span>



| <span data-ttu-id="197dc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="197dc-114">Value</span></span>   | <span data-ttu-id="197dc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="197dc-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="197dc-116">shuffle</span><span class="sxs-lookup"><span data-stu-id="197dc-116">shuffle</span></span> | <span data-ttu-id="197dc-117">Дорожки воспроизводятся в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="197dc-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="197dc-118">loop</span><span class="sxs-lookup"><span data-stu-id="197dc-118">loop</span></span>    | <span data-ttu-id="197dc-119">Все последовательности дорожек воспроизводятся постоянно.</span><span class="sxs-lookup"><span data-stu-id="197dc-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="197dc-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="197dc-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="197dc-121">**Логическое значение** , указывающее новое состояние указанного режима.</span><span class="sxs-lookup"><span data-stu-id="197dc-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197dc-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="197dc-122">Return value</span></span>

<span data-ttu-id="197dc-123">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="197dc-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="197dc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="197dc-124">Remarks</span></span>

<span data-ttu-id="197dc-125">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="197dc-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="197dc-126">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="197dc-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="197dc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="197dc-127">Requirements</span></span>



| <span data-ttu-id="197dc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="197dc-128">Requirement</span></span> | <span data-ttu-id="197dc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="197dc-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="197dc-130">Версия</span><span class="sxs-lookup"><span data-stu-id="197dc-130">Version</span></span><br/> | <span data-ttu-id="197dc-131">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="197dc-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="197dc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="197dc-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="197dc-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197dc-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197dc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="197dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197dc-135">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="197dc-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="197dc-136">**Settings. Мода**</span><span class="sxs-lookup"><span data-stu-id="197dc-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="197dc-137">**Settings. setMode**</span><span class="sxs-lookup"><span data-stu-id="197dc-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





