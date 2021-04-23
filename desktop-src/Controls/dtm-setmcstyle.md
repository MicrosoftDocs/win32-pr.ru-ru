---
title: Сообщение DTM_SETMCSTYLE (Коммктрл. h)
description: Задает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime сетмонскалстиле.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Элементы управления Windows для DTM_SETMCSTYLE сообщений
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136671"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="75b3b-105">\_Сообщение DTM сетмкстиле</span><span class="sxs-lookup"><span data-stu-id="75b3b-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="75b3b-106">Задает стиль элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="75b3b-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="75b3b-107">Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ сетмонскалстиле**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="75b3b-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="75b3b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75b3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75b3b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75b3b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="75b3b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75b3b-111">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75b3b-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="75b3b-112">Значение стиля.</span><span class="sxs-lookup"><span data-stu-id="75b3b-112">A style value.</span></span> <span data-ttu-id="75b3b-113">Дополнительные сведения см. в разделе <a href="month-calendar-control-styles.md">стили элементов управления календарем месяца</a>.</span><span class="sxs-lookup"><span data-stu-id="75b3b-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b3b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75b3b-114">Return value</span></span>

<span data-ttu-id="75b3b-115">Возвращает значение предыдущего стиля.</span><span class="sxs-lookup"><span data-stu-id="75b3b-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b3b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="75b3b-116">Requirements</span></span>



| <span data-ttu-id="75b3b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="75b3b-117">Requirement</span></span> | <span data-ttu-id="75b3b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="75b3b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75b3b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75b3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75b3b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75b3b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75b3b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75b3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75b3b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75b3b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75b3b-123">Header</span><span class="sxs-lookup"><span data-stu-id="75b3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b3b-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b3b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





