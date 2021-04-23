---
title: Код уведомления NM_RETURN (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления имеет фокус ввода и что пользователь нажал на клавишу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- Элементы управления Windows для кода уведомления NM_RETURN (представление в виде дерева)
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
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989078"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="6edcf-105">\_Код уведомления "NM return" (представление в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="6edcf-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="6edcf-106">Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления имеет фокус ввода и что пользователь нажал на клавишу.</span><span class="sxs-lookup"><span data-stu-id="6edcf-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="6edcf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6edcf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6edcf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6edcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6edcf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6edcf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6edcf-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="6edcf-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6edcf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6edcf-111">Return value</span></span>

<span data-ttu-id="6edcf-112">Возвращает ненулевое значение, чтобы предотвратить обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6edcf-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edcf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6edcf-113">Requirements</span></span>



| <span data-ttu-id="6edcf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6edcf-114">Requirement</span></span> | <span data-ttu-id="6edcf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6edcf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6edcf-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6edcf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6edcf-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6edcf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6edcf-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6edcf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6edcf-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6edcf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6edcf-120">Header</span><span class="sxs-lookup"><span data-stu-id="6edcf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edcf-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6edcf-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





