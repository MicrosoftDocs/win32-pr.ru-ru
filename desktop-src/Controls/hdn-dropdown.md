---
title: Код уведомления HDN_DROPDOWN (Коммктрл. h)
description: Посылается элементом управления "заголовок" родительскому элементу при щелчке стрелки раскрывающегося списка в элементе управления "заголовок". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892841"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="34948-105">\_Код уведомления раскрывающегося списка ХДН</span><span class="sxs-lookup"><span data-stu-id="34948-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="34948-106">Посылается элементом управления "заголовок" родительскому элементу при щелчке стрелки раскрывающегося списка в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="34948-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="34948-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="34948-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="34948-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34948-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34948-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34948-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34948-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="34948-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34948-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34948-111">Return value</span></span>

<span data-ttu-id="34948-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="34948-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34948-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34948-113">Remarks</span></span>

<span data-ttu-id="34948-114">Пример в разделе синтаксиса показывает, как получатель уведомлений применяет **lParam** для получения структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="34948-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="34948-115">**WParam** содержит идентификатор элемента управления, который отправляет это сообщение.</span><span class="sxs-lookup"><span data-stu-id="34948-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="34948-116">Это сообщение отправляется, только если \_ для элемента заголовка задан стиль ХДФ SPLITBUTTON.</span><span class="sxs-lookup"><span data-stu-id="34948-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="34948-117">Требования</span><span class="sxs-lookup"><span data-stu-id="34948-117">Requirements</span></span>



| <span data-ttu-id="34948-118">Требование</span><span class="sxs-lookup"><span data-stu-id="34948-118">Requirement</span></span> | <span data-ttu-id="34948-119">Значение</span><span class="sxs-lookup"><span data-stu-id="34948-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34948-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34948-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34948-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34948-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34948-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34948-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34948-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34948-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34948-124">Header</span><span class="sxs-lookup"><span data-stu-id="34948-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34948-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="34948-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





