---
title: Код уведомления BN_PUSHED (Winuser. h)
description: Посылается, когда для кнопки задано состояние pushd.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340505"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="81f40-104">МЛРД долл \_ отправленный код уведомления</span><span class="sxs-lookup"><span data-stu-id="81f40-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="81f40-105">Посылается, когда для кнопки задано состояние pushd.</span><span class="sxs-lookup"><span data-stu-id="81f40-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="81f40-106">Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0.</span><span class="sxs-lookup"><span data-stu-id="81f40-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="81f40-107">Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="81f40-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="81f40-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="81f40-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="81f40-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="81f40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f40-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81f40-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f40-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="81f40-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="81f40-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="81f40-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="81f40-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81f40-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f40-114">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="81f40-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81f40-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81f40-115">Remarks</span></span>

<span data-ttu-id="81f40-116">\_Отправленный млрд долл совпадает с кодом уведомления [ \_ хилите млрд долл](bn-hilite.md) .</span><span class="sxs-lookup"><span data-stu-id="81f40-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f40-117">Требования</span><span class="sxs-lookup"><span data-stu-id="81f40-117">Requirements</span></span>



| <span data-ttu-id="81f40-118">Требование</span><span class="sxs-lookup"><span data-stu-id="81f40-118">Requirement</span></span> | <span data-ttu-id="81f40-119">Значение</span><span class="sxs-lookup"><span data-stu-id="81f40-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f40-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81f40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81f40-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81f40-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81f40-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81f40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81f40-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81f40-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81f40-124">Header</span><span class="sxs-lookup"><span data-stu-id="81f40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f40-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81f40-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f40-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81f40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f40-127">**МЛРД долл не отправлено \_**</span><span class="sxs-lookup"><span data-stu-id="81f40-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 

