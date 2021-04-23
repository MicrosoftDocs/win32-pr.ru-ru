---
title: Сообщение LVM_ENSUREVISIBLE (Коммктрл. h)
description: Гарантирует, что элемент списка является полностью или частично видимым, при необходимости прокручивать элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Енсуревисибле ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Элементы управления Windows для LVM_ENSUREVISIBLE сообщений
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988204"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="c2aa0-105">\_Сообщение LVM енсуревисибле</span><span class="sxs-lookup"><span data-stu-id="c2aa0-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="c2aa0-106">Гарантирует, что элемент списка является полностью или частично видимым, при необходимости прокручивать элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c2aa0-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="c2aa0-107">Это сообщение можно отправить явно или с помощью макроса [**\_ енсуревисибле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="c2aa0-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2aa0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2aa0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2aa0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2aa0-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2aa0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2aa0-112">Значение типа, указывающее, должен ли элемент быть полностью видимым.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="c2aa0-113">Если этот параметр имеет **значение true**, прокрутка не выполняется, если элемент является по крайней мере частично видимым.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2aa0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2aa0-114">Return value</span></span>

<span data-ttu-id="c2aa0-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2aa0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2aa0-116">Remarks</span></span>

<span data-ttu-id="c2aa0-117">Сообщение завершается ошибкой, если стиль окна включает [**LVS " \_ Scroll**](list-view-window-styles.md)".</span><span class="sxs-lookup"><span data-stu-id="c2aa0-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2aa0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c2aa0-118">Requirements</span></span>



| <span data-ttu-id="c2aa0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c2aa0-119">Requirement</span></span> | <span data-ttu-id="c2aa0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c2aa0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2aa0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2aa0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2aa0-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2aa0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2aa0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2aa0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2aa0-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2aa0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2aa0-125">Header</span><span class="sxs-lookup"><span data-stu-id="c2aa0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2aa0-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2aa0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





