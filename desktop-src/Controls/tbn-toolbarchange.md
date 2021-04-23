---
title: Код уведомления TBN_TOOLBARCHANGE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь настроил панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- TBN_TOOLBARCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989059"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="533bf-105">\_Код уведомления ТБН тулбарчанже</span><span class="sxs-lookup"><span data-stu-id="533bf-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="533bf-106">Сообщает родительскому окну панели инструментов, что пользователь настроил панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="533bf-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="533bf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="533bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="533bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="533bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="533bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="533bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="533bf-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="533bf-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="533bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="533bf-111">Return value</span></span>

<span data-ttu-id="533bf-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="533bf-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="533bf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="533bf-113">Requirements</span></span>



| <span data-ttu-id="533bf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="533bf-114">Requirement</span></span> | <span data-ttu-id="533bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="533bf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="533bf-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="533bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="533bf-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="533bf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="533bf-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="533bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="533bf-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="533bf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="533bf-120">Header</span><span class="sxs-lookup"><span data-stu-id="533bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="533bf-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="533bf-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





