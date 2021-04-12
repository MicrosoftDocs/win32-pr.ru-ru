---
title: Сообщение EM_SHOWBALLOONTIP (Коммктрл. h)
description: В \_ сообщении EM шовбаллунтип отображается всплывающая подсказка, связанная с элементом управления "поле ввода".
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Элементы управления Windows для EM_SHOWBALLOONTIP сообщений
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136250"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="72efe-104">\_Сообщение ШОВБАЛЛУНТИП EM</span><span class="sxs-lookup"><span data-stu-id="72efe-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="72efe-105">В сообщении **EM \_ шовбаллунтип** отображается всплывающая подсказка, связанная с элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="72efe-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="72efe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72efe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72efe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72efe-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="72efe-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="72efe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72efe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72efe-110">Указатель на структуру [**едитбаллунтип**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) , содержащую сведения о всплывающей подсказке для отображения.</span><span class="sxs-lookup"><span data-stu-id="72efe-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72efe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72efe-111">Return value</span></span>

<span data-ttu-id="72efe-112">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="72efe-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="72efe-113">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="72efe-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72efe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72efe-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72efe-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="72efe-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="72efe-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72efe-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72efe-117">Требования</span><span class="sxs-lookup"><span data-stu-id="72efe-117">Requirements</span></span>



| <span data-ttu-id="72efe-118">Требование</span><span class="sxs-lookup"><span data-stu-id="72efe-118">Requirement</span></span> | <span data-ttu-id="72efe-119">Значение</span><span class="sxs-lookup"><span data-stu-id="72efe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72efe-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72efe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72efe-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72efe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72efe-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72efe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72efe-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72efe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72efe-124">Header</span><span class="sxs-lookup"><span data-stu-id="72efe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72efe-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="72efe-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72efe-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72efe-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="72efe-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="72efe-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72efe-128">**едитбаллунтип**</span><span class="sxs-lookup"><span data-stu-id="72efe-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="72efe-129">**Изменить \_ шовбаллунтип**</span><span class="sxs-lookup"><span data-stu-id="72efe-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





