---
title: Сообщение TVM_SETITEM (Коммктрл. h)
description: В \_ сообщении TVM сетитем задаются некоторые или все атрибуты элемента представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Сетитем TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Элементы управления Windows для TVM_SETITEM сообщений
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490842"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="6c3b8-105">\_Сообщение TVM сетитем</span><span class="sxs-lookup"><span data-stu-id="6c3b8-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="6c3b8-106">В сообщении **TVM \_ сетитем** задаются некоторые или все атрибуты элемента представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="6c3b8-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="6c3b8-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="6c3b8-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c3b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c3b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3b8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c3b8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c3b8-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6c3b8-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c3b8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c3b8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c3b8-112">Указатель на структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , содержащую новые атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="6c3b8-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="6c3b8-113">В [версии 4,71](common-control-versions.md) и более поздних вместо нее можно использовать структуру [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="6c3b8-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3b8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c3b8-114">Return value</span></span>

<span data-ttu-id="6c3b8-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c3b8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3b8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c3b8-116">Remarks</span></span>

<span data-ttu-id="6c3b8-117">Член **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) определяет элемент, а элемент **Mask** указывает, какие атрибуты задаются.</span><span class="sxs-lookup"><span data-stu-id="6c3b8-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3b8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3b8-118">Requirements</span></span>



| <span data-ttu-id="6c3b8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6c3b8-119">Requirement</span></span> | <span data-ttu-id="6c3b8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6c3b8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3b8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c3b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3b8-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c3b8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c3b8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c3b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3b8-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c3b8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c3b8-125">Header</span><span class="sxs-lookup"><span data-stu-id="6c3b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3b8-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3b8-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6c3b8-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6c3b8-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c3b8-128">**TVM \_ СЕТИТЕМВ** (Юникод) и **TVM \_ сетитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c3b8-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





