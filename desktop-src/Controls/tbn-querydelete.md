---
title: Код уведомления TBN_QUERYDELETE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533746"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="76e61-105">\_Код уведомления ТБН куериделете</span><span class="sxs-lookup"><span data-stu-id="76e61-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="76e61-106">Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="76e61-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="76e61-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="76e61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="76e61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76e61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76e61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76e61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76e61-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="76e61-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="76e61-111">Член **iItem** содержит отсчитываемый от нуля индекс удаляемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="76e61-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76e61-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76e61-112">Return value</span></span>

<span data-ttu-id="76e61-113">Возвращает **значение true** , чтобы разрешить удаление кнопки, или **значение false** , чтобы предотвратить удаление кнопки.</span><span class="sxs-lookup"><span data-stu-id="76e61-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e61-114">Требования</span><span class="sxs-lookup"><span data-stu-id="76e61-114">Requirements</span></span>



| <span data-ttu-id="76e61-115">Требование</span><span class="sxs-lookup"><span data-stu-id="76e61-115">Requirement</span></span> | <span data-ttu-id="76e61-116">Значение</span><span class="sxs-lookup"><span data-stu-id="76e61-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76e61-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76e61-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76e61-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76e61-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76e61-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76e61-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76e61-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76e61-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76e61-121">Header</span><span class="sxs-lookup"><span data-stu-id="76e61-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="76e61-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="76e61-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





