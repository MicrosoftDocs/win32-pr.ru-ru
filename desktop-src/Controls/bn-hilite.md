---
title: Код уведомления BN_HILITE (Winuser. h)
description: Посылается, когда пользователь нажимает кнопку.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988376"
---
# <a name="bn_hilite-notification-code"></a><span data-ttu-id="cd1b0-104">\_Код уведомления млрд долл хилите</span><span class="sxs-lookup"><span data-stu-id="cd1b0-104">BN\_HILITE notification code</span></span>

<span data-ttu-id="cd1b0-105">Посылается, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="cd1b0-105">Sent when the user selects a button.</span></span>

> [!Note]  
> <span data-ttu-id="cd1b0-106">Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0.</span><span class="sxs-lookup"><span data-stu-id="cd1b0-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="cd1b0-107">Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="cd1b0-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="cd1b0-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="cd1b0-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cd1b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd1b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd1b0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd1b0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1b0-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="cd1b0-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="cd1b0-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="cd1b0-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd1b0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1b0-114">Маркер для кнопки.</span><span class="sxs-lookup"><span data-stu-id="cd1b0-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd1b0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd1b0-115">Remarks</span></span>

<span data-ttu-id="cd1b0-116">МЛРД долл \_ хилите совпадает с кодом [ \_ отправленного уведомления млрд долл](bn-pushed.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1b0-116">BN\_HILITE is the same as the [BN\_PUSHED](bn-pushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd1b0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cd1b0-117">Requirements</span></span>



| <span data-ttu-id="cd1b0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cd1b0-118">Requirement</span></span> | <span data-ttu-id="cd1b0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cd1b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1b0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd1b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1b0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd1b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd1b0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd1b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1b0-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd1b0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd1b0-124">Header</span><span class="sxs-lookup"><span data-stu-id="cd1b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd1b0-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd1b0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

