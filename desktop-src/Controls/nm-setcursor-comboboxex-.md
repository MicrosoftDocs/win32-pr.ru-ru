---
title: Код уведомления NM_SETCURSOR (ComboBoxEx) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления ComboBoxEx, что элемент управления устанавливает курсор в ответ на \_ сообщение СЕТКУРСОР WM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- Элементы управления Windows для кода уведомления NM_SETCURSOR (ComboBoxEx)
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803149"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a><span data-ttu-id="f7bae-105">\_Код уведомления NM сеткурсор (ComboBoxEx)</span><span class="sxs-lookup"><span data-stu-id="f7bae-105">NM\_SETCURSOR (ComboBoxEx) notification code</span></span>

<span data-ttu-id="f7bae-106">Сообщает родительскому окну элемента управления ComboBoxEx, что элемент управления устанавливает курсор в ответ на сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="f7bae-106">Notifies a ComboBoxEx control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="f7bae-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f7bae-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f7bae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7bae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7bae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7bae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7bae-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="f7bae-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7bae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7bae-111">Return value</span></span>

<span data-ttu-id="f7bae-112">Возвращает ноль, чтобы позволить элементу управления установить курсор или ненулевой нуль, чтобы запретить элементу управления устанавливать курсор.</span><span class="sxs-lookup"><span data-stu-id="f7bae-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7bae-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f7bae-113">Requirements</span></span>



| <span data-ttu-id="f7bae-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f7bae-114">Requirement</span></span> | <span data-ttu-id="f7bae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f7bae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bae-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7bae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7bae-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7bae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7bae-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7bae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7bae-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7bae-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7bae-120">Header</span><span class="sxs-lookup"><span data-stu-id="f7bae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7bae-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7bae-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

