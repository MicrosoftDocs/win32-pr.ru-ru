---
title: Код уведомления NM_RETURN (представление списка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- Элементы управления Windows для кода уведомления NM_RETURN (представление списка)
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989079"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="c0ed2-105">\_Код уведомления "NM return" (представление списка)</span><span class="sxs-lookup"><span data-stu-id="c0ed2-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="c0ed2-106">Сообщает родительскому окну элемента управления "представление списка", что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c0ed2-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="c0ed2-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ed2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c0ed2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0ed2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ed2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0ed2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ed2-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="c0ed2-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ed2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0ed2-111">Return value</span></span>

<span data-ttu-id="c0ed2-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="c0ed2-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ed2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c0ed2-113">Requirements</span></span>



| <span data-ttu-id="c0ed2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c0ed2-114">Requirement</span></span> | <span data-ttu-id="c0ed2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c0ed2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ed2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0ed2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ed2-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0ed2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0ed2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0ed2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ed2-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0ed2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0ed2-120">Header</span><span class="sxs-lookup"><span data-stu-id="c0ed2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ed2-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ed2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





