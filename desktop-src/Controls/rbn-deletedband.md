---
title: Код уведомления RBN_DELETEDBAND (Коммктрл. h)
description: Посылается элементом управления "Главная панель" после удаления полосы. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892269"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="b89c7-105">\_Код уведомления РБН делетедбанд</span><span class="sxs-lookup"><span data-stu-id="b89c7-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="b89c7-106">Посылается элементом управления "Главная панель" после удаления полосы.</span><span class="sxs-lookup"><span data-stu-id="b89c7-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="b89c7-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b89c7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b89c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b89c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b89c7-110">Указатель на структуру [**нмребар**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="b89c7-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89c7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b89c7-111">Return value</span></span>

<span data-ttu-id="b89c7-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="b89c7-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89c7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b89c7-113">Requirements</span></span>



| <span data-ttu-id="b89c7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b89c7-114">Requirement</span></span> | <span data-ttu-id="b89c7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b89c7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b89c7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b89c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b89c7-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b89c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b89c7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b89c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b89c7-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b89c7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b89c7-120">Header</span><span class="sxs-lookup"><span data-stu-id="b89c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b89c7-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89c7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





