---
title: Сообщение TVM_HITTEST (Коммктрл. h)
description: Определяет расположение указанной точки относительно клиентской области элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса HitTest TreeView.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Элементы управления Windows для TVM_HITTEST сообщений
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071364"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="7e426-105">\_Сообщение TVM HITTEST</span><span class="sxs-lookup"><span data-stu-id="7e426-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="7e426-106">Определяет расположение указанной точки относительно клиентской области элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="7e426-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="7e426-107">Это сообщение можно отправить явно или с помощью макроса [**\_ HitTest TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="7e426-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e426-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e426-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e426-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e426-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7e426-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7e426-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7e426-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e426-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e426-112">Указатель на структуру [**твхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="7e426-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="7e426-113">При отправке сообщения элемент **PT** указывает координаты проверяемой точки.</span><span class="sxs-lookup"><span data-stu-id="7e426-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="7e426-114">При возвращении сообщения элемент **хитем** является маркером элемента в указанной точке или **значением NULL** , если элемент не занимает точку.</span><span class="sxs-lookup"><span data-stu-id="7e426-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="7e426-115">Кроме того, при возвращении сообщения элемент **flags** является значением проверки нажатия, которое указывает расположение указанной точки.</span><span class="sxs-lookup"><span data-stu-id="7e426-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="7e426-116">Список значений проверки попадания см. в описании структуры **твхиттестинфо** .</span><span class="sxs-lookup"><span data-stu-id="7e426-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e426-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e426-117">Return value</span></span>

<span data-ttu-id="7e426-118">Возвращает маркер элемента представления дерева, который занимает указанную точку, или **значение NULL** , если элемент не занимает точку.</span><span class="sxs-lookup"><span data-stu-id="7e426-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e426-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7e426-119">Requirements</span></span>



| <span data-ttu-id="7e426-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7e426-120">Requirement</span></span> | <span data-ttu-id="7e426-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7e426-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e426-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e426-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e426-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e426-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e426-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e426-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e426-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e426-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e426-126">Header</span><span class="sxs-lookup"><span data-stu-id="7e426-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e426-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e426-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





