---
title: Сообщение LVM_GETSELECTIONMARK (Коммктрл. h)
description: Извлекает метку выделения из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетселектионмарк ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Элементы управления Windows для LVM_GETSELECTIONMARK сообщений
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654653"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="af69e-105">\_Сообщение LVM жетселектионмарк</span><span class="sxs-lookup"><span data-stu-id="af69e-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="af69e-106">Извлекает метку выделения из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="af69e-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="af69e-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетселектионмарк ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="af69e-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af69e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af69e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af69e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af69e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af69e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="af69e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af69e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af69e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af69e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="af69e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af69e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af69e-113">Return value</span></span>

<span data-ttu-id="af69e-114">Возвращает знак выбора, начинающийся с нуля, или значение-1, если нет отметки выделения.</span><span class="sxs-lookup"><span data-stu-id="af69e-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="af69e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af69e-115">Remarks</span></span>

<span data-ttu-id="af69e-116">*Отметка выделения* — это индекс элемента, с которого начинается выбор нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="af69e-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="af69e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="af69e-117">Requirements</span></span>



| <span data-ttu-id="af69e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="af69e-118">Requirement</span></span> | <span data-ttu-id="af69e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="af69e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af69e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af69e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af69e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af69e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af69e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af69e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af69e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af69e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af69e-124">Header</span><span class="sxs-lookup"><span data-stu-id="af69e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af69e-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="af69e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af69e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af69e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af69e-127">**LVM \_ сетселектионмарк**</span><span class="sxs-lookup"><span data-stu-id="af69e-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





