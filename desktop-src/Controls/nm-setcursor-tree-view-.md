---
title: Код уведомления NM_SETCURSOR (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления устанавливает курсор в ответ на \_ сообщение СЕТКУРСОР WM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- Элементы управления Windows для кода уведомления NM_SETCURSOR (представление в виде дерева)
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
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989077"
---
# <a name="nm_setcursor-tree-view-notification-code"></a><span data-ttu-id="f2e88-105">\_Код уведомления NM сеткурсор (в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="f2e88-105">NM\_SETCURSOR (tree view) notification code</span></span>

<span data-ttu-id="f2e88-106">Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления устанавливает курсор в ответ на сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="f2e88-106">Notifies a tree-view control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="f2e88-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f2e88-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f2e88-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2e88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2e88-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e88-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="f2e88-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e88-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2e88-111">Return value</span></span>

<span data-ttu-id="f2e88-112">Возвращает ноль, чтобы позволить элементу управления установить курсор или ненулевой нуль, чтобы запретить элементу управления устанавливать курсор.</span><span class="sxs-lookup"><span data-stu-id="f2e88-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e88-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f2e88-113">Requirements</span></span>



| <span data-ttu-id="f2e88-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f2e88-114">Requirement</span></span> | <span data-ttu-id="f2e88-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e88-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e88-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2e88-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e88-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2e88-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2e88-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2e88-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e88-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2e88-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2e88-120">Header</span><span class="sxs-lookup"><span data-stu-id="f2e88-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e88-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e88-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

