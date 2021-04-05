---
title: Код уведомления RBN_DELETINGBAND (Коммктрл. h)
description: Посылается элементом управления главной панели, когда удаляется полоса. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988982"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="165ac-105">\_Код уведомления РБН делетингбанд</span><span class="sxs-lookup"><span data-stu-id="165ac-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="165ac-106">Посылается элементом управления главной панели, когда удаляется полоса.</span><span class="sxs-lookup"><span data-stu-id="165ac-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="165ac-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="165ac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="165ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="165ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="165ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="165ac-110">Указатель на структуру [**нмребар**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="165ac-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165ac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="165ac-111">Return value</span></span>

<span data-ttu-id="165ac-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="165ac-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="165ac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="165ac-113">Requirements</span></span>



| <span data-ttu-id="165ac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="165ac-114">Requirement</span></span> | <span data-ttu-id="165ac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="165ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="165ac-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="165ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="165ac-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="165ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="165ac-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="165ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="165ac-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="165ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="165ac-120">Header</span><span class="sxs-lookup"><span data-stu-id="165ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="165ac-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="165ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





