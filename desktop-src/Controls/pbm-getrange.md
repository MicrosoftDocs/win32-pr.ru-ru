---
title: Сообщение PBM_GETRANGE (Коммктрл. h)
description: Извлекает сведения о текущих высоких и младших ограничениях данного элемента управления "индикатор выполнения".
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Элементы управления Windows для PBM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989001"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="1ec9c-104">Сообщение о некотором \_ диапазоне PBM</span><span class="sxs-lookup"><span data-stu-id="1ec9c-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="1ec9c-105">Извлекает сведения о текущих высоких и младших ограничениях данного элемента управления "индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="1ec9c-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ec9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ec9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec9c-108">Значение флага, указывающее, какое предельное значение должно использоваться в качестве возвращаемого значения сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="1ec9c-109">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1ec9c-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="1ec9c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec9c-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="1ec9c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec9c-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="1ec9c-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9c-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="1ec9c-113">Возврат нижнего предела.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="1ec9c-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9c-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="1ec9c-115">Возврат верхнего предела.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ec9c-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec9c-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec9c-117">Указатель на структуру [**пбранже**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) , которая должна быть заполнена верхними и низкими границами элемента управления "индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="1ec9c-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="1ec9c-118">Если этот параметр имеет значение **null**, элемент управления возвратит только ограничение, заданное параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec9c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec9c-119">Return value</span></span>

<span data-ttu-id="1ec9c-120">Возвращает значение типа INT, представляющее ограничение, заданное параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="1ec9c-121">Если параметр *lParam* не равен **null**, то параметр *lParam* должен указывать на структуру [**пбранже**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) , которая должна быть заполнена обоими значениями предельного значения.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec9c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec9c-122">Requirements</span></span>



| <span data-ttu-id="1ec9c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec9c-123">Requirement</span></span> | <span data-ttu-id="1ec9c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec9c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec9c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec9c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec9c-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ec9c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ec9c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec9c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec9c-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ec9c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ec9c-129">Header</span><span class="sxs-lookup"><span data-stu-id="1ec9c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec9c-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





