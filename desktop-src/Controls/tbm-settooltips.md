---
title: Сообщение TBM_SETTOOLTIPS (Коммктрл. h)
description: Назначает элемент управления ToolTip элементу управления TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- Элементы управления Windows для TBM_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489801"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="f9072-104">\_Сообщение ТБМ сеттултипс</span><span class="sxs-lookup"><span data-stu-id="f9072-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="f9072-105">Назначает элемент управления ToolTip элементу управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f9072-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9072-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9072-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9072-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9072-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9072-108">Обработчик существующего элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f9072-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="f9072-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9072-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f9072-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f9072-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9072-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9072-111">Return value</span></span>

<span data-ttu-id="f9072-112">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="f9072-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9072-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9072-113">Remarks</span></span>

<span data-ttu-id="f9072-114">При создании элемента управления TrackBar с помощью стиля [**\_ всплывающих подсказок TBS**](trackbar-control-styles.md) создается элемент управления ToolTip по умолчанию, который отображается рядом с ползунком, отображая текущую положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="f9072-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9072-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f9072-115">Requirements</span></span>



| <span data-ttu-id="f9072-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f9072-116">Requirement</span></span> | <span data-ttu-id="f9072-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f9072-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9072-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9072-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9072-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9072-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9072-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9072-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9072-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9072-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9072-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9072-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9072-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





