---
title: Сообщение TBM_GETTIC (Коммктрл. h)
description: Извлекает логическую точку деления в TrackBar. Логическое положение может быть любым из целочисленных значений в диапазоне от минимума до максимальной позиции ползунка.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Элементы управления Windows для TBM_GETTIC сообщений
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490689"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="c0be7-105">\_Сообщение ТБМ жеттик</span><span class="sxs-lookup"><span data-stu-id="c0be7-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="c0be7-106">Извлекает логическую точку деления в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c0be7-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="c0be7-107">Логическое положение может быть любым из целочисленных значений в диапазоне от минимума до максимальной позиции ползунка.</span><span class="sxs-lookup"><span data-stu-id="c0be7-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0be7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0be7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0be7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0be7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0be7-110">Отсчитываемый от нуля индекс, указывающий деление.</span><span class="sxs-lookup"><span data-stu-id="c0be7-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="c0be7-111">Допустимые индексы находятся в диапазоне от нуля до двух меньше, чем число тактов, возвращенное сообщением [**ТБМ \_ жетнумтикс**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="c0be7-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c0be7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0be7-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0be7-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c0be7-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0be7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0be7-114">Return value</span></span>

<span data-ttu-id="c0be7-115">Возвращает логическую точку указанного деления или-1, если параметр *wParam* не указывает допустимый индекс.</span><span class="sxs-lookup"><span data-stu-id="c0be7-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0be7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0be7-116">Requirements</span></span>



| <span data-ttu-id="c0be7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0be7-117">Requirement</span></span> | <span data-ttu-id="c0be7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0be7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0be7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0be7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0be7-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0be7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0be7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0be7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0be7-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0be7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0be7-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0be7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0be7-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0be7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





