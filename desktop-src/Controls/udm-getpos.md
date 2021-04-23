---
title: Сообщение UDM_GETPOS (Коммктрл. h)
description: Извлекает текущее расположение элемента управления "вверх-вниз" с 16-разрядной точностью.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Элементы управления Windows для UDM_GETPOS сообщений
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654437"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="0d1b7-104">\_Сообщение ЖЕТПОС UDM</span><span class="sxs-lookup"><span data-stu-id="0d1b7-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="0d1b7-105">Извлекает текущее расположение элемента управления "вверх-вниз" с 16-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d1b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d1b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1b7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d1b7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d1b7-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d1b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d1b7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0d1b7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1b7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d1b7-111">Return value</span></span>

<span data-ttu-id="0d1b7-112">В случае успеха для [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) устанавливается нулевое значение, а для [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задается текущее расположение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="0d1b7-113">При возникновении ошибки **HIWORD** задается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1b7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d1b7-114">Remarks</span></span>

<span data-ttu-id="0d1b7-115">При обработке этого сообщения элемент управления "вверх-вниз" обновляет свое текущее расположение на основе заголовка окна собеседника.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="0d1b7-116">Элемент управления "вверх-вниз" возвращает ошибку, если нет окна собеседника или если в заголовке указано недопустимое или недействительное значение.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="0d1b7-117">Кроме того, флаг ошибки задается в HIWORD возвращаемого значения, если элемент управления создается без стиля [**доменов обновления \_ сетбуддинт**](up-down-control-styles.md) , хотя он возвращает допустимое значение координаты в ловорд возврата.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="0d1b7-118">Если 32-разрядные значения включены для элемента управления "вверх/вниз" с помощью [**UDM \_ SETRANGE32**](udm-setrange32.md), это сообщение возвращает только младшие 16 разряды расположения.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="0d1b7-119">Чтобы получить полное 32-разрядное расположение, используйте [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="0d1b7-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1b7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0d1b7-120">Requirements</span></span>



| <span data-ttu-id="0d1b7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0d1b7-121">Requirement</span></span> | <span data-ttu-id="0d1b7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0d1b7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1b7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d1b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1b7-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d1b7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d1b7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d1b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1b7-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d1b7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d1b7-127">Header</span><span class="sxs-lookup"><span data-stu-id="0d1b7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1b7-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1b7-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1b7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d1b7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d1b7-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d1b7-131">**многомерный \_ диапазон UDM**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="0d1b7-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="0d1b7-133">**\_СЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="0d1b7-134">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

