---
title: Сообщение PBM_DELTAPOS (Коммктрл. h)
description: Изменяет текущую позицию индикатора выполнения на заданное приращение и перерисовывает линию, чтобы отразить новую позицию.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Элементы управления Windows для PBM_DELTAPOS сообщений
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071815"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="261e2-104">\_Сообщение ДЕЛТАПОС PBM</span><span class="sxs-lookup"><span data-stu-id="261e2-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="261e2-105">Изменяет текущую позицию индикатора выполнения на заданное приращение и перерисовывает линию, чтобы отразить новую позицию.</span><span class="sxs-lookup"><span data-stu-id="261e2-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="261e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="261e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="261e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="261e2-108">Величина, на которую должно быть перемещено расположение.</span><span class="sxs-lookup"><span data-stu-id="261e2-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="261e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="261e2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="261e2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="261e2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="261e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="261e2-111">Return value</span></span>

<span data-ttu-id="261e2-112">Возвращает предыдущее расположение.</span><span class="sxs-lookup"><span data-stu-id="261e2-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="261e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="261e2-113">Remarks</span></span>

<span data-ttu-id="261e2-114">Если приращение приводит к значению, расположенному за пределами диапазона элемента управления, то устанавливается равным ближайшей границе.</span><span class="sxs-lookup"><span data-stu-id="261e2-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="261e2-115">Поведение этого сообщения не определено, если оно отправляется элементу управления с стилем [**\_ области PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="261e2-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="261e2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="261e2-116">Requirements</span></span>



| <span data-ttu-id="261e2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="261e2-117">Requirement</span></span> | <span data-ttu-id="261e2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="261e2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="261e2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="261e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="261e2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="261e2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="261e2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="261e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="261e2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="261e2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="261e2-123">Header</span><span class="sxs-lookup"><span data-stu-id="261e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="261e2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="261e2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





