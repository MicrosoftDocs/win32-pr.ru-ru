---
title: Сообщение TCM_SETITEMSIZE (Коммктрл. h)
description: Задает ширину и высоту вкладок в элементе управления вкладки с фиксированной шириной или владельцем. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетитемсизе.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Элементы управления Windows для TCM_SETITEMSIZE сообщений
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891401"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="27615-105">\_Сообщение СЕТИТЕМСИЗЕ TCM</span><span class="sxs-lookup"><span data-stu-id="27615-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="27615-106">Задает ширину и высоту вкладок в элементе управления вкладки с фиксированной шириной или владельцем.</span><span class="sxs-lookup"><span data-stu-id="27615-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="27615-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетитемсизе**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .</span><span class="sxs-lookup"><span data-stu-id="27615-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27615-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="27615-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27615-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27615-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="27615-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="27615-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="27615-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27615-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27615-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это значение **типа int** , указывающее новую ширину в пикселях.</span><span class="sxs-lookup"><span data-stu-id="27615-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="27615-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это значение **типа int** , указывающее новую высоту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="27615-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27615-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27615-114">Return value</span></span>

<span data-ttu-id="27615-115">Возвращает старую ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="27615-115">Returns the old width and height.</span></span> <span data-ttu-id="27615-116">Ширина находится в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) возвращаемого значения, а высота — в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="27615-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="27615-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27615-117">Remarks</span></span>

<span data-ttu-id="27615-118">Если для ширины задано значение меньше ширины изображения, установленного параметром [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), ширина вкладки устанавливается равным наименьшему значению, превышающему ширину изображения.</span><span class="sxs-lookup"><span data-stu-id="27615-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="27615-119">Требования</span><span class="sxs-lookup"><span data-stu-id="27615-119">Requirements</span></span>



| <span data-ttu-id="27615-120">Требование</span><span class="sxs-lookup"><span data-stu-id="27615-120">Requirement</span></span> | <span data-ttu-id="27615-121">Значение</span><span class="sxs-lookup"><span data-stu-id="27615-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27615-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27615-122">Minimum supported client</span></span><br/> | <span data-ttu-id="27615-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27615-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27615-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27615-124">Minimum supported server</span></span><br/> | <span data-ttu-id="27615-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27615-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27615-126">Header</span><span class="sxs-lookup"><span data-stu-id="27615-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="27615-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="27615-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

