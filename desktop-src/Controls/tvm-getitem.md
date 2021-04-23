---
title: Сообщение TVM_GETITEM (Коммктрл. h)
description: Извлекает некоторые или все атрибуты элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса элемента TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Элементы управления Windows для TVM_GETITEM сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137827"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="c8673-105">\_Сообщение TVM</span><span class="sxs-lookup"><span data-stu-id="c8673-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="c8673-106">Извлекает некоторые или все атрибуты элемента представления дерева.</span><span class="sxs-lookup"><span data-stu-id="c8673-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="c8673-107">Это сообщение можно отправить явно или с помощью макроса [**\_ элемента TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="c8673-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8673-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8673-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8673-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8673-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8673-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c8673-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8673-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8673-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8673-112">Указатель на структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , указывающую сведения для извлечения и получения сведений об элементе.</span><span class="sxs-lookup"><span data-stu-id="c8673-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="c8673-113">В [версии 4,71](common-control-versions.md) и более поздних вместо нее можно использовать структуру [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="c8673-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8673-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8673-114">Return value</span></span>

<span data-ttu-id="c8673-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c8673-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8673-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8673-116">Remarks</span></span>

<span data-ttu-id="c8673-117">Когда сообщение отправляется, элемент **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) определяет элемент для получения сведений, а элемент **Mask** задает атрибуты для извлечения.</span><span class="sxs-lookup"><span data-stu-id="c8673-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="c8673-118">Если для \_ элемента **Mask** в структуре [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) задан флаг текста твиф, то элемент **псзтекст** должен указывать на допустимый буфер, а элемент **кчтекстмакс** должен быть установлен в число символов в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="c8673-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8673-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c8673-119">Requirements</span></span>



| <span data-ttu-id="c8673-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c8673-120">Requirement</span></span> | <span data-ttu-id="c8673-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c8673-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8673-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8673-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c8673-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8673-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8673-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8673-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c8673-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8673-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8673-126">Header</span><span class="sxs-lookup"><span data-stu-id="c8673-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8673-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8673-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c8673-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c8673-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c8673-129">**TVM \_ ЖЕТИТЕМВ** (Юникод) и **TVM- \_ элемент** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c8673-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





