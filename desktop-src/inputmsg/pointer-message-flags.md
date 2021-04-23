---
title: Флаги сообщения указателя
description: Значения, используемые в различных макросах указателя (см. макросы).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719202"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="e0fe1-103">Флаги сообщения указателя</span><span class="sxs-lookup"><span data-stu-id="e0fe1-103">Pointer Message Flags</span></span>

<span data-ttu-id="e0fe1-104">Значения, используемые в различных макросах указателя (см. [макросы](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="e0fe1-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e0fe1-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-107">Указывает поступление нового указателя.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e0fe1-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-110">Указывает, что этот указатель остается существующим.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="e0fe1-111">Если этот флаг не установлен, он указывает, что указатель имеет левый диапазон обнаружения.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="e0fe1-112">Этот флаг обычно не устанавливается, только если указатель мыши выходит за пределы диапазона обнаружения (**POINTER_FLAG_UPDATE** задан) или если указатель в контакте с областью окна выходит за пределы диапазона обнаружения (**POINTER_FLAG_UP** установлен).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e0fe1-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-115">Указывает, что этот указатель находится в контакте с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="e0fe1-116">Если этот флаг не установлен, он указывает на наведение указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0fe1-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-119">Указывает основное действие, аналогичное нажатию левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="e0fe1-120">Указатель касания имеет установленный флаг, когда он находится в контакте с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="e0fe1-121">Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="e0fe1-122">Указатель мыши имеет этот флаг, установленный при нажатии левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e0fe1-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-125">Указывает вторичное действие, аналогичное нажатию правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="e0fe1-126">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-127">Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера с нажатой кнопкой пера.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="e0fe1-128">Указатель мыши имеет этот флаг, установленный при нажатии правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e0fe1-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-131">Аналогично кнопке колесика мыши вниз.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="e0fe1-132">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-133">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-134">Указатель мыши имеет этот флаг, установленный при нажатии кнопки колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e0fe1-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-137">Аналог первой расширенной кнопки мыши (XButton1).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="e0fe1-138">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-139">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-140">Указатель мыши имеет этот флаг, установленный при нажатии первой кнопки расширенной мыши (XBUTTON1).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e0fe1-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-143">Аналог второй кнопки расширенной мыши (XButton2).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="e0fe1-144">Указатель касания не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-145">Указатель пера не использует этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e0fe1-146">Указатель мыши имеет этот флаг, установленный при нажатии второй кнопки расширенной мыши (XBUTTON2).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e0fe1-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-149">Указывает, что этот указатель был обозначен как основной указатель.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="e0fe1-150">Первичный указатель — это один указатель, который может выполнять действия, отличные от доступных для неосновных указателей.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="e0fe1-151">Например, когда основной указатель устанавливает контакт с областью окна, он может предоставить окну возможность активировать, отправив ему WM_POINTERACTIVATE сообщение.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="e0fe1-152">Основной указатель определяется всеми действиями текущего пользователя в системе (мышь, касание, перо и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="e0fe1-153">Таким образом, основной указатель может не быть связан с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="e0fe1-154">Первый контакт в взаимодействии с несколькими касаниями устанавливается в качестве основного указателя.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="e0fe1-155">После идентификации основного указателя все контакты должны быть ликвидированы, прежде чем новый контакт будет идентифицирован как основной указатель.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="e0fe1-156">Для приложений, которые не обрабатывают ввод указателя, только события основного указателя переносятся в события мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="e0fe1-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-159">Достоверность — это предложение от исходного устройства о том, представляет ли указатель предполагаемое или случайное взаимодействие, которое особенно важно для PT_TOUCHных указателей, где случайное взаимодействие (например, с ладонью руки) может активировать ввод.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="e0fe1-160">Наличие этого флага означает, что исходное устройство имеет высокую уверенность в том, что эти входные данные являются частью предполагаемого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e0fe1-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fe1-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="e0fe1-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="e0fe1-163">Указывает, что указатель отменяется в ненормальном режиме, например, когда система получает недопустимые входные данные для указателя или когда устройство с активными указателями внезапно прерывается.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="e0fe1-164">Если приложение, получающее входные данные, находится в определенном месте, оно должно обрабатывать взаимодействие как незавершенное и обратить любое влияние на указатель.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0fe1-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0fe1-165">Remarks</span></span>

<span data-ttu-id="e0fe1-166">XBUTTON1 и XBUTTON2 — это дополнительные кнопки, используемые на многих устройствах мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="e0fe1-167">Они возвращают те же данные, что и стандартные кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fe1-168">Требования</span><span class="sxs-lookup"><span data-stu-id="e0fe1-168">Requirements</span></span>



| <span data-ttu-id="e0fe1-169">Требование</span><span class="sxs-lookup"><span data-stu-id="e0fe1-169">Requirement</span></span> | <span data-ttu-id="e0fe1-170">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fe1-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fe1-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0fe1-171">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fe1-172">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e0fe1-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e0fe1-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0fe1-173">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fe1-174">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e0fe1-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0fe1-175">Header</span><span class="sxs-lookup"><span data-stu-id="e0fe1-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0fe1-176"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0fe1-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fe1-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0fe1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fe1-178">Константы</span><span class="sxs-lookup"><span data-stu-id="e0fe1-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-179">Макросы</span><span class="sxs-lookup"><span data-stu-id="e0fe1-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





