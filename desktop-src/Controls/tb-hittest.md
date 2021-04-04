---
title: Сообщение TB_HITTEST (Коммктрл. h)
description: Определяет, где находится точка в элементе управления ToolBar.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Элементы управления Windows для TB_HITTEST сообщений
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988474"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="d4830-104">\_Сообщение HITTEST ТБ</span><span class="sxs-lookup"><span data-stu-id="d4830-104">TB\_HITTEST message</span></span>

<span data-ttu-id="d4830-105">Определяет, где находится точка в элементе управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="d4830-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4830-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4830-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4830-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4830-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d4830-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4830-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4830-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4830-110">Указатель на структуру [**Point**](/previous-versions//dd162805(v=vs.85)) , которая содержит координату x проверки попадания в элементе **x** и координату y проверки попадания в элементе **y** .</span><span class="sxs-lookup"><span data-stu-id="d4830-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="d4830-111">Координаты задаются относительно клиентской области панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="d4830-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4830-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4830-112">Return value</span></span>

<span data-ttu-id="d4830-113">Возвращает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="d4830-113">Returns an integer value.</span></span> <span data-ttu-id="d4830-114">Если возвращаемое значение равно нулю или положительному значению, то это Отсчитываемый от нуля индекс неразделителя элемента, в котором находится точка.</span><span class="sxs-lookup"><span data-stu-id="d4830-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="d4830-115">Если возвращаемое значение отрицательное, точка не находится внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="d4830-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="d4830-116">Абсолютное значение возвращаемого значения — это индекс элемента-разделителя или ближайший неразделительный элемент.</span><span class="sxs-lookup"><span data-stu-id="d4830-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4830-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d4830-117">Requirements</span></span>



| <span data-ttu-id="d4830-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d4830-118">Requirement</span></span> | <span data-ttu-id="d4830-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d4830-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4830-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4830-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4830-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4830-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4830-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4830-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4830-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4830-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4830-124">Header</span><span class="sxs-lookup"><span data-stu-id="d4830-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4830-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4830-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

