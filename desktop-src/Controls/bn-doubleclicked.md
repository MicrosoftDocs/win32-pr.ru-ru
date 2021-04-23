---
title: Код уведомления BN_DOUBLECLICKED (Winuser. h)
description: Посылается, когда пользователь дважды нажимает кнопку.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891653"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="df4fd-104">\_Код уведомления млрд долл даублекликкед</span><span class="sxs-lookup"><span data-stu-id="df4fd-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="df4fd-105">Посылается, когда пользователь дважды нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="df4fd-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="df4fd-106">Этот код уведомления отправляется автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="df4fd-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="df4fd-107">Другие типы кнопок отправляют млрд долл \_ даублекликкед только в том случае, если они имеют стиль " [**BS \_**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="df4fd-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="df4fd-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="df4fd-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="df4fd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df4fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df4fd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df4fd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df4fd-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="df4fd-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="df4fd-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="df4fd-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="df4fd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df4fd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df4fd-114">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="df4fd-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df4fd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df4fd-115">Remarks</span></span>

<span data-ttu-id="df4fd-116">МЛРД долл \_ даублекликкед совпадает с кодом уведомления [млрд долл \_ дблклк](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="df4fd-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4fd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="df4fd-117">Requirements</span></span>



| <span data-ttu-id="df4fd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="df4fd-118">Requirement</span></span> | <span data-ttu-id="df4fd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="df4fd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4fd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df4fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df4fd-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df4fd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df4fd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df4fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df4fd-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df4fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df4fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="df4fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df4fd-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df4fd-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

