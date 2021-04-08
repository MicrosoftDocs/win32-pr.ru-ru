---
title: Код уведомления RBN_CHILDSIZE (Коммктрл. h)
description: Посылается элементом управления главной панели при изменении размера дочернего окна полосы. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892141"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="4d78d-105">\_Код уведомления РБН чилдсизе</span><span class="sxs-lookup"><span data-stu-id="4d78d-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="4d78d-106">Посылается элементом управления главной панели при изменении размера дочернего окна полосы.</span><span class="sxs-lookup"><span data-stu-id="4d78d-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="4d78d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4d78d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4d78d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d78d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d78d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d78d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d78d-110">Указатель на структуру [**нмребарчилдсизе**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="4d78d-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d78d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d78d-111">Return value</span></span>

<span data-ttu-id="4d78d-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="4d78d-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d78d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4d78d-113">Requirements</span></span>



| <span data-ttu-id="4d78d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4d78d-114">Requirement</span></span> | <span data-ttu-id="4d78d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4d78d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d78d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d78d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4d78d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d78d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d78d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d78d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4d78d-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d78d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d78d-120">Header</span><span class="sxs-lookup"><span data-stu-id="4d78d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d78d-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d78d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





