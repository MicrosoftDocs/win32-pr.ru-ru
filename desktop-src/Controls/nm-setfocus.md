---
title: Код уведомления NM_SETFOCUS (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элемент управления получил фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4810afd3-c8a8-4813-b44a-eba3d409d4f1
keywords:
- NM_SETFOCUS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3d50596f39359fe2aeeeb4fe61b8bc73603efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989006"
---
# <a name="nm_setfocus-notification-code"></a><span data-ttu-id="d6b93-105">\_Код уведомления "NM SETFOCUS"</span><span class="sxs-lookup"><span data-stu-id="d6b93-105">NM\_SETFOCUS notification code</span></span>

<span data-ttu-id="d6b93-106">Сообщает родительскому окну элемента управления, что элемент управления получил фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="d6b93-106">Notifies a control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="d6b93-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b93-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d6b93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6b93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b93-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6b93-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b93-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="d6b93-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b93-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6b93-111">Return value</span></span>

<span data-ttu-id="d6b93-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d6b93-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b93-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d6b93-113">Requirements</span></span>



| <span data-ttu-id="d6b93-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d6b93-114">Requirement</span></span> | <span data-ttu-id="d6b93-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d6b93-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b93-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6b93-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6b93-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6b93-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6b93-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6b93-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6b93-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6b93-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6b93-120">Header</span><span class="sxs-lookup"><span data-stu-id="d6b93-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6b93-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6b93-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





