---
title: Сообщение TBM_CLEARTICS (Коммктрл. h)
description: Удаляет текущие деления из TrackBar. Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Элементы управления Windows для TBM_CLEARTICS сообщений
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489813"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="720f3-105">\_Сообщение ТБМ клеартикс</span><span class="sxs-lookup"><span data-stu-id="720f3-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="720f3-106">Удаляет текущие деления из TrackBar.</span><span class="sxs-lookup"><span data-stu-id="720f3-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="720f3-107">Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.</span><span class="sxs-lookup"><span data-stu-id="720f3-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="720f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="720f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="720f3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="720f3-110">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="720f3-110">Redraw flag.</span></span> <span data-ttu-id="720f3-111">Если этот параметр имеет **значение true**, линейка перерисовывается после очистки делений.</span><span class="sxs-lookup"><span data-stu-id="720f3-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="720f3-112">Если этот параметр имеет **значение false**, сообщение очищает деления, но не перерисовывает TrackBar.</span><span class="sxs-lookup"><span data-stu-id="720f3-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="720f3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="720f3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="720f3-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="720f3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720f3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="720f3-115">Return value</span></span>

<span data-ttu-id="720f3-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="720f3-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="720f3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="720f3-117">Requirements</span></span>



| <span data-ttu-id="720f3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="720f3-118">Requirement</span></span> | <span data-ttu-id="720f3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="720f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="720f3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="720f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="720f3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="720f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="720f3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="720f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="720f3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="720f3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="720f3-124">Header</span><span class="sxs-lookup"><span data-stu-id="720f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="720f3-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="720f3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





