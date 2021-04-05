---
title: Сообщение SBM_ENABLE_ARROWS (Winuser. h)
description: Приложение отправляет \_ \_ сообщение со СТРЕЛКАми СБМ, чтобы включить или отключить одну или обе стрелки элемента управления "полоса прокрутки".
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Элементы управления Windows для SBM_ENABLE_ARROWS сообщений
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989070"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="d9935-104">СБМ \_ включить \_ сообщение со стрелками</span><span class="sxs-lookup"><span data-stu-id="d9935-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="d9935-105">Приложение отправляет сообщение **\_ \_ со стрелками СБМ** , чтобы включить или отключить одну или обе стрелки элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="d9935-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9935-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9935-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9935-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9935-108">Указывает, включены ли стрелки полосы прокрутки или отключены, и указывает, какие стрелки включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="d9935-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="d9935-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="d9935-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d9935-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d9935-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="d9935-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d9935-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="d9935-112"><dt>**\_отключение \_ обеих**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="d9935-113">Отключает обе стрелки на полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="d9935-114"><dt>**\_Отключение ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="d9935-115">Отключает стрелку вниз на вертикальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="d9935-116"><dt>**\_лтуп отключение \_ ESB**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="d9935-117">Отключает стрелку влево на горизонтальной полосе прокрутки или на стрелке вверх на вертикальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="d9935-118"><dt>**Отключение ESB, \_ \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="d9935-119">Отключает стрелку влево на горизонтальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="d9935-120"><dt>**\_ртдн отключение \_ ESB**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="d9935-121">Отключает стрелку вправо на горизонтальной полосе прокрутки или на стрелке вниз на вертикальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="d9935-122"><dt>**\_Отключение ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="d9935-123">Отключает стрелку вверх на вертикальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="d9935-124"><dt>**\_Активация ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="d9935-125">Включает обе стрелки на полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d9935-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="d9935-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9935-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9935-127">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="d9935-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9935-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9935-128">Return value</span></span>

<span data-ttu-id="d9935-129">Если сообщение прошло удачно, возвращается значение **true**. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="d9935-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9935-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d9935-130">Requirements</span></span>



| <span data-ttu-id="d9935-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d9935-131">Requirement</span></span> | <span data-ttu-id="d9935-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d9935-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9935-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9935-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d9935-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9935-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9935-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9935-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d9935-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9935-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9935-137">Header</span><span class="sxs-lookup"><span data-stu-id="d9935-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9935-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9935-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





