---
title: Сообщение UDM_SETRANGE (Коммктрл. h)
description: Задает минимальное и максимальное положение (диапазон) для элемента управления "вверх/вниз".
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Элементы управления Windows для UDM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071803"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="8be12-104">\_Сообщение SETRANGE UDM</span><span class="sxs-lookup"><span data-stu-id="8be12-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="8be12-105">Задает минимальное и максимальное положение (диапазон) для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="8be12-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8be12-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8be12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be12-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8be12-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8be12-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8be12-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8be12-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8be12-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8be12-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **короткое** значение, указывающее максимальное значение для элемента управления "вверх/вниз", а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — **короткое** значение, указывающее минимальную длину.</span><span class="sxs-lookup"><span data-stu-id="8be12-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="8be12-111">Ни одна из позиций не может быть больше \_ значения обновления максвал или меньше значения обновления \_ минвал.</span><span class="sxs-lookup"><span data-stu-id="8be12-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="8be12-112">Кроме того, разница между двумя позициями не может превышать обновления \_ максвал.</span><span class="sxs-lookup"><span data-stu-id="8be12-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be12-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8be12-113">Return value</span></span>

<span data-ttu-id="8be12-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8be12-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be12-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8be12-115">Remarks</span></span>

<span data-ttu-id="8be12-116">Максимальная длина может быть меньше, чем минимальная.</span><span class="sxs-lookup"><span data-stu-id="8be12-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="8be12-117">При нажатии кнопки со стрелкой вверх текущее расположение перемещается ближе к максимальному положению, а нажатие кнопки со стрелкой вниз перемещается к минимальному положению.</span><span class="sxs-lookup"><span data-stu-id="8be12-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be12-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8be12-118">Requirements</span></span>



| <span data-ttu-id="8be12-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8be12-119">Requirement</span></span> | <span data-ttu-id="8be12-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8be12-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8be12-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8be12-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8be12-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8be12-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8be12-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8be12-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8be12-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8be12-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8be12-125">Header</span><span class="sxs-lookup"><span data-stu-id="8be12-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be12-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8be12-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be12-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8be12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be12-128">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="8be12-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="8be12-129">**Унифицированная многомерная модель \_**</span><span class="sxs-lookup"><span data-stu-id="8be12-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

