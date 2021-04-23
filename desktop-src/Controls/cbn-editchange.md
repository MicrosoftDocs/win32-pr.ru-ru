---
title: Код уведомления CBN_EDITCHANGE (Winuser. h)
description: Посылается после того, как пользователь выполнит действие, которое могло изменить текст в элементе управления поля со списком.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654706"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="c3c2d-104">\_Код уведомления КБН едитчанже</span><span class="sxs-lookup"><span data-stu-id="c3c2d-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="c3c2d-105">Посылается после того, как пользователь выполнит действие, которое могло изменить текст в элементе управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="c3c2d-106">В отличие от кода уведомления [КБН \_ едитупдате](cbn-editupdate.md) , этот код уведомления отправляется после того, как система обновляет экран.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="c3c2d-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c3c2d-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c3c2d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3c2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3c2d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3c2d-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="c3c2d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3c2d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3c2d-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3c2d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3c2d-114">Remarks</span></span>

<span data-ttu-id="c3c2d-115">Если поле со списком имеет стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) , этот код уведомления не отправляется.</span><span class="sxs-lookup"><span data-stu-id="c3c2d-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c2d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c3c2d-116">Requirements</span></span>



| <span data-ttu-id="c3c2d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c3c2d-117">Requirement</span></span> | <span data-ttu-id="c3c2d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c2d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c2d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3c2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c2d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3c2d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c3c2d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3c2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c2d-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3c2d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c3c2d-123">Header</span><span class="sxs-lookup"><span data-stu-id="c3c2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c2d-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3c2d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c2d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3c2d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3c2d-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c3c2d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3c2d-127">КБН \_ едитупдате</span><span class="sxs-lookup"><span data-stu-id="c3c2d-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="c3c2d-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c3c2d-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c3c2d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3c2d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c3c2d-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3c2d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c3c2d-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="c3c2d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

