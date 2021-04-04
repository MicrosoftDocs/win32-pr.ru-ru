---
title: Код уведомления NM_RDBLCLK (в виде дерева) (Коммктрл. h)
description: Уведомляет родительский элемент управления представлением дерева о том, что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления. Это уведомление отправляется в виде \_ сообщения WM notify.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (представление в виде дерева)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136967"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a><span data-ttu-id="ed8b2-105">\_Код уведомления NM рдблклк (в виде дерева)</span><span class="sxs-lookup"><span data-stu-id="ed8b2-105">NM\_RDBLCLK (tree view) notification code</span></span>

<span data-ttu-id="ed8b2-106">Уведомляет родительский элемент управления представлением дерева о том, что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-106">Notifies the parent of a tree-view control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="ed8b2-107">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ed8b2-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ed8b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed8b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed8b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8b2-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed8b2-111">Return value</span></span>

<span data-ttu-id="ed8b2-112">Возвращает ненулевое значение, чтобы предотвратить обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8b2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ed8b2-113">Requirements</span></span>



| <span data-ttu-id="ed8b2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ed8b2-114">Requirement</span></span> | <span data-ttu-id="ed8b2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ed8b2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8b2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed8b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8b2-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed8b2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed8b2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed8b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8b2-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed8b2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed8b2-120">Header</span><span class="sxs-lookup"><span data-stu-id="ed8b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8b2-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8b2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





