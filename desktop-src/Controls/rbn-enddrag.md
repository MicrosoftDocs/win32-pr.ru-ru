---
title: Код уведомления RBN_ENDDRAG (Коммктрл. h)
description: Посылается элементом управления главной панели, когда пользователь перестает перетаскивать полосу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071807"
---
# <a name="rbn_enddrag-notification-code"></a><span data-ttu-id="96d66-105">\_Код уведомления РБН енддраг</span><span class="sxs-lookup"><span data-stu-id="96d66-105">RBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="96d66-106">Посылается элементом управления главной панели, когда пользователь перестает перетаскивать полосу.</span><span class="sxs-lookup"><span data-stu-id="96d66-106">Sent by a rebar control when the user stops dragging a band.</span></span> <span data-ttu-id="96d66-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="96d66-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="96d66-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96d66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96d66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96d66-110">Указатель на структуру [**нмребар**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="96d66-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d66-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96d66-111">Return value</span></span>

<span data-ttu-id="96d66-112">Возвращаемое значение для этого кода уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="96d66-112">The return value for this notification code is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d66-113">Требования</span><span class="sxs-lookup"><span data-stu-id="96d66-113">Requirements</span></span>



| <span data-ttu-id="96d66-114">Требование</span><span class="sxs-lookup"><span data-stu-id="96d66-114">Requirement</span></span> | <span data-ttu-id="96d66-115">Значение</span><span class="sxs-lookup"><span data-stu-id="96d66-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96d66-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96d66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96d66-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96d66-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96d66-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96d66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96d66-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96d66-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96d66-120">Header</span><span class="sxs-lookup"><span data-stu-id="96d66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d66-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d66-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





