---
title: Код уведомления MCN_VIEWCHANGE (Коммктрл. h)
description: Посылается элементом управления "месячный календарь" при изменении текущего представления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489441"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="2481f-105">\_Код уведомления МКН виевчанже</span><span class="sxs-lookup"><span data-stu-id="2481f-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="2481f-106">Посылается элементом управления "месячный календарь" при изменении текущего представления.</span><span class="sxs-lookup"><span data-stu-id="2481f-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="2481f-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2481f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2481f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2481f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2481f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2481f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2481f-110">Указатель на структуру [**нмвиевчанже**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) , содержащую сведения о текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="2481f-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2481f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2481f-111">Return value</span></span>

<span data-ttu-id="2481f-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2481f-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2481f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2481f-113">Requirements</span></span>



| <span data-ttu-id="2481f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2481f-114">Requirement</span></span> | <span data-ttu-id="2481f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2481f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2481f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2481f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2481f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2481f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2481f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2481f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2481f-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2481f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2481f-120">Header</span><span class="sxs-lookup"><span data-stu-id="2481f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2481f-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2481f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





