---
title: Сообщение TDM_SET_PROGRESS_BAR_RANGE (Коммктрл. h)
description: Задает минимальное и максимальное значения индикатора выполнения в диалоговом окне задачи.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_RANGE сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892717"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="f9e95-104">TDM \_ задать \_ \_ \_ сообщение диапазона индикатора выполнения</span><span class="sxs-lookup"><span data-stu-id="f9e95-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="f9e95-105">Задает минимальное и максимальное значения индикатора выполнения в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="f9e95-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9e95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e95-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9e95-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e95-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f9e95-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9e95-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9e95-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e95-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="f9e95-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="f9e95-111">По умолчанию минимальное значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f9e95-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="f9e95-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="f9e95-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="f9e95-113">По умолчанию максимальное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="f9e95-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e95-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9e95-114">Return value</span></span>

<span data-ttu-id="f9e95-115">Возвращает предыдущие минимальные и максимальные значения, если они успешно, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f9e95-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="f9e95-116">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит минимальное значение, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="f9e95-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e95-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f9e95-117">Requirements</span></span>



| <span data-ttu-id="f9e95-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f9e95-118">Requirement</span></span> | <span data-ttu-id="f9e95-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f9e95-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e95-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9e95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e95-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9e95-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9e95-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9e95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e95-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9e95-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9e95-124">Header</span><span class="sxs-lookup"><span data-stu-id="f9e95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e95-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e95-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

