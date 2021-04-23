---
title: Код уведомления TBN_HOTITEMCHANGE (Коммктрл. h)
description: Посылается элементом управления ToolBar при изменении элемента "горячий" (выделенный). Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801067"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="cf83d-105">\_Код уведомления ТБН хотитемчанже</span><span class="sxs-lookup"><span data-stu-id="cf83d-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="cf83d-106">Посылается элементом управления ToolBar при изменении элемента "горячий" (выделенный).</span><span class="sxs-lookup"><span data-stu-id="cf83d-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="cf83d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cf83d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cf83d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf83d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf83d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf83d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf83d-110">Указатель на структуру [**нмтбхотитем**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="cf83d-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf83d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf83d-111">Return value</span></span>

<span data-ttu-id="cf83d-112">Возвращает ноль, чтобы разрешить выделение элемента, или ненулевое значение, чтобы предотвратить выделение элемента.</span><span class="sxs-lookup"><span data-stu-id="cf83d-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf83d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cf83d-113">Requirements</span></span>



| <span data-ttu-id="cf83d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cf83d-114">Requirement</span></span> | <span data-ttu-id="cf83d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cf83d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf83d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf83d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf83d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf83d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf83d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf83d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf83d-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf83d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf83d-120">Header</span><span class="sxs-lookup"><span data-stu-id="cf83d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf83d-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf83d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





