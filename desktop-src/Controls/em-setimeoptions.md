---
title: Сообщение EM_SETIMEOPTIONS (RichEdit. h)
description: Задает параметры редактора метода ввода (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Элементы управления Windows для EM_SETIMEOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892162"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="26035-104">\_Сообщение СЕТИМЕОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="26035-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="26035-105">Задает параметры редактора метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="26035-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="26035-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="26035-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="26035-107">Он не поддерживается в каких-либо более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="26035-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="26035-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26035-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26035-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26035-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26035-110">Задает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="26035-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="26035-111">Значение</span><span class="sxs-lookup"><span data-stu-id="26035-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="26035-112">Значение</span><span class="sxs-lookup"><span data-stu-id="26035-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="26035-113"><dt>**\_набор екуп**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="26035-114">Задает параметры, заданные параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="26035-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="26035-115"><dt>**ЕКУП \_ или**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="26035-116">Объединяет указанные параметры с текущими параметрами.</span><span class="sxs-lookup"><span data-stu-id="26035-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="26035-117"><dt>**ЕКУП \_ и**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="26035-118">Сохраняются только текущие параметры, которые также задаются параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="26035-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="26035-119"><dt>**ЕКУП \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="26035-120">Логически исключающие или текущие параметры с параметрами, указанными как *lParam.*</span><span class="sxs-lookup"><span data-stu-id="26035-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="26035-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26035-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26035-122">Указывает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="26035-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="26035-123">Значение</span><span class="sxs-lookup"><span data-stu-id="26035-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="26035-124">Значение</span><span class="sxs-lookup"><span data-stu-id="26035-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="26035-125"><dt>**интеллектуальный фильтр сообщений \_ клосестатусвиндов**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="26035-126">Закрывает окно состояния редактора IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="26035-127"><dt>**интеллектуальный фильтр сообщений \_ форцеактиве**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="26035-128">Активирует IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="26035-129"><dt>**интеллектуальный фильтр сообщений \_ форцедисабле**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="26035-130">Отключает IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="26035-131"><dt>**интеллектуальный фильтр сообщений \_ форцеенабле**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="26035-132">Включает IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="26035-133"><dt>**интеллектуальный фильтр сообщений \_ форцеинактиве**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="26035-134">Отключает IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="26035-135"><dt>**интеллектуальный фильтр сообщений \_ форценоне**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="26035-136">Отключает обработку IME.</span><span class="sxs-lookup"><span data-stu-id="26035-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="26035-137"><dt>**интеллектуальный фильтр сообщений \_ форцеремембер**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="26035-138">Восстанавливает предыдущее состояние IME, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="26035-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="26035-139"><dt>**интеллектуальный фильтр сообщений \_ мултиплидит**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="26035-140">Указывает, что строка композиции не будет отменена или определена изменением фокуса.</span><span class="sxs-lookup"><span data-stu-id="26035-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="26035-141">Это позволяет приложению иметь отдельные строки композиции для каждого элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="26035-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="26035-142"><dt>**вертикальный фильтр интеллектуального фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26035-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="26035-143">Примечание, используемое в расширенном редактировании 2,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="26035-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26035-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26035-144">Return value</span></span>

<span data-ttu-id="26035-145">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="26035-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="26035-146">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="26035-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="26035-147">Требования</span><span class="sxs-lookup"><span data-stu-id="26035-147">Requirements</span></span>



| <span data-ttu-id="26035-148">Требование</span><span class="sxs-lookup"><span data-stu-id="26035-148">Requirement</span></span> | <span data-ttu-id="26035-149">Значение</span><span class="sxs-lookup"><span data-stu-id="26035-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26035-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26035-150">Minimum supported client</span></span><br/> | <span data-ttu-id="26035-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26035-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26035-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26035-152">Minimum supported server</span></span><br/> | <span data-ttu-id="26035-153">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26035-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26035-154">Header</span><span class="sxs-lookup"><span data-stu-id="26035-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="26035-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="26035-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26035-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26035-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26035-157">**EM \_ жетимеоптионс**</span><span class="sxs-lookup"><span data-stu-id="26035-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





