---
title: Сообщение TBM_GETPOS (Коммктрл. h)
description: Извлекает текущее логическое положение ползунка в TrackBar. Логические позиции — это целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- Элементы управления Windows для TBM_GETPOS сообщений
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490698"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="56649-105">\_Сообщение ТБМ жетпос</span><span class="sxs-lookup"><span data-stu-id="56649-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="56649-106">Извлекает текущее логическое положение ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="56649-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="56649-107">Логические позиции — это целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.</span><span class="sxs-lookup"><span data-stu-id="56649-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="56649-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56649-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56649-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56649-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="56649-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="56649-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="56649-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56649-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="56649-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="56649-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56649-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56649-113">Return value</span></span>

<span data-ttu-id="56649-114">Возвращает 32-разрядное значение, указывающее текущую логическую точку ползунка TrackBar.</span><span class="sxs-lookup"><span data-stu-id="56649-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="56649-115">Требования</span><span class="sxs-lookup"><span data-stu-id="56649-115">Requirements</span></span>



| <span data-ttu-id="56649-116">Требование</span><span class="sxs-lookup"><span data-stu-id="56649-116">Requirement</span></span> | <span data-ttu-id="56649-117">Значение</span><span class="sxs-lookup"><span data-stu-id="56649-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56649-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56649-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56649-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56649-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56649-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56649-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56649-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56649-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56649-122">Header</span><span class="sxs-lookup"><span data-stu-id="56649-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56649-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="56649-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56649-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56649-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56649-125">**ТБМ \_ сетпос**</span><span class="sxs-lookup"><span data-stu-id="56649-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





