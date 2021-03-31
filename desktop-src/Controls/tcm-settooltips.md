---
title: Сообщение TCM_SETTOOLTIPS (Коммктрл. h)
description: Назначает элемент управления ToolTip элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеттултипс.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Элементы управления Windows для TCM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801054"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="2e64b-105">\_Сообщение СЕТТУЛТИПС TCM</span><span class="sxs-lookup"><span data-stu-id="2e64b-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="2e64b-106">Назначает элемент управления ToolTip элементу управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="2e64b-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="2e64b-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сеттултипс**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="2e64b-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e64b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e64b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e64b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e64b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e64b-110">Обработчик для элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="2e64b-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="2e64b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e64b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e64b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2e64b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e64b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e64b-113">Return value</span></span>

<span data-ttu-id="2e64b-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2e64b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e64b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e64b-115">Remarks</span></span>

<span data-ttu-id="2e64b-116">Элемент управления ToolTip, связанный с элементом управления "Вкладка", можно получить с помощью сообщения [**TCM- \_ ToolTips**](tcm-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="2e64b-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e64b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2e64b-117">Requirements</span></span>



| <span data-ttu-id="2e64b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2e64b-118">Requirement</span></span> | <span data-ttu-id="2e64b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2e64b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e64b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e64b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e64b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e64b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e64b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e64b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e64b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e64b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e64b-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e64b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e64b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e64b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





