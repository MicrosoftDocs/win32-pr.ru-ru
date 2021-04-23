---
title: Сообщение UDM_GETRANGE (Коммктрл. h)
description: Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Элементы управления Windows для UDM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262229"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="c3034-104">\_Сообщение о ВЫДИАПАЗОНЕ UDM</span><span class="sxs-lookup"><span data-stu-id="c3034-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="c3034-105">Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="c3034-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3034-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3034-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3034-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3034-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3034-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c3034-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3034-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3034-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3034-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c3034-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3034-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3034-111">Return value</span></span>

<span data-ttu-id="c3034-112">Возвращаемое значение — это 32-разрядное значение, которое содержит минимальное и максимальное позиции.</span><span class="sxs-lookup"><span data-stu-id="c3034-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="c3034-113">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является максимальным положением для элемента управления, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — минимальным положением.</span><span class="sxs-lookup"><span data-stu-id="c3034-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3034-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c3034-114">Requirements</span></span>



| <span data-ttu-id="c3034-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c3034-115">Requirement</span></span> | <span data-ttu-id="c3034-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3034-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3034-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3034-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3034-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3034-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3034-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3034-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3034-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3034-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3034-121">Header</span><span class="sxs-lookup"><span data-stu-id="c3034-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3034-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3034-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

