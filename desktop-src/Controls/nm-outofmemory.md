---
title: Код уведомления NM_OUTOFMEMORY (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элементу управления не удалось выполнить операцию из-за нехватки памяти. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071184"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="3cd28-105">\_Код уведомления OUTOFMEMORY (NM)</span><span class="sxs-lookup"><span data-stu-id="3cd28-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="3cd28-106">Сообщает родительскому окну элемента управления, что элементу управления не удалось выполнить операцию из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="3cd28-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="3cd28-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3cd28-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3cd28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cd28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cd28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd28-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="3cd28-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cd28-111">Return value</span></span>

<span data-ttu-id="3cd28-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="3cd28-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd28-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3cd28-113">Requirements</span></span>



| <span data-ttu-id="3cd28-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3cd28-114">Requirement</span></span> | <span data-ttu-id="3cd28-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3cd28-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd28-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cd28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd28-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cd28-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cd28-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cd28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd28-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3cd28-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cd28-120">Header</span><span class="sxs-lookup"><span data-stu-id="3cd28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cd28-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd28-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





