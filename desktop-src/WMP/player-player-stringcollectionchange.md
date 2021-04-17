---
title: Событие Player. Стрингколлектиончанже
description: Событие Стрингколлектиончанже возникает при изменении коллекции строк. | Событие Player. Стрингколлектиончанже
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Проигрыватель Windows Media Event Стрингколлектиончанже
- Проигрыватель Windows Media Event Стрингколлектиончанже, класс Player
- Класс проигрывателя Windows Media Player, событие Стрингколлектиончанже
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704165"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="dd824-107">Событие Player. Стрингколлектиончанже</span><span class="sxs-lookup"><span data-stu-id="dd824-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="dd824-108">Событие Стрингколлектиончанже возникает при изменении коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="dd824-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd824-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd824-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="dd824-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd824-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd824-111">*пдиспстрингколлектион*</span><span class="sxs-lookup"><span data-stu-id="dd824-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="dd824-112">Измененный объект **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="dd824-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="dd824-113">*change*</span><span class="sxs-lookup"><span data-stu-id="dd824-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="dd824-114">Число (Long), указывающее тип изменения, произошедшего в коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="dd824-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="dd824-115">Включает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dd824-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="dd824-116">Число</span><span class="sxs-lookup"><span data-stu-id="dd824-116">Number</span></span> | <span data-ttu-id="dd824-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dd824-117">Description</span></span>                        |
| <span data-ttu-id="dd824-118">0</span><span class="sxs-lookup"><span data-stu-id="dd824-118">0</span></span>      | <span data-ttu-id="dd824-119">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dd824-119">Unknown.</span></span> <span data-ttu-id="dd824-120">(Недопустимое значение)</span><span class="sxs-lookup"><span data-stu-id="dd824-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="dd824-121">1</span><span class="sxs-lookup"><span data-stu-id="dd824-121">1</span></span>      | <span data-ttu-id="dd824-122">Элемент был вставлен.</span><span class="sxs-lookup"><span data-stu-id="dd824-122">An item was inserted.</span></span>              |
| <span data-ttu-id="dd824-123">2</span><span class="sxs-lookup"><span data-stu-id="dd824-123">2</span></span>      | <span data-ttu-id="dd824-124">Изменена коллекция строк.</span><span class="sxs-lookup"><span data-stu-id="dd824-124">The string collection changed.</span></span>     |
| <span data-ttu-id="dd824-125">3</span><span class="sxs-lookup"><span data-stu-id="dd824-125">3</span></span>      | <span data-ttu-id="dd824-126">Элемент удален.</span><span class="sxs-lookup"><span data-stu-id="dd824-126">An item was deleted.</span></span>               |
| <span data-ttu-id="dd824-127">4</span><span class="sxs-lookup"><span data-stu-id="dd824-127">4</span></span>      | <span data-ttu-id="dd824-128">Коллекция строк была удалена.</span><span class="sxs-lookup"><span data-stu-id="dd824-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="dd824-129">5</span><span class="sxs-lookup"><span data-stu-id="dd824-129">5</span></span>      | <span data-ttu-id="dd824-130">Начинается групповое обновление.</span><span class="sxs-lookup"><span data-stu-id="dd824-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="dd824-131">6</span><span class="sxs-lookup"><span data-stu-id="dd824-131">6</span></span>      | <span data-ttu-id="dd824-132">Групповые обновления завершены.</span><span class="sxs-lookup"><span data-stu-id="dd824-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="dd824-133">*лколлектиониндекс*</span><span class="sxs-lookup"><span data-stu-id="dd824-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="dd824-134">Число (Long), содержащее индекс измененного элемента коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="dd824-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd824-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd824-135">Return value</span></span>

<span data-ttu-id="dd824-136">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd824-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd824-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd824-137">Remarks</span></span>

<span data-ttu-id="dd824-138">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd824-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd824-139">Требования</span><span class="sxs-lookup"><span data-stu-id="dd824-139">Requirements</span></span>



| <span data-ttu-id="dd824-140">Требование</span><span class="sxs-lookup"><span data-stu-id="dd824-140">Requirement</span></span> | <span data-ttu-id="dd824-141">Значение</span><span class="sxs-lookup"><span data-stu-id="dd824-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd824-142">Версия</span><span class="sxs-lookup"><span data-stu-id="dd824-142">Version</span></span><br/> | <span data-ttu-id="dd824-143">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="dd824-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="dd824-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dd824-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd824-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd824-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd824-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd824-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd824-147">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="dd824-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="dd824-148">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="dd824-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





