---
title: Коды ошибок анимации Windows (Winerror. h)
description: При возникновении ошибки анимация Windows возвращает код в виде значения HRESULT. В этом разделе содержится список кодов ошибок, относящихся к анимации Windows. Список общих кодов ошибок COM см. в разделе Коды ошибок COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691814"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="0e198-105">Коды ошибок анимации Windows</span><span class="sxs-lookup"><span data-stu-id="0e198-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="0e198-106">При возникновении ошибки анимация Windows возвращает код в виде значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e198-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="0e198-107">В этом разделе содержится список кодов ошибок, относящихся к анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="0e198-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="0e198-108">Список общих кодов ошибок COM см. в разделе [коды ошибок COM](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0e198-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0e198-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ сбой создания пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="0e198-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="0e198-111">Не удалось создать объект.</span><span class="sxs-lookup"><span data-stu-id="0e198-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**\_ \_ вызвано завершение работы пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="0e198-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="0e198-114">Метод [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) был вызван в диспетчере анимации, что привело к завершению работы диспетчера анимации, а также к освобождению всех переменных анимации и раскадровок, которые она создала.</span><span class="sxs-lookup"><span data-stu-id="0e198-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="0e198-115">После [**завершения работы**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)не удается вызвать методы для любого объекта анимации.</span><span class="sxs-lookup"><span data-stu-id="0e198-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**Недопустимый повторный вход пользовательского интерфейса \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="0e198-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="0e198-118">Этот метод не может быть вызван во время обратного вызова этого типа.</span><span class="sxs-lookup"><span data-stu-id="0e198-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**\_объект UI \_ E \_ запечатан**</span><span class="sxs-lookup"><span data-stu-id="0e198-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="0e198-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="0e198-121">Этот объект запечатан, поэтому это изменение больше не разрешено.</span><span class="sxs-lookup"><span data-stu-id="0e198-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**значение пользовательского интерфейса \_ E \_ \_ не \_ задано**</span><span class="sxs-lookup"><span data-stu-id="0e198-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="0e198-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="0e198-124">Запрошенное значение никогда не было задано и поэтому не может быть получено.</span><span class="sxs-lookup"><span data-stu-id="0e198-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**значение пользовательского интерфейса \_ E \_ \_ не \_ определено**</span><span class="sxs-lookup"><span data-stu-id="0e198-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="0e198-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="0e198-127">Не удается определить запрошенное значение.</span><span class="sxs-lookup"><span data-stu-id="0e198-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**\_ \_ Недопустимый вывод пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="0e198-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="0e198-130">Обратный вызов вернул недопустимый выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="0e198-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**\_ \_ ожидалось логическое значение пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="0e198-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="0e198-133">Обратный вызов вернул код успешного выполнения, отличный от S \_ ОК или \_ false.</span><span class="sxs-lookup"><span data-stu-id="0e198-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**Пользовательский интерфейс \_ E- \_ другой \_ владелец**</span><span class="sxs-lookup"><span data-stu-id="0e198-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="0e198-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="0e198-136">Владельцем параметра, который должен быть владельцем этого объекта, является другой объект.</span><span class="sxs-lookup"><span data-stu-id="0e198-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ неоднозначное соответствие пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="0e198-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="0e198-139">Критерию поиска соответствует более одного элемента.</span><span class="sxs-lookup"><span data-stu-id="0e198-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**\_переполнение пользовательского интерфейса E \_ FP \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="0e198-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="0e198-142">Произошло переполнение с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="0e198-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**Пользовательский интерфейс \_ E \_ неправильный \_ поток**</span><span class="sxs-lookup"><span data-stu-id="0e198-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="0e198-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="0e198-145">Этот метод может быть вызван только из потока, в котором был создан объект.</span><span class="sxs-lookup"><span data-stu-id="0e198-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**\_ \_ Активная раскадровка интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="0e198-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="0e198-148">Раскадровка в данный момент находится в расписании.</span><span class="sxs-lookup"><span data-stu-id="0e198-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**\_раскадровка интерфейса E \_ \_ не \_ воспроизводилась**</span><span class="sxs-lookup"><span data-stu-id="0e198-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="0e198-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="0e198-151">Раскадровка не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="0e198-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**\_ \_ начальный \_ ОПОРНЫЙ кадр пользовательского интерфейса E \_ после \_ окончания**</span><span class="sxs-lookup"><span data-stu-id="0e198-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="0e198-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="0e198-154">Начальный опорный кадр может находиться после конечного опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="0e198-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**\_ \_ конечный \_ ОПОРНЫЙ кадр пользовательского интерфейса E \_ не \_ определен**</span><span class="sxs-lookup"><span data-stu-id="0e198-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="0e198-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="0e198-157">При достижении начального опорного кадра может быть невозможно определить время конечного опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="0e198-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_Перекрытие \_ циклов пользовательского интерфейса E \_**</span><span class="sxs-lookup"><span data-stu-id="0e198-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="0e198-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="0e198-160">Две повторяющиеся части раскадровки могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="0e198-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**Переход пользовательского интерфейса \_ E \_ \_ уже \_ используется**</span><span class="sxs-lookup"><span data-stu-id="0e198-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="0e198-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="0e198-163">Переход уже добавлен в другую раскадровку или был добавлен в раскадровку, которая завершила воспроизведение и выпуск.</span><span class="sxs-lookup"><span data-stu-id="0e198-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**Переход пользовательского интерфейса \_ E \_ \_ не \_ в \_ раскадровке**</span><span class="sxs-lookup"><span data-stu-id="0e198-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="0e198-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="0e198-166">Переход не был добавлен в раскадровку.</span><span class="sxs-lookup"><span data-stu-id="0e198-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**Переход пользовательского интерфейса \_ E в \_ \_ поeclipse**</span><span class="sxs-lookup"><span data-stu-id="0e198-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="0e198-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="0e198-169">Переход может заeclipse начало другого перехода в раскадровке.</span><span class="sxs-lookup"><span data-stu-id="0e198-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_время по электронной почты пользовательского интерфейса \_ \_ до \_ последнего \_ обновления**</span><span class="sxs-lookup"><span data-stu-id="0e198-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="0e198-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="0e198-172">Указанное время предшествует времени, переданном последнему обновлению.</span><span class="sxs-lookup"><span data-stu-id="0e198-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e198-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_ \_ клиент таймера пользовательского интерфейса E \_ \_ уже \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="0e198-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e198-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="0e198-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="0e198-175">Этот клиент уже подключен к таймеру.</span><span class="sxs-lookup"><span data-stu-id="0e198-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e198-176">Требования</span><span class="sxs-lookup"><span data-stu-id="0e198-176">Requirements</span></span>



| <span data-ttu-id="0e198-177">Требование</span><span class="sxs-lookup"><span data-stu-id="0e198-177">Requirement</span></span> | <span data-ttu-id="0e198-178">Значение</span><span class="sxs-lookup"><span data-stu-id="0e198-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e198-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e198-179">Minimum supported client</span></span><br/> | <span data-ttu-id="0e198-180">Windows 7, Windows Vista и обновление платформы \[ только для настольных приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e198-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e198-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e198-181">Minimum supported server</span></span><br/> | <span data-ttu-id="0e198-182">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0e198-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0e198-183">Header</span><span class="sxs-lookup"><span data-stu-id="0e198-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e198-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e198-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="0e198-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e198-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e198-186">Справочник по анимации Windows</span><span class="sxs-lookup"><span data-stu-id="0e198-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

