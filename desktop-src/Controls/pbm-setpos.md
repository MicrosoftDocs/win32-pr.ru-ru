---
title: Сообщение PBM_SETPOS (Коммктрл. h)
description: Задает текущую точку для индикатора выполнения и перерисовывает линию для отражения новой должности.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Элементы управления Windows для PBM_SETPOS сообщений
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654579"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="2074d-104">\_Сообщение СЕТПОС PBM</span><span class="sxs-lookup"><span data-stu-id="2074d-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="2074d-105">Задает текущую точку для индикатора выполнения и перерисовывает линию для отражения новой должности.</span><span class="sxs-lookup"><span data-stu-id="2074d-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="2074d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2074d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2074d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2074d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2074d-108">Целое число со знаком, которое станет новой позицией.</span><span class="sxs-lookup"><span data-stu-id="2074d-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="2074d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2074d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2074d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2074d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2074d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2074d-111">Return value</span></span>

<span data-ttu-id="2074d-112">Возвращает предыдущее расположение.</span><span class="sxs-lookup"><span data-stu-id="2074d-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="2074d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2074d-113">Remarks</span></span>

<span data-ttu-id="2074d-114">Если параметр *wParam* находится за пределами диапазона элемента управления, то в качестве расположения устанавливается Ближайшая граница.</span><span class="sxs-lookup"><span data-stu-id="2074d-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="2074d-115">Не отправляйте это сообщение элементу управления с стилем [**\_ области PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2074d-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2074d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2074d-116">Requirements</span></span>



| <span data-ttu-id="2074d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2074d-117">Requirement</span></span> | <span data-ttu-id="2074d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2074d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2074d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2074d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2074d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2074d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2074d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2074d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2074d-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2074d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2074d-123">Header</span><span class="sxs-lookup"><span data-stu-id="2074d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2074d-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2074d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





