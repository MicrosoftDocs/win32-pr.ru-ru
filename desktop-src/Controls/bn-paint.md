---
title: Код уведомления BN_PAINT (Winuser. h)
description: Посылается, когда кнопка должна быть окрашена.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071130"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="b1000-104">\_Код уведомления млрд долл Paint</span><span class="sxs-lookup"><span data-stu-id="b1000-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="b1000-105">Посылается, когда кнопка должна быть окрашена.</span><span class="sxs-lookup"><span data-stu-id="b1000-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="b1000-106">Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0.</span><span class="sxs-lookup"><span data-stu-id="b1000-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="b1000-107">Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="b1000-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="b1000-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b1000-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b1000-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1000-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1000-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1000-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1000-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="b1000-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="b1000-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="b1000-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b1000-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1000-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1000-114">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="b1000-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1000-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b1000-115">Requirements</span></span>



| <span data-ttu-id="b1000-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b1000-116">Requirement</span></span> | <span data-ttu-id="b1000-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b1000-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1000-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1000-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1000-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1000-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1000-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1000-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1000-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1000-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1000-122">Header</span><span class="sxs-lookup"><span data-stu-id="b1000-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1000-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1000-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

