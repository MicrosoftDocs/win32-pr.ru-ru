---
title: Код уведомления CBN_EDITUPDATE (Winuser. h)
description: Посылается, когда часть поля со списком будет отображаться как измененный текст.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137635"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="d8abb-104">\_Код уведомления КБН едитупдате</span><span class="sxs-lookup"><span data-stu-id="d8abb-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="d8abb-105">Посылается, когда часть поля со списком будет отображаться как измененный текст.</span><span class="sxs-lookup"><span data-stu-id="d8abb-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="d8abb-106">Этот код уведомления отправляется после того, как элемент управления отформатирует текст, но перед отображением текста.</span><span class="sxs-lookup"><span data-stu-id="d8abb-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="d8abb-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d8abb-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d8abb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8abb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8abb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8abb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8abb-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="d8abb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d8abb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="d8abb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d8abb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8abb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8abb-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="d8abb-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8abb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8abb-114">Remarks</span></span>

<span data-ttu-id="d8abb-115">Если поле со списком имеет стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) , этот код уведомления не отправляется.</span><span class="sxs-lookup"><span data-stu-id="d8abb-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8abb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d8abb-116">Requirements</span></span>



| <span data-ttu-id="d8abb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d8abb-117">Requirement</span></span> | <span data-ttu-id="d8abb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d8abb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8abb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8abb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8abb-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8abb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8abb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8abb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8abb-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8abb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d8abb-123">Header</span><span class="sxs-lookup"><span data-stu-id="d8abb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8abb-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8abb-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8abb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8abb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8abb-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d8abb-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8abb-127">КБН \_ едитчанже</span><span class="sxs-lookup"><span data-stu-id="d8abb-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="d8abb-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="d8abb-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d8abb-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8abb-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d8abb-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8abb-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d8abb-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="d8abb-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

