---
title: Код уведомления CBN_DROPDOWN (Winuser. h)
description: Посылается, когда список поля со списком станет видимым. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654553"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="75301-105">\_Код уведомления раскрывающегося списка КБН</span><span class="sxs-lookup"><span data-stu-id="75301-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="75301-106">Посылается, когда список поля со списком станет видимым.</span><span class="sxs-lookup"><span data-stu-id="75301-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="75301-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="75301-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="75301-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75301-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75301-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75301-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="75301-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="75301-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="75301-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="75301-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75301-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75301-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="75301-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75301-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75301-114">Remarks</span></span>

<span data-ttu-id="75301-115">Этот код уведомления отправляется, только если поле со списком имеет [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="75301-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="75301-116">Требования</span><span class="sxs-lookup"><span data-stu-id="75301-116">Requirements</span></span>



| <span data-ttu-id="75301-117">Требование</span><span class="sxs-lookup"><span data-stu-id="75301-117">Requirement</span></span> | <span data-ttu-id="75301-118">Значение</span><span class="sxs-lookup"><span data-stu-id="75301-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75301-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75301-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75301-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75301-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="75301-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75301-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75301-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75301-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75301-123">Header</span><span class="sxs-lookup"><span data-stu-id="75301-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75301-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75301-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75301-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75301-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="75301-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="75301-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75301-127">КБН \_ крупный план</span><span class="sxs-lookup"><span data-stu-id="75301-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="75301-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="75301-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="75301-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75301-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="75301-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75301-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75301-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="75301-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

