---
title: Player. Плайстате
description: Свойство Плайстате извлекает значение, указывающее состояние операции проигрывателя Windows Media.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Проигрыватель проигрывателя Windows Media Player. Плайстате
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704402"
---
# <a name="playerplaystate"></a><span data-ttu-id="805be-104">Player. Плайстате</span><span class="sxs-lookup"><span data-stu-id="805be-104">Player.playState</span></span>

<span data-ttu-id="805be-105">Свойство **плайстате** извлекает значение, указывающее состояние операции проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="805be-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="805be-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="805be-106">Syntax</span></span>

<span data-ttu-id="805be-107">*проигрыватель* . **плайстате**</span><span class="sxs-lookup"><span data-stu-id="805be-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="805be-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="805be-108">Possible Values</span></span>

<span data-ttu-id="805be-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="805be-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="805be-110">Константу перечисления в стиле C можно получить с помощью префикса "вмппс" в качестве значения состояния.</span><span class="sxs-lookup"><span data-stu-id="805be-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="805be-111">Например, константа для воспроизводимого состояния — **вмппсплайинг**.</span><span class="sxs-lookup"><span data-stu-id="805be-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="805be-112">Значение</span><span class="sxs-lookup"><span data-stu-id="805be-112">Value</span></span> | <span data-ttu-id="805be-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="805be-113">State</span></span>         | <span data-ttu-id="805be-114">Описание</span><span class="sxs-lookup"><span data-stu-id="805be-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805be-115">0</span><span class="sxs-lookup"><span data-stu-id="805be-115">0</span></span>     | <span data-ttu-id="805be-116">Не определено.</span><span class="sxs-lookup"><span data-stu-id="805be-116">Undefined</span></span>     | <span data-ttu-id="805be-117">Проигрыватель Windows Media находится в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="805be-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="805be-118">1</span><span class="sxs-lookup"><span data-stu-id="805be-118">1</span></span>     | <span data-ttu-id="805be-119">Остановлена</span><span class="sxs-lookup"><span data-stu-id="805be-119">Stopped</span></span>       | <span data-ttu-id="805be-120">Воспроизведение текущего элемента мультимедиа остановлено.</span><span class="sxs-lookup"><span data-stu-id="805be-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="805be-121">2</span><span class="sxs-lookup"><span data-stu-id="805be-121">2</span></span>     | <span data-ttu-id="805be-122">Пауза</span><span class="sxs-lookup"><span data-stu-id="805be-122">Paused</span></span>        | <span data-ttu-id="805be-123">Воспроизведение текущего элемента мультимедиа приостановлено.</span><span class="sxs-lookup"><span data-stu-id="805be-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="805be-124">Когда элемент мультимедиа приостанавливается, возобновление воспроизведения начинается с того же расположения.</span><span class="sxs-lookup"><span data-stu-id="805be-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="805be-125">3</span><span class="sxs-lookup"><span data-stu-id="805be-125">3</span></span>     | <span data-ttu-id="805be-126">Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="805be-126">Playing</span></span>       | <span data-ttu-id="805be-127">Текущий элемент мультимедиа воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="805be-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="805be-128">4</span><span class="sxs-lookup"><span data-stu-id="805be-128">4</span></span>     | <span data-ttu-id="805be-129">сканфорвард</span><span class="sxs-lookup"><span data-stu-id="805be-129">ScanForward</span></span>   | <span data-ttu-id="805be-130">Текущий элемент мультимедиа обеспечивает быструю пересылку.</span><span class="sxs-lookup"><span data-stu-id="805be-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="805be-131">5</span><span class="sxs-lookup"><span data-stu-id="805be-131">5</span></span>     | <span data-ttu-id="805be-132">сканреверсе</span><span class="sxs-lookup"><span data-stu-id="805be-132">ScanReverse</span></span>   | <span data-ttu-id="805be-133">Текущий элемент мультимедиа — быстрое перемотка назад.</span><span class="sxs-lookup"><span data-stu-id="805be-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="805be-134">6</span><span class="sxs-lookup"><span data-stu-id="805be-134">6</span></span>     | <span data-ttu-id="805be-135">ответов</span><span class="sxs-lookup"><span data-stu-id="805be-135">Buffering</span></span>     | <span data-ttu-id="805be-136">Текущий элемент мультимедиа получает дополнительные данные с сервера.</span><span class="sxs-lookup"><span data-stu-id="805be-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="805be-137">7</span><span class="sxs-lookup"><span data-stu-id="805be-137">7</span></span>     | <span data-ttu-id="805be-138">Ожидание</span><span class="sxs-lookup"><span data-stu-id="805be-138">Waiting</span></span>       | <span data-ttu-id="805be-139">Соединение установлено, но сервер не отправляет данные.</span><span class="sxs-lookup"><span data-stu-id="805be-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="805be-140">Ожидание начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="805be-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="805be-141">8</span><span class="sxs-lookup"><span data-stu-id="805be-141">8</span></span>     | <span data-ttu-id="805be-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="805be-142">MediaEnded</span></span>    | <span data-ttu-id="805be-143">Воспроизведение элемента мультимедиа завершено.</span><span class="sxs-lookup"><span data-stu-id="805be-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="805be-144">9</span><span class="sxs-lookup"><span data-stu-id="805be-144">9</span></span>     | <span data-ttu-id="805be-145">Переход</span><span class="sxs-lookup"><span data-stu-id="805be-145">Transitioning</span></span> | <span data-ttu-id="805be-146">Подготовка нового элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="805be-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="805be-147">10</span><span class="sxs-lookup"><span data-stu-id="805be-147">10</span></span>    | <span data-ttu-id="805be-148">Ready</span><span class="sxs-lookup"><span data-stu-id="805be-148">Ready</span></span>         | <span data-ttu-id="805be-149">Все готово для начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="805be-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="805be-150">11</span><span class="sxs-lookup"><span data-stu-id="805be-150">11</span></span>    | <span data-ttu-id="805be-151">Повторное подключение</span><span class="sxs-lookup"><span data-stu-id="805be-151">Reconnecting</span></span>  | <span data-ttu-id="805be-152">Повторное подключение к потоку.</span><span class="sxs-lookup"><span data-stu-id="805be-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="805be-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="805be-153">Remarks</span></span>

<span data-ttu-id="805be-154">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="805be-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="805be-155">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="805be-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="805be-156">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="805be-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="805be-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="805be-157">Examples</span></span>

<span data-ttu-id="805be-158">В следующем коде JScript показано использование *проигрывателя*. Свойство **плайстате** .</span><span class="sxs-lookup"><span data-stu-id="805be-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="805be-159">В текстовом элементе HTML с именем "myText" отображается текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="805be-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="805be-160">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="805be-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="805be-161">Требования</span><span class="sxs-lookup"><span data-stu-id="805be-161">Requirements</span></span>



| <span data-ttu-id="805be-162">Требование</span><span class="sxs-lookup"><span data-stu-id="805be-162">Requirement</span></span> | <span data-ttu-id="805be-163">Значение</span><span class="sxs-lookup"><span data-stu-id="805be-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="805be-164">Версия</span><span class="sxs-lookup"><span data-stu-id="805be-164">Version</span></span><br/> | <span data-ttu-id="805be-165">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="805be-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="805be-166">DLL</span><span class="sxs-lookup"><span data-stu-id="805be-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="805be-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805be-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805be-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="805be-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805be-169">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="805be-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="805be-170">**Событие Player. Плайстатечанже**</span><span class="sxs-lookup"><span data-stu-id="805be-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





