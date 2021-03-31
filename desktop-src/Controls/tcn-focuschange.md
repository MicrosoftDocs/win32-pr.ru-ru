---
title: Код уведомления TCN_FOCUSCHANGE (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что фокус кнопки изменился. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801049"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="1ec7b-105">\_Код уведомления ТКН фокусчанже</span><span class="sxs-lookup"><span data-stu-id="1ec7b-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="1ec7b-106">Сообщает родительскому окну элемента управления вкладки, что фокус кнопки изменился.</span><span class="sxs-lookup"><span data-stu-id="1ec7b-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="1ec7b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1ec7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec7b-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="1ec7b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec7b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec7b-111">Return value</span></span>

<span data-ttu-id="1ec7b-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1ec7b-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec7b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec7b-113">Requirements</span></span>



| <span data-ttu-id="1ec7b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec7b-114">Requirement</span></span> | <span data-ttu-id="1ec7b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec7b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec7b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec7b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec7b-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ec7b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ec7b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec7b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec7b-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ec7b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ec7b-120">Header</span><span class="sxs-lookup"><span data-stu-id="1ec7b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec7b-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec7b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





