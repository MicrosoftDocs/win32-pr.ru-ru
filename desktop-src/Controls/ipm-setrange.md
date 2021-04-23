---
title: Сообщение IPM_SETRANGE (Коммктрл. h)
description: Задает допустимый диапазон для указанного поля в элементе управления IP-адреса.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Элементы управления Windows для IPM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071872"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="3fad8-104">\_Сообщение IPM SETRANGE</span><span class="sxs-lookup"><span data-stu-id="3fad8-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="3fad8-105">Задает допустимый диапазон для указанного поля в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3fad8-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fad8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fad8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fad8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fad8-108">Отсчитываемый от нуля индекс поля, к которому будет применен диапазон.</span><span class="sxs-lookup"><span data-stu-id="3fad8-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fad8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fad8-110">Значение **слова** , содержащее нижнюю границу диапазона в байте нижнего порядка и верхнее ограничение в байте высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="3fad8-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="3fad8-111">Оба эти значения являются инклюзивными.</span><span class="sxs-lookup"><span data-stu-id="3fad8-111">Both of these values are inclusive.</span></span> <span data-ttu-id="3fad8-112">Для создания диапазона также можно использовать макрос [**макеипранже**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) .</span><span class="sxs-lookup"><span data-stu-id="3fad8-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fad8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fad8-113">Return value</span></span>

<span data-ttu-id="3fad8-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3fad8-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fad8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fad8-115">Remarks</span></span>

<span data-ttu-id="3fad8-116">Если пользователь вводит значение в поле, находящееся за пределами этого диапазона, элемент управления отправит уведомление [ИПН \_ фиелдчанжед](ipn-fieldchanged.md) с введенным значением.</span><span class="sxs-lookup"><span data-stu-id="3fad8-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="3fad8-117">Если значение по-прежнему находится вне диапазона после отправки уведомления, элемент управления попытается изменить указанное значение на ближайшее ограничение диапазона.</span><span class="sxs-lookup"><span data-stu-id="3fad8-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fad8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3fad8-118">Requirements</span></span>



| <span data-ttu-id="3fad8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3fad8-119">Requirement</span></span> | <span data-ttu-id="3fad8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3fad8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fad8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fad8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3fad8-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fad8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fad8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fad8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3fad8-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fad8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fad8-125">Header</span><span class="sxs-lookup"><span data-stu-id="3fad8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fad8-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fad8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





