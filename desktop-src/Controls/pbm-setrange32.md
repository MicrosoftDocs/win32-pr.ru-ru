---
title: Сообщение PBM_SETRANGE32 (Коммктрл. h)
description: Устанавливает минимальное и максимальное значения для индикатора выполнения до 32-битных значений и перерисовывает линию для отражения нового диапазона.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Элементы управления Windows для PBM_SETRANGE32 сообщений
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803047"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="7ef9a-104">\_Сообщение SETRANGE32 PBM</span><span class="sxs-lookup"><span data-stu-id="7ef9a-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="7ef9a-105">Устанавливает минимальное и максимальное значения для индикатора выполнения до 32-битных значений и перерисовывает линию для отражения нового диапазона.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ef9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ef9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ef9a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef9a-108">Минимальное значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-108">Minimum range value.</span></span> <span data-ttu-id="7ef9a-109">По умолчанию минимальное значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ef9a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ef9a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef9a-111">Максимальное значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-111">Maximum range value.</span></span> <span data-ttu-id="7ef9a-112">Это значение должно быть больше, чем *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="7ef9a-113">По умолчанию максимальное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef9a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ef9a-114">Return value</span></span>

<span data-ttu-id="7ef9a-115">Возвращает значение **типа DWORD** , которое содержит предыдущее 16-разрядное нижнее ограничение в его [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и предыдущий 16-разрядный верхний предел в его [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ef9a-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="7ef9a-116">Если предыдущие диапазоны были 32-разрядными, возвращаемое значение состоит из **ловорд** s обоих 32-разрядных ограничений.</span><span class="sxs-lookup"><span data-stu-id="7ef9a-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef9a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ef9a-117">Remarks</span></span>

<span data-ttu-id="7ef9a-118">Чтобы получить все высокие и младшие 32-битные значения, используйте сообщение [**PBM- \_ Range**](pbm-getrange.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef9a-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef9a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7ef9a-119">Requirements</span></span>



| <span data-ttu-id="7ef9a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7ef9a-120">Requirement</span></span> | <span data-ttu-id="7ef9a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7ef9a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef9a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ef9a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef9a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ef9a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ef9a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ef9a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef9a-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ef9a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ef9a-126">Header</span><span class="sxs-lookup"><span data-stu-id="7ef9a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ef9a-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef9a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

