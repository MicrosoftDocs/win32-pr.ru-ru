---
title: Сообщение EM_GETCTFMODEBIAS (RichEdit. h)
description: Возвращает значения смещения режима платформы текстовых служб для элемента управления Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Элементы управления Windows для EM_GETCTFMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136139"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="ff332-104">\_Сообщение ЖЕТКТФМОДЕБИАС EM</span><span class="sxs-lookup"><span data-stu-id="ff332-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="ff332-105">Возвращает значения смещения режима платформы текстовых служб для элемента управления Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ff332-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff332-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff332-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff332-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff332-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ff332-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ff332-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff332-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff332-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ff332-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff332-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff332-111">Return value</span></span>

<span data-ttu-id="ff332-112">Текущее значение смещения в режиме платформы текстовых служб.</span><span class="sxs-lookup"><span data-stu-id="ff332-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff332-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff332-113">Remarks</span></span>

<span data-ttu-id="ff332-114">Чтобы получить смещение режима IME, вызовите [**EM \_ жетимемодебиас**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="ff332-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff332-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ff332-115">Requirements</span></span>



| <span data-ttu-id="ff332-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ff332-116">Requirement</span></span> | <span data-ttu-id="ff332-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ff332-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff332-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff332-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff332-119">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff332-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff332-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff332-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff332-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff332-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff332-122">Header</span><span class="sxs-lookup"><span data-stu-id="ff332-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff332-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff332-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff332-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff332-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff332-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ff332-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff332-126">**EM \_ сетктфмодебиас**</span><span class="sxs-lookup"><span data-stu-id="ff332-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="ff332-127">**EM \_ жетимемодебиас**</span><span class="sxs-lookup"><span data-stu-id="ff332-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





