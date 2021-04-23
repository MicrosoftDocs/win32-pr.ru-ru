---
title: Код уведомления NM_RCLICK (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления представлением дерева, что пользователь щелкнул правой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- Элементы управления Windows для кода уведомления NM_RCLICK (представление в виде дерева)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137858"
---
# <a name="nm_rclick-tree-view-notification-code"></a><span data-ttu-id="ab48d-105">\_Код уведомления NM ркликк (в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="ab48d-105">NM\_RCLICK (tree view) notification code</span></span>

<span data-ttu-id="ab48d-106">Сообщает родительскому окну элемента управления представлением дерева, что пользователь щелкнул правой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="ab48d-106">Notifies the parent window of a tree-view control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="ab48d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ab48d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ab48d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab48d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab48d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab48d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab48d-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ab48d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab48d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab48d-111">Return value</span></span>

<span data-ttu-id="ab48d-112">Возвращает ненулевое значение, чтобы предотвратить обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab48d-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab48d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ab48d-113">Requirements</span></span>



| <span data-ttu-id="ab48d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ab48d-114">Requirement</span></span> | <span data-ttu-id="ab48d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ab48d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab48d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab48d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab48d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab48d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab48d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab48d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab48d-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab48d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab48d-120">Header</span><span class="sxs-lookup"><span data-stu-id="ab48d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab48d-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab48d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





