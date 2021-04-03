---
title: Сообщение EM_GETIMESTATUS (Winuser. h)
description: Получает набор флагов состояния, которые указывают, как элемент управления Edit взаимодействует с редактором метода ввода (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Элементы управления Windows для EM_GETIMESTATUS сообщений
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136859"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="83eaa-104">\_Сообщение ЖЕТИМЕСТАТУС EM</span><span class="sxs-lookup"><span data-stu-id="83eaa-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="83eaa-105">Получает набор флагов состояния, которые указывают, как элемент управления Edit взаимодействует с редактором метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="83eaa-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="83eaa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83eaa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83eaa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83eaa-108">Тип извлекаемого состояния.</span><span class="sxs-lookup"><span data-stu-id="83eaa-108">The type of status to retrieve.</span></span> <span data-ttu-id="83eaa-109">Этот параметр может иметь следующее значение.</span><span class="sxs-lookup"><span data-stu-id="83eaa-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="83eaa-110">Значение</span><span class="sxs-lookup"><span data-stu-id="83eaa-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="83eaa-111">Значение</span><span class="sxs-lookup"><span data-stu-id="83eaa-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="83eaa-112"><dt>**ЕМСИС \_ компоситионстринг**</dt></span><span class="sxs-lookup"><span data-stu-id="83eaa-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="83eaa-113">Задает поведение для обработки строки композиции.</span><span class="sxs-lookup"><span data-stu-id="83eaa-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83eaa-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83eaa-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83eaa-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="83eaa-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83eaa-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83eaa-116">Return value</span></span>

<span data-ttu-id="83eaa-117">Данные, относящиеся к типу извлекаемого состояния.</span><span class="sxs-lookup"><span data-stu-id="83eaa-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="83eaa-118">Если для *Status* задано значение **емсис \_ компоситионстринг** , это возвращаемое значение является одним или несколькими из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="83eaa-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="83eaa-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="83eaa-119">Return code</span></span>                                                                                                    | <span data-ttu-id="83eaa-120">Описание</span><span class="sxs-lookup"><span data-stu-id="83eaa-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83eaa-121"><dt>**ЕИМЕС \_ жеткомпстратонце**</dt></span><span class="sxs-lookup"><span data-stu-id="83eaa-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="83eaa-122">Если этот флаг установлен, элемент управления "поле ввода" ловит сообщение [**\_ \_ композиции редактора IME WM**](/windows/desktop/Intl/wm-ime-composition) с *ФФЛАГС* , настроенным на GC \_ ресултстр, и возвращает результирующую строку немедленно.</span><span class="sxs-lookup"><span data-stu-id="83eaa-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="83eaa-123">Если этот флаг не установлен, элемент управления "поле ввода" передает сообщение **\_ \_ композиции редактора WM IME** в процедуру окна по умолчанию и обрабатывает результирующую строку из сообщения [**WM \_ char**](/windows/desktop/inputdev/wm-char) . это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83eaa-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="83eaa-124"><dt>**ЕИМЕС \_ канцелкомпстринфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="83eaa-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="83eaa-125">Если этот флаг установлен, элемент управления "поле ввода" отменяет строку композиции при получении сообщения [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="83eaa-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="83eaa-126">Если этот флаг не установлен, элемент управления "поле ввода" не отменяет строку композиции; Это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83eaa-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="83eaa-127"><dt>**ЕИМЕС \_ комплетекомпстркиллфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="83eaa-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="83eaa-128">Если этот флаг установлен, элемент управления "поле ввода" завершает строку композиции после получения сообщения [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="83eaa-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="83eaa-129">Если этот флаг не установлен, то элемент управления "поле ввода" не завершает строку композиции. Это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83eaa-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="83eaa-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83eaa-130">Remarks</span></span>

<span data-ttu-id="83eaa-131">**Расширенное редактирование:** Сообщение **EM \_ жетиместатус** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83eaa-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="83eaa-132">Требования</span><span class="sxs-lookup"><span data-stu-id="83eaa-132">Requirements</span></span>



| <span data-ttu-id="83eaa-133">Требование</span><span class="sxs-lookup"><span data-stu-id="83eaa-133">Requirement</span></span> | <span data-ttu-id="83eaa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="83eaa-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83eaa-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83eaa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="83eaa-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83eaa-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83eaa-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83eaa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="83eaa-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83eaa-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83eaa-139">Header</span><span class="sxs-lookup"><span data-stu-id="83eaa-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="83eaa-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83eaa-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83eaa-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83eaa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83eaa-142">**EM \_ сетиместатус**</span><span class="sxs-lookup"><span data-stu-id="83eaa-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

