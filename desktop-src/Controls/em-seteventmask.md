---
title: Сообщение EM_SETEVENTMASK (RichEdit. h)
description: Задает маску события для элемента управления расширенного редактирования. Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Элементы управления Windows для EM_SETEVENTMASK сообщений
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492459"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="fd447-105">\_Сообщение SETEVENTMASK EM</span><span class="sxs-lookup"><span data-stu-id="fd447-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="fd447-106">Задает маску события для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="fd447-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="fd447-107">Маска событий определяет, какие коды уведомлений отправляет элемент управления в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="fd447-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd447-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd447-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd447-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd447-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fd447-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd447-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd447-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd447-112">Новая маска событий для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fd447-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="fd447-113">Список масок событий см. в разделе [**Флаги Маски событий элемента управления Rich Edit**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fd447-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd447-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd447-114">Return value</span></span>

<span data-ttu-id="fd447-115">Это сообщение возвращает предыдущую маску события.</span><span class="sxs-lookup"><span data-stu-id="fd447-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd447-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd447-116">Remarks</span></span>

<span data-ttu-id="fd447-117">Маска события по умолчанию (перед любым набором) — ЕНМ \_ None.</span><span class="sxs-lookup"><span data-stu-id="fd447-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd447-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fd447-118">Requirements</span></span>



| <span data-ttu-id="fd447-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fd447-119">Requirement</span></span> | <span data-ttu-id="fd447-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fd447-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd447-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd447-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd447-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd447-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd447-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd447-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd447-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd447-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd447-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd447-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd447-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd447-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd447-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd447-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd447-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fd447-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fd447-129">**EM \_ GETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="fd447-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="fd447-130">**Флаги Маски событий элемента управления Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="fd447-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





