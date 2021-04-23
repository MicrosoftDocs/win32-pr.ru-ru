---
title: Сообщение HDM_GETBITMAPMARGIN (Коммктрл. h)
description: Возвращает ширину поля точечного рисунка для элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетбитмапмаргин.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Элементы управления Windows для HDM_GETBITMAPMARGIN сообщений
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988695"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="4e088-105">\_Сообщение ЖЕТБИТМАПМАРГИН HDM</span><span class="sxs-lookup"><span data-stu-id="4e088-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="4e088-106">Возвращает ширину поля точечного рисунка для элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="4e088-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="4e088-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетбитмапмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="4e088-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e088-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e088-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e088-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e088-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4e088-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4e088-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4e088-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e088-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e088-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4e088-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e088-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e088-113">Return value</span></span>

<span data-ttu-id="4e088-114">Возвращает ширину поля точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4e088-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="4e088-115">Если поле точечного рисунка не было указано ранее, возвращается значение по умолчанию 3 \* [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ ккседже).</span><span class="sxs-lookup"><span data-stu-id="4e088-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e088-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4e088-116">Requirements</span></span>



| <span data-ttu-id="4e088-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4e088-117">Requirement</span></span> | <span data-ttu-id="4e088-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4e088-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e088-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e088-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e088-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e088-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e088-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e088-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e088-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e088-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e088-123">Header</span><span class="sxs-lookup"><span data-stu-id="4e088-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e088-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e088-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e088-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e088-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e088-126">**\_СЕТБИТМАПМАРГИН HDM**</span><span class="sxs-lookup"><span data-stu-id="4e088-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

