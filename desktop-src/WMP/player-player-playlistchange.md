---
title: Событие Player. Плайлистчанже
description: Событие Плайлистчанже возникает при изменении списка воспроизведения. | Событие Player. Плайлистчанже
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Проигрыватель Windows Media Event Плайлистчанже
- Проигрыватель Windows Media Event Плайлистчанже, класс Player
- Класс проигрывателя Windows Media Player, событие Плайлистчанже
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704241"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="ead86-107">Событие Player. Плайлистчанже</span><span class="sxs-lookup"><span data-stu-id="ead86-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="ead86-108">Событие **плайлистчанже** возникает при изменении списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ead86-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead86-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ead86-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="ead86-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ead86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead86-111">*Списком*</span><span class="sxs-lookup"><span data-stu-id="ead86-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="ead86-112">Измененный объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="ead86-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="ead86-113">*change*</span><span class="sxs-lookup"><span data-stu-id="ead86-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="ead86-114">**Число** (**длинное**), указывающее тип изменения, произошедшего в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ead86-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="ead86-115">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ead86-115">Contains one of the following values.</span></span>



| <span data-ttu-id="ead86-116">number</span><span class="sxs-lookup"><span data-stu-id="ead86-116">Number</span></span> | <span data-ttu-id="ead86-117">name</span><span class="sxs-lookup"><span data-stu-id="ead86-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="ead86-118">0</span><span class="sxs-lookup"><span data-stu-id="ead86-118">0</span></span>      | <span data-ttu-id="ead86-119">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="ead86-119">Unknown</span></span>       |
| <span data-ttu-id="ead86-120">1</span><span class="sxs-lookup"><span data-stu-id="ead86-120">1</span></span>      | <span data-ttu-id="ead86-121">Clear</span><span class="sxs-lookup"><span data-stu-id="ead86-121">Clear</span></span>         |
| <span data-ttu-id="ead86-122">2</span><span class="sxs-lookup"><span data-stu-id="ead86-122">2</span></span>      | <span data-ttu-id="ead86-123">инфочанже</span><span class="sxs-lookup"><span data-stu-id="ead86-123">InfoChange</span></span>    |
| <span data-ttu-id="ead86-124">3</span><span class="sxs-lookup"><span data-stu-id="ead86-124">3</span></span>      | <span data-ttu-id="ead86-125">Переместить</span><span class="sxs-lookup"><span data-stu-id="ead86-125">Move</span></span>          |
| <span data-ttu-id="ead86-126">4</span><span class="sxs-lookup"><span data-stu-id="ead86-126">4</span></span>      | <span data-ttu-id="ead86-127">Удалить</span><span class="sxs-lookup"><span data-stu-id="ead86-127">Delete</span></span>        |
| <span data-ttu-id="ead86-128">5</span><span class="sxs-lookup"><span data-stu-id="ead86-128">5</span></span>      | <span data-ttu-id="ead86-129">Вставить</span><span class="sxs-lookup"><span data-stu-id="ead86-129">Insert</span></span>        |
| <span data-ttu-id="ead86-130">6</span><span class="sxs-lookup"><span data-stu-id="ead86-130">6</span></span>      | <span data-ttu-id="ead86-131">Добавление</span><span class="sxs-lookup"><span data-stu-id="ead86-131">Append</span></span>        |
| <span data-ttu-id="ead86-132">7</span><span class="sxs-lookup"><span data-stu-id="ead86-132">7</span></span>      | <span data-ttu-id="ead86-133">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ead86-133">Not supported</span></span> |
| <span data-ttu-id="ead86-134">8</span><span class="sxs-lookup"><span data-stu-id="ead86-134">8</span></span>      | <span data-ttu-id="ead86-135">NameChange</span><span class="sxs-lookup"><span data-stu-id="ead86-135">NameChange</span></span>    |
| <span data-ttu-id="ead86-136">9</span><span class="sxs-lookup"><span data-stu-id="ead86-136">9</span></span>      | <span data-ttu-id="ead86-137">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ead86-137">Not supported</span></span> |
| <span data-ttu-id="ead86-138">10</span><span class="sxs-lookup"><span data-stu-id="ead86-138">10</span></span>     | <span data-ttu-id="ead86-139">Сортировка</span><span class="sxs-lookup"><span data-stu-id="ead86-139">Sort</span></span>          |



 

<span data-ttu-id="ead86-140">Константу перечисления в стиле C можно получить, добавив префикс "вмплк" к значению Name.</span><span class="sxs-lookup"><span data-stu-id="ead86-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="ead86-141">Например, константа для состояния перемещения — **вмплкмове**.</span><span class="sxs-lookup"><span data-stu-id="ead86-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead86-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ead86-142">Return value</span></span>

<span data-ttu-id="ead86-143">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ead86-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ead86-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ead86-144">Remarks</span></span>

<span data-ttu-id="ead86-145">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="ead86-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="ead86-146">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="ead86-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="ead86-147">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ead86-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead86-148">Требования</span><span class="sxs-lookup"><span data-stu-id="ead86-148">Requirements</span></span>



| <span data-ttu-id="ead86-149">Требование</span><span class="sxs-lookup"><span data-stu-id="ead86-149">Requirement</span></span> | <span data-ttu-id="ead86-150">Значение</span><span class="sxs-lookup"><span data-stu-id="ead86-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ead86-151">Версия</span><span class="sxs-lookup"><span data-stu-id="ead86-151">Version</span></span><br/> | <span data-ttu-id="ead86-152">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ead86-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ead86-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ead86-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="ead86-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead86-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead86-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ead86-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead86-156">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="ead86-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





