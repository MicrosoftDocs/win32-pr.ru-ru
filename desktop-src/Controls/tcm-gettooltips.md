---
title: Сообщение TCM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip, связанного с элементом управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Элементы управления Windows для TCM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137270"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="36ce6-105">\_Сообщение о подсказках TCM</span><span class="sxs-lookup"><span data-stu-id="36ce6-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="36ce6-106">Получает маркер для элемента управления ToolTip, связанного с элементом управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="36ce6-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="36ce6-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="36ce6-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36ce6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36ce6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ce6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36ce6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36ce6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="36ce6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="36ce6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36ce6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36ce6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="36ce6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ce6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36ce6-113">Return value</span></span>

<span data-ttu-id="36ce6-114">Возвращает маркер для элемента управления ToolTip, если он успешно, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36ce6-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ce6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36ce6-115">Remarks</span></span>

<span data-ttu-id="36ce6-116">Элемент управления "Вкладка" создает элемент управления ToolTip, если он имеет стиль [**\_ подсказок TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="36ce6-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="36ce6-117">Элемент управления ToolTip можно также назначить элементу управления "Вкладка" с помощью сообщения [**TCM \_ сеттултипс**](tcm-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="36ce6-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ce6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="36ce6-118">Requirements</span></span>



| <span data-ttu-id="36ce6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="36ce6-119">Requirement</span></span> | <span data-ttu-id="36ce6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="36ce6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36ce6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36ce6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36ce6-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36ce6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36ce6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36ce6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36ce6-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36ce6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36ce6-125">Header</span><span class="sxs-lookup"><span data-stu-id="36ce6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ce6-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ce6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





