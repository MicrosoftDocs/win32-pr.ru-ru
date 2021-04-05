---
title: Код уведомления TBN_QUERYINSERT (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, можно ли вставить кнопку слева от указанной кнопки, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989288"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="8dd6d-105">\_Код уведомления ТБН куеринсерт</span><span class="sxs-lookup"><span data-stu-id="8dd6d-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="8dd6d-106">Сообщает родительскому окну панели инструментов, можно ли вставить кнопку слева от указанной кнопки, пока пользователь настраивает панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="8dd6d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8dd6d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8dd6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dd6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8dd6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dd6d-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="8dd6d-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="8dd6d-111">Член **iItem** содержит отсчитываемый от нуля индекс вставляемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dd6d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dd6d-112">Return value</span></span>

<span data-ttu-id="8dd6d-113">Возвращает **значение true** , чтобы разрешить вставку кнопки перед заданной кнопкой, или **значение false** , чтобы запретить вставку кнопки.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd6d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8dd6d-114">Requirements</span></span>



| <span data-ttu-id="8dd6d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8dd6d-115">Requirement</span></span> | <span data-ttu-id="8dd6d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8dd6d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd6d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dd6d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd6d-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dd6d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8dd6d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dd6d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd6d-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8dd6d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dd6d-121">Header</span><span class="sxs-lookup"><span data-stu-id="8dd6d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dd6d-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dd6d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





