---
title: Код уведомления CBEN_DELETEITEM (Коммктрл. h)
description: Отправляется при удалении элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892549"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="9d023-105">\_Код уведомления кбен DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="9d023-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="9d023-106">Отправляется при удалении элемента.</span><span class="sxs-lookup"><span data-stu-id="9d023-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="9d023-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9d023-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9d023-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d023-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d023-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d023-110">Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления и удаленном элементе.</span><span class="sxs-lookup"><span data-stu-id="9d023-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d023-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d023-111">Return value</span></span>

<span data-ttu-id="9d023-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="9d023-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d023-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9d023-113">Requirements</span></span>



| <span data-ttu-id="9d023-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9d023-114">Requirement</span></span> | <span data-ttu-id="9d023-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9d023-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d023-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d023-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d023-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d023-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d023-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d023-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d023-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d023-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d023-120">Header</span><span class="sxs-lookup"><span data-stu-id="9d023-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d023-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d023-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





