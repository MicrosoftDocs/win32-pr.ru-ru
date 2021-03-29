---
title: Сообщение SB_SETPARTS (Коммктрл. h)
description: Задает количество частей в окне состояния и координату правого края каждой части.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Элементы управления Windows для SB_SETPARTS сообщений
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534823"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="8769f-104">\_Сообщение SB сетпартс</span><span class="sxs-lookup"><span data-stu-id="8769f-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="8769f-105">Задает количество частей в окне состояния и координату правого края каждой части.</span><span class="sxs-lookup"><span data-stu-id="8769f-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="8769f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8769f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8769f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8769f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8769f-108">Число устанавливаемых частей (не может быть больше 256).</span><span class="sxs-lookup"><span data-stu-id="8769f-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="8769f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8769f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8769f-110">Указатель на целочисленный массив.</span><span class="sxs-lookup"><span data-stu-id="8769f-110">Pointer to an integer array.</span></span> <span data-ttu-id="8769f-111">Число элементов указывается в параметре *wParam*.</span><span class="sxs-lookup"><span data-stu-id="8769f-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="8769f-112">Каждый элемент задает расположение в клиентских координатах правого края соответствующей части.</span><span class="sxs-lookup"><span data-stu-id="8769f-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="8769f-113">Если элемент имеет значение-1, правый край соответствующей части расширяется на границу окна.</span><span class="sxs-lookup"><span data-stu-id="8769f-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8769f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8769f-114">Return value</span></span>

<span data-ttu-id="8769f-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8769f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8769f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8769f-116">Requirements</span></span>



| <span data-ttu-id="8769f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8769f-117">Requirement</span></span> | <span data-ttu-id="8769f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8769f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8769f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8769f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8769f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8769f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8769f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8769f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8769f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8769f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8769f-123">Header</span><span class="sxs-lookup"><span data-stu-id="8769f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8769f-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8769f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





