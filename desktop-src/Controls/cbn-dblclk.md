---
title: Код уведомления CBN_DBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды щелкает строку в поле со списком. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654715"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="b8bc3-105">\_Код уведомления КБН дблклк</span><span class="sxs-lookup"><span data-stu-id="b8bc3-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="b8bc3-106">Посылается, когда пользователь дважды щелкает строку в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="b8bc3-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="b8bc3-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b8bc3-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b8bc3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8bc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8bc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8bc3-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="b8bc3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="b8bc3-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="b8bc3-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b8bc3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8bc3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8bc3-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="b8bc3-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8bc3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8bc3-114">Remarks</span></span>

<span data-ttu-id="b8bc3-115">Этот код уведомления имеет место только для полей со списком, [**имеющих \_ простой стиль CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b8bc3-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="b8bc3-116">В поле со списком, имеющем [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) , двойной щелчок не может произойти, поскольку один щелчок закрывает окно списка.</span><span class="sxs-lookup"><span data-stu-id="b8bc3-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bc3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b8bc3-117">Requirements</span></span>



| <span data-ttu-id="b8bc3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b8bc3-118">Requirement</span></span> | <span data-ttu-id="b8bc3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b8bc3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bc3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8bc3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bc3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8bc3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8bc3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8bc3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bc3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8bc3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8bc3-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8bc3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8bc3-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8bc3-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8bc3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8bc3-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8bc3-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b8bc3-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8bc3-128">КБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="b8bc3-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="b8bc3-129">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b8bc3-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b8bc3-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8bc3-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b8bc3-131">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8bc3-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8bc3-132">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="b8bc3-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

