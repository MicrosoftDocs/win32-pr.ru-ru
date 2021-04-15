---
title: Сообщение PGM_FORWARDMOUSE (Коммктрл. h)
description: Включает или отключает пересылку указателя мыши для элемента управления страничного навигатора. Если пересылка указателя мыши включена, элемент управления страничного навигатора пересылает \_ сообщения WM MOUSEMOVE в автономное окно. Это сообщение можно отправить явным образом или использовать \_ макрос Форвардмаусе пейджера.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Элементы управления Windows для PGM_FORWARDMOUSE сообщений
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654575"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="fa2a0-106">\_Сообщение ФОРВАРДМАУСЕ PGM</span><span class="sxs-lookup"><span data-stu-id="fa2a0-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="fa2a0-107">Включает или отключает пересылку указателя мыши для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="fa2a0-108">Если пересылка указателя мыши включена, элемент управления страничного навигатора пересылает сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) в автономное окно.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="fa2a0-109">Это сообщение можно отправить явным образом или использовать макрос [**\_ форвардмаусе пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .</span><span class="sxs-lookup"><span data-stu-id="fa2a0-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa2a0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa2a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa2a0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa2a0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa2a0-112">**Логическое** значение, которое определяет, включена или отключена переадресация мыши.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="fa2a0-113">Если это значение не равно нулю, пересылка указателя мыши включена.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="fa2a0-114">Если это значение равно нулю, пересылка указателя мыши отключена.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="fa2a0-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa2a0-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa2a0-116">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa2a0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa2a0-117">Return value</span></span>

<span data-ttu-id="fa2a0-118">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="fa2a0-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2a0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fa2a0-119">Requirements</span></span>



| <span data-ttu-id="fa2a0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fa2a0-120">Requirement</span></span> | <span data-ttu-id="fa2a0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fa2a0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2a0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa2a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2a0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa2a0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa2a0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa2a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2a0-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa2a0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa2a0-126">Header</span><span class="sxs-lookup"><span data-stu-id="fa2a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2a0-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2a0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

