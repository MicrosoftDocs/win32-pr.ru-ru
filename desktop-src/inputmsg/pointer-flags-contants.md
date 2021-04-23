---
title: Флаги указателя
description: Значения, которые могут отображаться в поле Поинтерфлагс структуры POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802897"
---
# <a name="pointer-flags"></a><span data-ttu-id="d317f-103">Флаги указателя</span><span class="sxs-lookup"><span data-stu-id="d317f-103">Pointer Flags</span></span>

<span data-ttu-id="d317f-104">Значения, которые могут отображаться в поле **поинтерфлагс** структуры [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d317f-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="d317f-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="d317f-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d317f-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d317f-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="d317f-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d317f-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="d317f-110">Указывает поступление нового указателя.</span><span class="sxs-lookup"><span data-stu-id="d317f-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="d317f-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d317f-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="d317f-113">Указывает, что этот указатель остается существующим.</span><span class="sxs-lookup"><span data-stu-id="d317f-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="d317f-114">Если этот флаг не установлен, он указывает, что указатель имеет левый диапазон обнаружения.</span><span class="sxs-lookup"><span data-stu-id="d317f-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="d317f-115">Этот флаг обычно не устанавливается, только если указатель мыши выходит за пределы диапазона обнаружения (**POINTER_FLAG_UPDATE** задан) или если указатель в контакте с областью окна выходит за пределы диапазона обнаружения (**POINTER_FLAG_UP** установлен).</span><span class="sxs-lookup"><span data-stu-id="d317f-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="d317f-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d317f-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="d317f-118">Указывает, что этот указатель находится в контакте с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="d317f-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="d317f-119">Если этот флаг не установлен, он указывает на наведение указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d317f-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d317f-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="d317f-122">Указывает основное действие, аналогичное нажатию левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="d317f-123">Указатель касания имеет установленный флаг, когда он находится в контакте с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="d317f-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="d317f-124">Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.</span><span class="sxs-lookup"><span data-stu-id="d317f-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="d317f-125">Указатель мыши имеет этот флаг, установленный при нажатии левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d317f-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d317f-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="d317f-128">Указывает вторичное действие, аналогичное нажатию правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="d317f-129">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-130">Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера с нажатой кнопкой пера.</span><span class="sxs-lookup"><span data-stu-id="d317f-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="d317f-131">Указатель мыши имеет этот флаг, установленный при нажатии правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d317f-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d317f-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="d317f-134">Аналогично кнопке колесика мыши вниз.</span><span class="sxs-lookup"><span data-stu-id="d317f-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="d317f-135">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-136">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-137">Указатель мыши имеет этот флаг, установленный при нажатии кнопки колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d317f-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d317f-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="d317f-140">Аналог первой расширенной кнопки мыши (XButton1).</span><span class="sxs-lookup"><span data-stu-id="d317f-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="d317f-141">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-142">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-143">Указатель мыши имеет этот флаг, установленный при нажатии первой кнопки расширенной мыши (XBUTTON1).</span><span class="sxs-lookup"><span data-stu-id="d317f-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d317f-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d317f-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="d317f-146">Аналог второй кнопки расширенной мыши (XButton2).</span><span class="sxs-lookup"><span data-stu-id="d317f-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="d317f-147">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-148">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="d317f-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="d317f-149">Указатель мыши имеет этот флаг, установленный при нажатии второй кнопки расширенной мыши (XBUTTON2).</span><span class="sxs-lookup"><span data-stu-id="d317f-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="d317f-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d317f-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-152">Указывает, что этот указатель был обозначен как основной указатель.</span><span class="sxs-lookup"><span data-stu-id="d317f-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="d317f-153">Первичный указатель — это один указатель, который может выполнять действия, отличные от доступных для неосновных указателей.</span><span class="sxs-lookup"><span data-stu-id="d317f-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="d317f-154">Например, когда основной указатель устанавливает контакт с областью окна, он может предоставить окну возможность активировать, отправив ему [**WM_POINTERACTIVATE**](wm-pointeractivate.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="d317f-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="d317f-155">Основной указатель определяется всеми действиями текущего пользователя в системе (мышь, касание, перо и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d317f-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="d317f-156">Таким образом, основной указатель может не быть связан с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="d317f-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="d317f-157">Первый контакт в взаимодействии с несколькими касаниями устанавливается в качестве основного указателя.</span><span class="sxs-lookup"><span data-stu-id="d317f-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="d317f-158">После идентификации основного указателя все контакты должны быть ликвидированы, прежде чем новый контакт будет идентифицирован как основной указатель.</span><span class="sxs-lookup"><span data-stu-id="d317f-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="d317f-159">Для приложений, которые не обрабатывают ввод указателя, только события основного указателя переносятся в события мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="d317f-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="d317f-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-162">Достоверность — это предложение от исходного устройства о том, представляет ли указатель предполагаемое или случайное взаимодействие, которое особенно важно для PT_TOUCHных указателей, где случайное взаимодействие (например, с ладонью руки) может активировать ввод.</span><span class="sxs-lookup"><span data-stu-id="d317f-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="d317f-163">Наличие этого флага означает, что исходное устройство имеет высокую уверенность в том, что эти входные данные являются частью предполагаемого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d317f-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="d317f-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="d317f-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-166">Указывает, что указатель отменяется в ненормальном режиме, например, когда система получает недопустимые входные данные для указателя или когда устройство с активными указателями внезапно прерывается.</span><span class="sxs-lookup"><span data-stu-id="d317f-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="d317f-167">Если приложение, получающее входные данные, находится в определенном месте, оно должно обрабатывать взаимодействие как незавершенное и обратить любое влияние на указатель.</span><span class="sxs-lookup"><span data-stu-id="d317f-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="d317f-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d317f-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-170">Указывает, что этот указатель перешел в Нештатное состояние; то есть он сделал контакт с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="d317f-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="d317f-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d317f-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-173">Указывает, что это простое обновление, которое не включает изменение состояния указателя.</span><span class="sxs-lookup"><span data-stu-id="d317f-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="d317f-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="d317f-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-176">Указывает, что этот указатель перешел в состояние Up. Это значит, что контакт с поверхностью дигитайзера закончился.</span><span class="sxs-lookup"><span data-stu-id="d317f-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="d317f-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d317f-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-179">Указывает входные данные, связанные с колесом-указателем.</span><span class="sxs-lookup"><span data-stu-id="d317f-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="d317f-180">Для указателей мыши это эквивалентно действию колесика прокрутки мыши ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="d317f-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="d317f-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d317f-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-183">Указывает входные данные, связанные с указателем h-Wheel.</span><span class="sxs-lookup"><span data-stu-id="d317f-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="d317f-184">Для указателей мыши это эквивалентно действию колеса горизонтальной прокрутки мыши ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="d317f-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="d317f-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="d317f-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-187">Указывает, что этот указатель был захвачен (связан с) другим элементом, а исходный элемент потерял захват (см. [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="d317f-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d317f-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="d317f-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d317f-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="d317f-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="d317f-190">Указывает, что этот указатель имеет связанное преобразование.</span><span class="sxs-lookup"><span data-stu-id="d317f-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d317f-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d317f-191">Remarks</span></span>

<span data-ttu-id="d317f-192">XBUTTON1 и XBUTTON2 — это дополнительные кнопки, используемые на многих устройствах мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="d317f-193">Они возвращают те же данные, что и стандартные кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="d317f-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="d317f-194">Требования</span><span class="sxs-lookup"><span data-stu-id="d317f-194">Requirements</span></span>



| <span data-ttu-id="d317f-195">Требование</span><span class="sxs-lookup"><span data-stu-id="d317f-195">Requirement</span></span> | <span data-ttu-id="d317f-196">Значение</span><span class="sxs-lookup"><span data-stu-id="d317f-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d317f-197">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d317f-197">Minimum supported client</span></span><br/> | <span data-ttu-id="d317f-198">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d317f-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d317f-199">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d317f-199">Minimum supported server</span></span><br/> | <span data-ttu-id="d317f-200">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d317f-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d317f-201">Header</span><span class="sxs-lookup"><span data-stu-id="d317f-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="d317f-202"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="d317f-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d317f-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d317f-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d317f-204">Константы</span><span class="sxs-lookup"><span data-stu-id="d317f-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="d317f-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="d317f-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d317f-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d317f-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

