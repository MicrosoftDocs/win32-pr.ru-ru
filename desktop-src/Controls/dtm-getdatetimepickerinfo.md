---
title: Сообщение DTM_GETDATETIMEPICKERINFO (Коммктрл. h)
description: Возвращает сведения об элементе управления "Выбор даты и времени" (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Элементы управления Windows для DTM_GETDATETIMEPICKERINFO сообщений
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489297"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="6348e-104">\_Сообщение DTM жетдатетимепиккеринфо</span><span class="sxs-lookup"><span data-stu-id="6348e-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="6348e-105">Возвращает сведения об элементе управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="6348e-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6348e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6348e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6348e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6348e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6348e-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6348e-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6348e-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6348e-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="6348e-110">Указатель на <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**датетимепиккеринфо**</a> для получения информации.</span><span class="sxs-lookup"><span data-stu-id="6348e-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="6348e-111">Вызывающий объект отвечает за выделение памяти для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="6348e-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="6348e-112">Перед отправкой этого сообщения установите для элемента **кбсизе** структуры значение sizeof (датетимепиккеринфо).</span><span class="sxs-lookup"><span data-stu-id="6348e-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6348e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6348e-113">Return value</span></span>

<span data-ttu-id="6348e-114">Возвращаемое значение не учитывается.</span><span class="sxs-lookup"><span data-stu-id="6348e-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6348e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6348e-115">Requirements</span></span>



| <span data-ttu-id="6348e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6348e-116">Requirement</span></span> | <span data-ttu-id="6348e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6348e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6348e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6348e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6348e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6348e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6348e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6348e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6348e-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6348e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6348e-122">Header</span><span class="sxs-lookup"><span data-stu-id="6348e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6348e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6348e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





