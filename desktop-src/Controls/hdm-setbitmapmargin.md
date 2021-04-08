---
title: Сообщение HDM_SETBITMAPMARGIN (Коммктрл. h)
description: Задает ширину поля, заданное в пикселях точечного рисунка в существующем элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетбитмапмаргин.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Элементы управления Windows для HDM_SETBITMAPMARGIN сообщений
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892393"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="36cb2-105">\_Сообщение СЕТБИТМАПМАРГИН HDM</span><span class="sxs-lookup"><span data-stu-id="36cb2-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="36cb2-106">Задает ширину поля, заданное в пикселях точечного рисунка в существующем элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="36cb2-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="36cb2-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетбитмапмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="36cb2-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36cb2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36cb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cb2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36cb2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cb2-110">Ширина (в пикселях) поля, охватывающего точечный рисунок в существующем элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="36cb2-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="36cb2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36cb2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36cb2-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="36cb2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cb2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36cb2-113">Return value</span></span>

<span data-ttu-id="36cb2-114">Возвращает ширину поля точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="36cb2-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="36cb2-115">Если поле точечного рисунка не было указано ранее, возвращается значение по умолчанию 3 \* [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ ккседже*).</span><span class="sxs-lookup"><span data-stu-id="36cb2-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cb2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="36cb2-116">Requirements</span></span>



| <span data-ttu-id="36cb2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="36cb2-117">Requirement</span></span> | <span data-ttu-id="36cb2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="36cb2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36cb2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36cb2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36cb2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36cb2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36cb2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36cb2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36cb2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36cb2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36cb2-123">Header</span><span class="sxs-lookup"><span data-stu-id="36cb2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cb2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36cb2-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cb2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36cb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cb2-126">**\_ЖЕТБИТМАПМАРГИН HDM**</span><span class="sxs-lookup"><span data-stu-id="36cb2-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

