---
title: Сообщение TBM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip, назначенного для TrackBar, если таковой имеется.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Элементы управления Windows для TBM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891953"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="fa742-104">Сообщение ТБМ с \_ ПОДсказками</span><span class="sxs-lookup"><span data-stu-id="fa742-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="fa742-105">Получает маркер для элемента управления ToolTip, назначенного для TrackBar, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="fa742-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa742-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa742-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa742-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa742-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa742-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fa742-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa742-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa742-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa742-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fa742-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa742-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa742-111">Return value</span></span>

<span data-ttu-id="fa742-112">Возвращает маркер для элемента управления ToolTip, назначенного для TrackBar, или **значение NULL** , если подсказки не используются.</span><span class="sxs-lookup"><span data-stu-id="fa742-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="fa742-113">Если элемент управления TrackBar не использует стиль [**\_ подсказок TBS**](trackbar-control-styles.md) , возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fa742-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa742-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fa742-114">Requirements</span></span>



| <span data-ttu-id="fa742-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fa742-115">Requirement</span></span> | <span data-ttu-id="fa742-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fa742-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa742-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa742-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa742-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa742-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa742-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa742-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa742-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa742-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa742-121">Header</span><span class="sxs-lookup"><span data-stu-id="fa742-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa742-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa742-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





