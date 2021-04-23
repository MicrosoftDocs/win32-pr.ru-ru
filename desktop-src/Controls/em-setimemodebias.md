---
title: Сообщение EM_SETIMEMODEBIAS (RichEdit. h)
description: Задайте смещение режима редактора метода ввода (IME) для элемента управления расширенного редактирования.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Элементы управления Windows для EM_SETIMEMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491211"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="1ece3-104">\_Сообщение СЕТИМЕМОДЕБИАС EM</span><span class="sxs-lookup"><span data-stu-id="1ece3-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="1ece3-105">Задайте смещение режима редактора метода ввода (IME) для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ece3-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ece3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ece3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ece3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ece3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ece3-108">Значение смещения режима IME.</span><span class="sxs-lookup"><span data-stu-id="1ece3-108">IME mode bias value.</span></span> <span data-ttu-id="1ece3-109">Может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="1ece3-109">It can be one of the following.</span></span>



| <span data-ttu-id="1ece3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1ece3-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="1ece3-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1ece3-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="1ece3-112"><dt>**интеллектуальный фильтр сообщений \_ смоде \_ плауралклаусе**</dt></span><span class="sxs-lookup"><span data-stu-id="1ece3-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="1ece3-113">Задает для смещения режима IME значение Name.</span><span class="sxs-lookup"><span data-stu-id="1ece3-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="1ece3-114"><dt>**интеллектуальный фильтр сообщений \_ смоде \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="1ece3-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="1ece3-115">Без смещения.</span><span class="sxs-lookup"><span data-stu-id="1ece3-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="1ece3-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ece3-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ece3-117">Это должно быть то же значение, что и параметр *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1ece3-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ece3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ece3-118">Return value</span></span>

<span data-ttu-id="1ece3-119">Это сообщение возвращает новый параметр смещения режима IME.</span><span class="sxs-lookup"><span data-stu-id="1ece3-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ece3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ece3-120">Remarks</span></span>

<span data-ttu-id="1ece3-121">Когда редактор IME создает список альтернативных символов, это сообщение задает условия, по которым некоторые из вариантов будут отображаться в верхней части списка.</span><span class="sxs-lookup"><span data-stu-id="1ece3-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="1ece3-122">Чтобы задать уровень смещения в режиме платформы текстовых служб (TSF), используйте [**EM \_ сетктфмодебиас**](em-setctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="1ece3-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="1ece3-123">Перед вызовом этой функции приложение должно вызвать [**EM \_ исиме**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="1ece3-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ece3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1ece3-124">Requirements</span></span>



| <span data-ttu-id="1ece3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1ece3-125">Requirement</span></span> | <span data-ttu-id="1ece3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1ece3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ece3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ece3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ece3-128">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ece3-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ece3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ece3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ece3-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ece3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ece3-131">Header</span><span class="sxs-lookup"><span data-stu-id="1ece3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ece3-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ece3-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ece3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ece3-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ece3-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1ece3-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ece3-135">**EM \_ исиме**</span><span class="sxs-lookup"><span data-stu-id="1ece3-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="1ece3-136">**EM \_ сетктфмодебиас**</span><span class="sxs-lookup"><span data-stu-id="1ece3-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





