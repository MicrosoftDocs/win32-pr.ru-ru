---
title: Код уведомления BCN_DROPDOWN (Winuser. h)
description: Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке. Родительское окно элемента управления получает этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654471"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="a0d30-105">\_Код уведомления для раскрывающегося списка BCN</span><span class="sxs-lookup"><span data-stu-id="a0d30-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="a0d30-106">Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке.</span><span class="sxs-lookup"><span data-stu-id="a0d30-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="a0d30-107">Родительское окно элемента управления получает этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a0d30-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a0d30-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0d30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0d30-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0d30-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0d30-110">Указатель на структуру [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="a0d30-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="a0d30-111">Для элемента **ркбуттон** задано описание раскрывающегося области.</span><span class="sxs-lookup"><span data-stu-id="a0d30-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0d30-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0d30-112">Return value</span></span>

<span data-ttu-id="a0d30-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a0d30-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d30-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0d30-114">Remarks</span></span>

<span data-ttu-id="a0d30-115">Получатель уведомлений выполняет приведение **lParam** для получения структуры [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="a0d30-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="a0d30-116">**WParam** содержит идентификатор элемента управления, который отправляет это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a0d30-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="a0d30-117">Элемент управления "Кнопка" должен иметь стиль кнопки раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a0d30-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d30-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a0d30-118">Requirements</span></span>



| <span data-ttu-id="a0d30-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a0d30-119">Requirement</span></span> | <span data-ttu-id="a0d30-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a0d30-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d30-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0d30-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d30-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0d30-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0d30-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0d30-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d30-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0d30-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0d30-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0d30-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0d30-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0d30-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





