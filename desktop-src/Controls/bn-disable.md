---
title: Код уведомления BN_DISABLE (Winuser. h)
description: Посылается, когда кнопка отключена.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- BN_DISABLE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faaba622c056366fe0c49683adc2c020a6302929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988377"
---
# <a name="bn_disable-notification-code"></a><span data-ttu-id="67b91-104">МЛРД долл \_ Отключить код уведомления</span><span class="sxs-lookup"><span data-stu-id="67b91-104">BN\_DISABLE notification code</span></span>

<span data-ttu-id="67b91-105">Посылается, когда кнопка отключена.</span><span class="sxs-lookup"><span data-stu-id="67b91-105">Sent when a button is disabled.</span></span>

> [!Note]  
> <span data-ttu-id="67b91-106">Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0.</span><span class="sxs-lookup"><span data-stu-id="67b91-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="67b91-107">Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="67b91-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="67b91-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="67b91-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DISABLE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="67b91-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="67b91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b91-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67b91-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67b91-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="67b91-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="67b91-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="67b91-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="67b91-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67b91-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67b91-114">Маркер для кнопки.</span><span class="sxs-lookup"><span data-stu-id="67b91-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67b91-115">Требования</span><span class="sxs-lookup"><span data-stu-id="67b91-115">Requirements</span></span>



| <span data-ttu-id="67b91-116">Требование</span><span class="sxs-lookup"><span data-stu-id="67b91-116">Requirement</span></span> | <span data-ttu-id="67b91-117">Значение</span><span class="sxs-lookup"><span data-stu-id="67b91-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b91-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67b91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67b91-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67b91-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67b91-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67b91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67b91-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67b91-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67b91-122">Header</span><span class="sxs-lookup"><span data-stu-id="67b91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67b91-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67b91-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

