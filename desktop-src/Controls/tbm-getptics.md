---
title: Сообщение TBM_GETPTICS (Коммктрл. h)
description: Извлекает адрес массива, содержащего позиции делений для TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Элементы управления Windows для TBM_GETPTICS сообщений
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988688"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="bd9c5-104">\_Сообщение ТБМ жетптикс</span><span class="sxs-lookup"><span data-stu-id="bd9c5-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="bd9c5-105">Извлекает адрес массива, содержащего позиции делений для TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd9c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd9c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd9c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd9c5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd9c5-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd9c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd9c5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd9c5-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd9c5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd9c5-111">Return value</span></span>

<span data-ttu-id="bd9c5-112">Возвращает адрес массива значений **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="bd9c5-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="bd9c5-113">Элементы массива задают логические позиции делений TrackBar, не включая первый и последний деления, созданные с помощью TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="bd9c5-114">Логическими позициями может быть любое из целочисленных значений в диапазоне от минимума до максимальных позиций ползунка.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd9c5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd9c5-115">Remarks</span></span>

<span data-ttu-id="bd9c5-116">Число элементов в массиве меньше, чем число тактов, возвращенное сообщением [**ТБМ \_ жетнумтикс**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="bd9c5-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="bd9c5-117">Обратите внимание, что значения в массиве могут включать в себя дубликаты позиций и могут не находиться в последовательном порядке.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="bd9c5-118">Возвращаемый указатель действителен до тех пор, пока не будут изменены деления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bd9c5-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9c5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bd9c5-119">Requirements</span></span>



| <span data-ttu-id="bd9c5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bd9c5-120">Requirement</span></span> | <span data-ttu-id="bd9c5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bd9c5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9c5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd9c5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd9c5-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd9c5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd9c5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd9c5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd9c5-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd9c5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd9c5-126">Header</span><span class="sxs-lookup"><span data-stu-id="bd9c5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd9c5-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd9c5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





