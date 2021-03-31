---
title: Сообщение PGM_GETBUTTONSIZE (Коммктрл. h)
description: Получает текущий размер кнопки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбуттонсизе пейджера.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Элементы управления Windows для PGM_GETBUTTONSIZE сообщений
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071813"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="e4288-105">\_Сообщение ЖЕТБУТТОНСИЗЕ PGM</span><span class="sxs-lookup"><span data-stu-id="e4288-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="e4288-106">Получает текущий размер кнопки для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="e4288-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="e4288-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетбуттонсизе пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="e4288-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4288-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4288-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4288-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e4288-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e4288-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e4288-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4288-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e4288-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e4288-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4288-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4288-113">Return value</span></span>

<span data-ttu-id="e4288-114">Возвращает значение типа INT, которое содержит текущий размер кнопки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e4288-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4288-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e4288-115">Requirements</span></span>



| <span data-ttu-id="e4288-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e4288-116">Requirement</span></span> | <span data-ttu-id="e4288-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e4288-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4288-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4288-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4288-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4288-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4288-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4288-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4288-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4288-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4288-122">Header</span><span class="sxs-lookup"><span data-stu-id="e4288-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4288-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4288-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4288-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4288-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4288-125">**\_СЕТБУТТОНСИЗЕ PGM**</span><span class="sxs-lookup"><span data-stu-id="e4288-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





