---
title: Сообщение EM_SETIMESTATUS (Winuser. h)
description: Задает флаги состояния, определяющие взаимодействие элемента управления редактирования с редактором метода ввода (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Элементы управления Windows для EM_SETIMESTATUS сообщений
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802657"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="4b36f-104">\_Сообщение СЕТИМЕСТАТУС EM</span><span class="sxs-lookup"><span data-stu-id="4b36f-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="4b36f-105">Задает флаги состояния, определяющие взаимодействие элемента управления редактирования с редактором метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="4b36f-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="4b36f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b36f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b36f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b36f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b36f-108">Тип состояния, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="4b36f-108">The type of status to set.</span></span> <span data-ttu-id="4b36f-109">Этот параметр может иметь следующее значение.</span><span class="sxs-lookup"><span data-stu-id="4b36f-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="4b36f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="4b36f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="4b36f-112"><dt>**ЕМСИС \_ компоситионстринг**</dt></span><span class="sxs-lookup"><span data-stu-id="4b36f-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="4b36f-113">Задает поведение для обработки строки композиции.</span><span class="sxs-lookup"><span data-stu-id="4b36f-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4b36f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b36f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b36f-115">Данные, относящиеся к типу состояния.</span><span class="sxs-lookup"><span data-stu-id="4b36f-115">Data specific to the status type.</span></span> <span data-ttu-id="4b36f-116">Если параметр *wParam* имеет значение **емсис \_ компоситионстринг**, это может быть одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4b36f-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4b36f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="4b36f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="4b36f-119"><dt>**ЕИМЕС \_ жеткомпстратонце**</dt></span><span class="sxs-lookup"><span data-stu-id="4b36f-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="4b36f-120">Если этот флаг установлен, элемент управления "поле ввода" ловит сообщение [**\_ \_ композиции редактора IME WM**](/windows/desktop/Intl/wm-ime-composition) с параметром *lParam* , имеющим значение "GC ресултстр", \_ и возвращает результирующую строку немедленно.</span><span class="sxs-lookup"><span data-stu-id="4b36f-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="4b36f-121">Если этот флаг не установлен, элемент управления "поле ввода" передает сообщение **\_ \_ композиции редактора WM IME** в процедуру окна по умолчанию и обрабатывает результирующую строку из сообщения [**WM \_ char**](/windows/desktop/inputdev/wm-char) . это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b36f-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="4b36f-122"><dt>**ЕИМЕС \_ канцелкомпстринфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="4b36f-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="4b36f-123">Если этот флаг установлен, элемент управления "поле ввода" отменяет строку композиции при получении сообщения [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="4b36f-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="4b36f-124">Если этот флаг не установлен, элемент управления "поле ввода" не отменяет строку композиции; Это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b36f-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="4b36f-125"><dt>**ЕИМЕС \_ комплетекомпстркиллфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="4b36f-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="4b36f-126">Если этот флаг установлен, элемент управления "поле ввода" завершает строку композиции после получения сообщения [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="4b36f-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="4b36f-127">Если этот флаг не установлен, то элемент управления "поле ввода" не завершает строку композиции. Это поведение элемента управления "поле ввода" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b36f-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b36f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-128">Return value</span></span>

<span data-ttu-id="4b36f-129">Возвращает предыдущее значение параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4b36f-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b36f-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b36f-130">Remarks</span></span>

<span data-ttu-id="4b36f-131">**Расширенное редактирование:** Сообщение **EM \_ сетиместатус** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b36f-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b36f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4b36f-132">Requirements</span></span>



| <span data-ttu-id="4b36f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4b36f-133">Requirement</span></span> | <span data-ttu-id="4b36f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4b36f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b36f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b36f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4b36f-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b36f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b36f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b36f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4b36f-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b36f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b36f-139">Header</span><span class="sxs-lookup"><span data-stu-id="4b36f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b36f-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b36f-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b36f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b36f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b36f-142">**EM \_ жетиместатус**</span><span class="sxs-lookup"><span data-stu-id="4b36f-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

