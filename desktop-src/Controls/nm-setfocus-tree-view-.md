---
title: Код уведомления NM_SETFOCUS (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления получил фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4bdd6cd2-afd3-4c0b-914b-8fff55e474a9
keywords:
- Элементы управления Windows для кода уведомления NM_SETFOCUS (представление в виде дерева)
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
ms.openlocfilehash: 1b9e24d95b95b3c66fe43920f780b2e8d0f66679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892053"
---
# <a name="nm_setfocus-tree-view-notification-code"></a><span data-ttu-id="60416-105">\_Код уведомления NM (представление в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="60416-105">NM\_SETFOCUS (tree view) notification code</span></span>

<span data-ttu-id="60416-106">Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления получил фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="60416-106">Notifies a tree-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="60416-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="60416-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="60416-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60416-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60416-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60416-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="60416-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60416-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60416-111">Return value</span></span>

<span data-ttu-id="60416-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="60416-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="60416-113">Требования</span><span class="sxs-lookup"><span data-stu-id="60416-113">Requirements</span></span>



| <span data-ttu-id="60416-114">Требование</span><span class="sxs-lookup"><span data-stu-id="60416-114">Requirement</span></span> | <span data-ttu-id="60416-115">Значение</span><span class="sxs-lookup"><span data-stu-id="60416-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60416-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60416-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60416-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60416-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60416-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60416-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60416-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60416-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60416-120">Header</span><span class="sxs-lookup"><span data-stu-id="60416-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60416-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="60416-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





