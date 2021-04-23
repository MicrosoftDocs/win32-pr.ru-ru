---
title: Сообщение UDM_GETPOS32 (Коммктрл. h)
description: Возвращает 32-разрядное расположение элемента управления "вверх/вниз".
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Элементы управления Windows для UDM_GETPOS32 сообщений
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489618"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="19213-104">\_Сообщение GETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="19213-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="19213-105">Возвращает 32-разрядное расположение элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="19213-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="19213-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19213-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19213-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19213-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="19213-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19213-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19213-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19213-110">Указатель на **логическое** значение, равное нулю, если значение успешно получено или ненулевое при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="19213-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="19213-111">Если этот параметр имеет значение **null**, сообщения об ошибках не выводятся.</span><span class="sxs-lookup"><span data-stu-id="19213-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="19213-112">Если **\_ GETPOS32 UDM** используется в межпроцессной ситуации, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="19213-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19213-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19213-113">Return value</span></span>

<span data-ttu-id="19213-114">Возвращает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="19213-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="19213-115">Приложения должны проверить значение *lParam* , чтобы определить, является ли возвращаемое значение допустимым.</span><span class="sxs-lookup"><span data-stu-id="19213-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="19213-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19213-116">Remarks</span></span>

<span data-ttu-id="19213-117">При обработке этого сообщения элемент управления "вверх-вниз" обновляет свое текущее расположение на основе заголовка окна собеседника.</span><span class="sxs-lookup"><span data-stu-id="19213-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="19213-118">Он возвращает ошибку, если нет дружественного окна или если в заголовке указано недопустимое или недействительное значение.</span><span class="sxs-lookup"><span data-stu-id="19213-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19213-119">Требования</span><span class="sxs-lookup"><span data-stu-id="19213-119">Requirements</span></span>



| <span data-ttu-id="19213-120">Требование</span><span class="sxs-lookup"><span data-stu-id="19213-120">Requirement</span></span> | <span data-ttu-id="19213-121">Значение</span><span class="sxs-lookup"><span data-stu-id="19213-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19213-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19213-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19213-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19213-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19213-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19213-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19213-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19213-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19213-126">Header</span><span class="sxs-lookup"><span data-stu-id="19213-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19213-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="19213-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19213-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19213-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="19213-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="19213-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19213-130">**\_ЖЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="19213-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="19213-131">**\_СЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="19213-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="19213-132">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="19213-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





