---
title: Сообщение LVM_DELETEALLITEMS (Коммктрл. h)
description: Удаляет все элементы из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Делетеаллитемс ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Элементы управления Windows для LVM_DELETEALLITEMS сообщений
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489093"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="53f08-105">\_Сообщение LVM делетеаллитемс</span><span class="sxs-lookup"><span data-stu-id="53f08-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="53f08-106">Удаляет все элементы из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="53f08-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="53f08-107">Это сообщение можно отправить явно или с помощью макроса [**\_ делетеаллитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="53f08-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="53f08-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53f08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f08-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53f08-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53f08-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="53f08-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="53f08-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53f08-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="53f08-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="53f08-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f08-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53f08-113">Return value</span></span>

<span data-ttu-id="53f08-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="53f08-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f08-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53f08-115">Remarks</span></span>

<span data-ttu-id="53f08-116">Когда элемент управления "представление списка" получает сообщение **LVM \_ делетеаллитемс** , он отправляет код уведомления [**ЛВН \_ делетеаллитемс**](lvn-deleteallitems.md) в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="53f08-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f08-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53f08-117">Requirements</span></span>



| <span data-ttu-id="53f08-118">Требование</span><span class="sxs-lookup"><span data-stu-id="53f08-118">Requirement</span></span> | <span data-ttu-id="53f08-119">Значение</span><span class="sxs-lookup"><span data-stu-id="53f08-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53f08-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53f08-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53f08-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53f08-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53f08-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53f08-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53f08-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53f08-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53f08-124">Header</span><span class="sxs-lookup"><span data-stu-id="53f08-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f08-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f08-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





