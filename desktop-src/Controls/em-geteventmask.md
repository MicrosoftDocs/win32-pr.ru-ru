---
title: Сообщение EM_GETEVENTMASK (RichEdit. h)
description: Извлекает маску события для элемента управления Rich Edit. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Элементы управления Windows для EM_GETEVENTMASK сообщений
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989016"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="2cf80-105">\_Сообщение GETEVENTMASK EM</span><span class="sxs-lookup"><span data-stu-id="2cf80-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="2cf80-106">Извлекает маску события для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2cf80-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="2cf80-107">Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="2cf80-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cf80-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cf80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf80-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cf80-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf80-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2cf80-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2cf80-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cf80-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf80-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2cf80-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf80-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cf80-113">Return value</span></span>

<span data-ttu-id="2cf80-114">Это сообщение возвращает маску события для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2cf80-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf80-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2cf80-115">Requirements</span></span>



| <span data-ttu-id="2cf80-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2cf80-116">Requirement</span></span> | <span data-ttu-id="2cf80-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2cf80-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf80-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cf80-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf80-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cf80-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2cf80-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cf80-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf80-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2cf80-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2cf80-122">Header</span><span class="sxs-lookup"><span data-stu-id="2cf80-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf80-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf80-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf80-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cf80-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="2cf80-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2cf80-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2cf80-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="2cf80-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="2cf80-127">**Флаги Маски событий элемента управления Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="2cf80-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





