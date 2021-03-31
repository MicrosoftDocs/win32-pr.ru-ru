---
title: Сообщение EM_HIDEBALLOONTIP (Коммктрл. h)
description: Скрывает все всплывающие подсказки, связанные с элементом управления "изменение".
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- Элементы управления Windows для EM_HIDEBALLOONTIP сообщений
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988268"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="bbbae-104">\_Сообщение ХИДЕБАЛЛУНТИП EM</span><span class="sxs-lookup"><span data-stu-id="bbbae-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="bbbae-105">Скрывает все всплывающие подсказки, связанные с элементом управления "изменение".</span><span class="sxs-lookup"><span data-stu-id="bbbae-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbbae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbbae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbbae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbbae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbbae-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bbbae-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bbbae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbbae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbbae-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bbbae-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbbae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbbae-111">Return value</span></span>

<span data-ttu-id="bbbae-112">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="bbbae-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="bbbae-113">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="bbbae-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbbae-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbbae-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bbbae-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="bbbae-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bbbae-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bbbae-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bbbae-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bbbae-117">Requirements</span></span>



| <span data-ttu-id="bbbae-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bbbae-118">Requirement</span></span> | <span data-ttu-id="bbbae-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bbbae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbae-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbbae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbae-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbbae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbbae-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbbae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbae-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbbae-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbbae-124">Header</span><span class="sxs-lookup"><span data-stu-id="bbbae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbbae-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbbae-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbbae-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbbae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbae-127">**Изменить \_ хидебаллунтип**</span><span class="sxs-lookup"><span data-stu-id="bbbae-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





