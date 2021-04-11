---
title: Сообщение TBM_SETTIC (Коммктрл. h)
description: Задает деление на значение TrackBar в указанной логической позиции.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Элементы управления Windows для TBM_SETTIC сообщений
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135455"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="d9615-104">ТБМ \_ Set Message</span><span class="sxs-lookup"><span data-stu-id="d9615-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="d9615-105">Задает деление на значение TrackBar в указанной логической позиции.</span><span class="sxs-lookup"><span data-stu-id="d9615-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9615-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9615-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9615-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9615-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d9615-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d9615-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d9615-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9615-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9615-110">Расположение деления.</span><span class="sxs-lookup"><span data-stu-id="d9615-110">Position of the tick mark.</span></span> <span data-ttu-id="d9615-111">Этот параметр может быть любым из целочисленных значений в диапазоне от минимума до максимальной позиции ползунка.</span><span class="sxs-lookup"><span data-stu-id="d9615-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9615-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9615-112">Return value</span></span>

<span data-ttu-id="d9615-113">Возвращает **значение true** , если деление имеет значение, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d9615-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9615-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9615-114">Remarks</span></span>

<span data-ttu-id="d9615-115">Значение TrackBar создает собственные первый и последний деления.</span><span class="sxs-lookup"><span data-stu-id="d9615-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="d9615-116">Не используйте это сообщение, чтобы задать первый и последний деления.</span><span class="sxs-lookup"><span data-stu-id="d9615-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9615-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d9615-117">Requirements</span></span>



| <span data-ttu-id="d9615-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d9615-118">Requirement</span></span> | <span data-ttu-id="d9615-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d9615-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9615-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9615-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9615-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9615-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9615-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9615-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9615-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9615-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9615-124">Header</span><span class="sxs-lookup"><span data-stu-id="d9615-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9615-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9615-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9615-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9615-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9615-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d9615-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9615-128">**ТБМ \_ жетптикс**</span><span class="sxs-lookup"><span data-stu-id="d9615-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="d9615-129">**ТБМ \_ жеттик**</span><span class="sxs-lookup"><span data-stu-id="d9615-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





