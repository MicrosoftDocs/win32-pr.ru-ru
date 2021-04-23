---
title: Код уведомления IPN_FIELDCHANGED (Коммктрл. h)
description: Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071871"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="ceec9-105">\_Код уведомления ИПН фиелдчанжед</span><span class="sxs-lookup"><span data-stu-id="ceec9-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="ceec9-106">Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое.</span><span class="sxs-lookup"><span data-stu-id="ceec9-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="ceec9-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ceec9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ceec9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceec9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceec9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ceec9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceec9-110">Указатель на структуру [**нмипаддресс**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) , содержащую сведения об измененном адресе.</span><span class="sxs-lookup"><span data-stu-id="ceec9-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="ceec9-111">Элемент **iValue** этой структуры будет содержать указанное значение, даже если оно выходит за пределы диапазона поля.</span><span class="sxs-lookup"><span data-stu-id="ceec9-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="ceec9-112">Этот элемент можно изменить на любое значение в диапазоне для поля в ответ на этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="ceec9-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceec9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceec9-113">Return value</span></span>

<span data-ttu-id="ceec9-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ceec9-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceec9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ceec9-115">Remarks</span></span>

<span data-ttu-id="ceec9-116">Этот код уведомления не отправляется в ответ на сообщение [**IPM \_ сетаддресс**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="ceec9-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceec9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ceec9-117">Requirements</span></span>



| <span data-ttu-id="ceec9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ceec9-118">Requirement</span></span> | <span data-ttu-id="ceec9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ceec9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceec9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ceec9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ceec9-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ceec9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ceec9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ceec9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ceec9-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ceec9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ceec9-124">Header</span><span class="sxs-lookup"><span data-stu-id="ceec9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceec9-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceec9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





