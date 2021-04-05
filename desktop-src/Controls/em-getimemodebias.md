---
title: Сообщение EM_GETIMEMODEBIAS (RichEdit. h)
description: Получает смещение режима редактора метода ввода (IME) для элемента управления Microsoft Rich Edit.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Элементы управления Windows для EM_GETIMEMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071820"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="8691a-104">\_Сообщение ЖЕТИМЕМОДЕБИАС EM</span><span class="sxs-lookup"><span data-stu-id="8691a-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="8691a-105">Получает смещение режима редактора метода ввода (IME) для элемента управления Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8691a-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8691a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8691a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8691a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8691a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8691a-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8691a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8691a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8691a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8691a-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8691a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8691a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8691a-111">Return value</span></span>

<span data-ttu-id="8691a-112">Это сообщение возвращает текущий параметр смещения режима IME.</span><span class="sxs-lookup"><span data-stu-id="8691a-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="8691a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8691a-113">Remarks</span></span>

<span data-ttu-id="8691a-114">Чтобы получить значение смещения в режиме платформы текстовых служб, используйте [**EM \_ жетктфмодебиас**](em-getctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="8691a-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="8691a-115">Перед вызовом этой функции приложение должно вызвать [**EM \_ исиме**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="8691a-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8691a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8691a-116">Requirements</span></span>



| <span data-ttu-id="8691a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8691a-117">Requirement</span></span> | <span data-ttu-id="8691a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8691a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8691a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8691a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8691a-120">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="8691a-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8691a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8691a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8691a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8691a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8691a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8691a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8691a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8691a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8691a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8691a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8691a-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8691a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8691a-127">**EM \_ исиме**</span><span class="sxs-lookup"><span data-stu-id="8691a-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="8691a-128">**EM \_ жетктфмодебиас**</span><span class="sxs-lookup"><span data-stu-id="8691a-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





