---
description: '\_Константы побитового флага линефорвардмоде описывают условия, при которых вызовы к адресу можно перенаправить.'
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Константы LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689470"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="dc724-103">\_Константы линефорвардмоде</span><span class="sxs-lookup"><span data-stu-id="dc724-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="dc724-104">Константы побитового флага **линефорвардмоде \_** описывают условия, при которых вызовы к адресу можно перенаправить.</span><span class="sxs-lookup"><span data-stu-id="dc724-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="dc724-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**ЛИНЕФОРВАРДМОДЕ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="dc724-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-106">Пересылка всех вызовов в состоянии Busy, независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="dc724-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="dc724-107">Используйте это значение при пересылке внутренних и внешних вызовов в состоянии Busy, и отсутствие ответа не может контролироваться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусекстернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-109">Пересылка всех внешних вызовов в состоянии Busy.</span><span class="sxs-lookup"><span data-stu-id="dc724-109">Forward all external calls on busy.</span></span> <span data-ttu-id="dc724-110">Используйте это значение при пересылке внутренних и внешних вызовов в состоянии Busy, и отсутствие ответа можно контролировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусинтернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-112">Пересылка всех внутренних вызовов на занятии.</span><span class="sxs-lookup"><span data-stu-id="dc724-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="dc724-113">Используйте это значение при пересылке внутренних и внешних вызовов в состоянии Busy, и отсутствие ответа можно контролировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусина**</span><span class="sxs-lookup"><span data-stu-id="dc724-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-115">Перенаправлять все вызовы на "занят" или "нет", независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="dc724-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="dc724-116">Используйте это значение при пересылке внутренних и внешних вызовов в состоянии Busy, и отсутствие ответа не может контролироваться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусинаекстернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-118">Пересылка всех внешних вызовов в состоянии занятости/без ответа.</span><span class="sxs-lookup"><span data-stu-id="dc724-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="dc724-119">Используйте это значение, если Пересылка вызовов перегружена, и ни один ответ не может управляться отдельно для внутренних вызовов.</span><span class="sxs-lookup"><span data-stu-id="dc724-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусинаинтернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-121">Пересылка всех внутренних вызовов по занятости/без ответа.</span><span class="sxs-lookup"><span data-stu-id="dc724-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="dc724-122">Используйте это значение, если Пересылка вызовов перегружена, и ни один ответ не может управляться отдельно для внутренних вызовов.</span><span class="sxs-lookup"><span data-stu-id="dc724-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусинаспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="dc724-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-124">Пересылка занятости/отсутствие ответа на все вызовы, порожденные по указанному адресу (Выборочная переадресация вызовов).</span><span class="sxs-lookup"><span data-stu-id="dc724-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**ЛИНЕФОРВАРДМОДЕ \_ бусиспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="dc724-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-126">Пересылка занятых всех вызовов, поступающих по указанному адресу (Выборочная переадресация вызовов).</span><span class="sxs-lookup"><span data-stu-id="dc724-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**ЛИНЕФОРВАРДМОДЕ \_ ноансв**</span><span class="sxs-lookup"><span data-stu-id="dc724-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-128">Пересылать все вызовы без ответа независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="dc724-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="dc724-129">Используйте это значение, если переадресация вызовов для внутренних и внешних вызовов не может управляться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ ноансвекстернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-131">Пересылать все внешние вызовы без ответа.</span><span class="sxs-lookup"><span data-stu-id="dc724-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="dc724-132">Используйте это значение при пересылке внутренних и внешних вызовов без ответа, которые можно контролировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ ноансвинтернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-134">Пересылать все внутренние вызовы без ответа.</span><span class="sxs-lookup"><span data-stu-id="dc724-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="dc724-135">Используйте это значение при пересылке внутренних и внешних вызовов без ответа, которые можно контролировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**ЛИНЕФОРВАРДМОДЕ \_ ноансвспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="dc724-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-137">Пересылка без ответа на все вызовы, созданные по указанному адресу (Выборочная переадресация вызовов).</span><span class="sxs-lookup"><span data-stu-id="dc724-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**ЛИНЕФОРВАРДМОДЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="dc724-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-139">Вызовы перенаправляются, но условия, при которых происходит пересылка, неизвестны и никогда не будут известны поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="dc724-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="dc724-140">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="dc724-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**ЛИНЕФОРВАРДМОДЕ \_ унконд**</span><span class="sxs-lookup"><span data-stu-id="dc724-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-142">Пересылать все вызовы безусловно, независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="dc724-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="dc724-143">Используйте это значение, если неусловная пересылка для внутренних и внешних вызовов не может управляться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="dc724-144">Безусловное перенаправление переопределяет перенаправление перенаправления "занят" и/или не имеет условий ответа.</span><span class="sxs-lookup"><span data-stu-id="dc724-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ ункондекстернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-146">Пересылка всех внешних вызовов безусловно.</span><span class="sxs-lookup"><span data-stu-id="dc724-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="dc724-147">Используйте это значение, если неусловная пересылка для внутренних и внешних вызовов может управляться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**ЛИНЕФОРВАРДМОДЕ \_ ункондинтернал**</span><span class="sxs-lookup"><span data-stu-id="dc724-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-149">Пересылать все внутренние вызовы безусловно.</span><span class="sxs-lookup"><span data-stu-id="dc724-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="dc724-150">Используйте это значение, если неусловная пересылка для внутренних и внешних вызовов может управляться отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**ЛИНЕФОРВАРДМОДЕ \_ ункондспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="dc724-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-152">Безусловно пересылать все вызовы, порожденные по указанному адресу (Выборочная переадресация вызовов).</span><span class="sxs-lookup"><span data-stu-id="dc724-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc724-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**ЛИНЕФОРВАРДМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="dc724-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dc724-154">Вызовы перенаправляются, но условия, при которых произойдет пересылка, в настоящее время не известны.</span><span class="sxs-lookup"><span data-stu-id="dc724-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="dc724-155">Возможно, условия могут быть известны в будущем.</span><span class="sxs-lookup"><span data-stu-id="dc724-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="dc724-156">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="dc724-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc724-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc724-157">Remarks</span></span>

<span data-ttu-id="dc724-158">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="dc724-158">No extensibility.</span></span> <span data-ttu-id="dc724-159">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="dc724-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="dc724-160">Битовые флаги, определенные ЛИНЕФОРВАРДМОДЕ \_ , не являются ортогональными.</span><span class="sxs-lookup"><span data-stu-id="dc724-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="dc724-161">Безусловное перенаправление игнорирует любое определенное условие, например «занят» или «нет ответа».</span><span class="sxs-lookup"><span data-stu-id="dc724-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="dc724-162">Если неусловная пересылка не действует, перенаправление на занятый и без ответа можно контролировать отдельно или не отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="dc724-163">Если управление осуществляется отдельно, \_ Флаги линефорвардмоде Busy и линефорвардмоде \_ ноансв можно использовать отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc724-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="dc724-164">Если управление не осуществляется отдельно, \_ необходимо использовать флаг линефорвардмоде бусина.</span><span class="sxs-lookup"><span data-stu-id="dc724-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="dc724-165">Аналогично, если переадресация внутренних и внешних вызовов может контролироваться отдельно, то ЛИНЕФОРВАРДМОДЕ \_ внутренние и линефорвардмоде \_ Внешние флаги можно использовать отдельно. в противном случае используется сочетание.</span><span class="sxs-lookup"><span data-stu-id="dc724-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="dc724-166">Возможности адресации указывают, какие режимы перенаправления доступны для каждого адреса, назначенного линии.</span><span class="sxs-lookup"><span data-stu-id="dc724-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="dc724-167">Приложение может использовать [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) для установки условий переадресации в параметре.</span><span class="sxs-lookup"><span data-stu-id="dc724-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="dc724-168">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API в строке и не использовать эти значения ЛИНЕФОРВАРДМОДЕ, \_ Если согласованная версия не поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="dc724-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc724-169">Требования</span><span class="sxs-lookup"><span data-stu-id="dc724-169">Requirements</span></span>



| <span data-ttu-id="dc724-170">Требование</span><span class="sxs-lookup"><span data-stu-id="dc724-170">Requirement</span></span> | <span data-ttu-id="dc724-171">Значение</span><span class="sxs-lookup"><span data-stu-id="dc724-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dc724-172">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="dc724-172">TAPI version</span></span><br/> | <span data-ttu-id="dc724-173">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dc724-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dc724-174">Header</span><span class="sxs-lookup"><span data-stu-id="dc724-174">Header</span></span><br/>       | <dl> <span data-ttu-id="dc724-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc724-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




