---
title: Код уведомления SBN_SIMPLEMODECHANGE (Коммктрл. h)
description: Посылается элементом управления "строка состояния" при изменении простого режима из-за \_ простого сообщения SB. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654602"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="7e870-105">\_Код уведомления СБН симплемодечанже</span><span class="sxs-lookup"><span data-stu-id="7e870-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="7e870-106">Посылается элементом управления "строка состояния" при изменении простого режима из-за [**\_ простого сообщения SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="7e870-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="7e870-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7e870-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7e870-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e870-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e870-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e870-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e870-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="7e870-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e870-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e870-111">Return value</span></span>

<span data-ttu-id="7e870-112">Возвращаемое значение игнорируется в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="7e870-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e870-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7e870-113">Requirements</span></span>



| <span data-ttu-id="7e870-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7e870-114">Requirement</span></span> | <span data-ttu-id="7e870-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7e870-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e870-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e870-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e870-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e870-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e870-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e870-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e870-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e870-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e870-120">Header</span><span class="sxs-lookup"><span data-stu-id="7e870-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e870-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e870-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





