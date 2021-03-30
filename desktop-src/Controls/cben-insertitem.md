---
title: Код уведомления CBEN_INSERTITEM (Коммктрл. h)
description: Посылается при вставке нового элемента в элемент управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804013"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="73659-105">\_Код уведомления кбен INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="73659-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="73659-106">Посылается при вставке нового элемента в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="73659-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="73659-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73659-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="73659-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73659-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73659-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73659-110">Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления и вставленном элементе.</span><span class="sxs-lookup"><span data-stu-id="73659-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73659-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73659-111">Return value</span></span>

<span data-ttu-id="73659-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="73659-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="73659-113">Требования</span><span class="sxs-lookup"><span data-stu-id="73659-113">Requirements</span></span>



| <span data-ttu-id="73659-114">Требование</span><span class="sxs-lookup"><span data-stu-id="73659-114">Requirement</span></span> | <span data-ttu-id="73659-115">Значение</span><span class="sxs-lookup"><span data-stu-id="73659-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73659-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73659-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73659-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73659-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73659-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73659-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73659-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73659-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73659-120">Header</span><span class="sxs-lookup"><span data-stu-id="73659-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73659-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73659-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





