---
title: Код уведомления NM_SETCURSOR (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элемент управления устанавливает курсор в ответ на \_ сообщение СЕТКУРСОР WM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- NM_SETCURSOR кода уведомления элементы управления Windows
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
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135583"
---
# <a name="nm_setcursor-notification-code"></a><span data-ttu-id="30be4-105">\_Код уведомления сеткурсор (NM)</span><span class="sxs-lookup"><span data-stu-id="30be4-105">NM\_SETCURSOR notification code</span></span>

<span data-ttu-id="30be4-106">Сообщает родительскому окну элемента управления, что элемент управления устанавливает курсор в ответ на сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="30be4-106">Notifies a control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="30be4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="30be4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="30be4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="30be4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30be4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30be4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30be4-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="30be4-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30be4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30be4-111">Return value</span></span>

<span data-ttu-id="30be4-112">Возвращает ноль, чтобы позволить элементу управления установить курсор или ненулевой нуль, чтобы запретить элементу управления устанавливать курсор.</span><span class="sxs-lookup"><span data-stu-id="30be4-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="30be4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30be4-113">Requirements</span></span>



| <span data-ttu-id="30be4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30be4-114">Requirement</span></span> | <span data-ttu-id="30be4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30be4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30be4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30be4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30be4-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30be4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30be4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30be4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30be4-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30be4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30be4-120">Header</span><span class="sxs-lookup"><span data-stu-id="30be4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="30be4-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="30be4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

