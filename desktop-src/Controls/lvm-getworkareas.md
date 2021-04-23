---
title: Сообщение LVM_GETWORKAREAS (Коммктрл. h)
description: Извлекает рабочие области из элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетворкареас ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Элементы управления Windows для LVM_GETWORKAREAS сообщений
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492396"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="39cde-105">\_Сообщение LVM жетворкареас</span><span class="sxs-lookup"><span data-stu-id="39cde-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="39cde-106">Извлекает рабочие области из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="39cde-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="39cde-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетворкареас ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .</span><span class="sxs-lookup"><span data-stu-id="39cde-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="39cde-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39cde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39cde-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39cde-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39cde-110">Число структур [**Rect**](/previous-versions//dd162897(v=vs.85)) в массиве в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="39cde-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="39cde-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39cde-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39cde-112">Указатель на массив структур [**Rect**](/previous-versions//dd162897(v=vs.85)) , который получает текущие рабочие области элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="39cde-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="39cde-113">Значения в этих структурах находятся в клиентских координатах.</span><span class="sxs-lookup"><span data-stu-id="39cde-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="39cde-114">*wParam* задает количество структур в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="39cde-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39cde-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39cde-115">Return value</span></span>

<span data-ttu-id="39cde-116">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="39cde-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="39cde-117">Требования</span><span class="sxs-lookup"><span data-stu-id="39cde-117">Requirements</span></span>



| <span data-ttu-id="39cde-118">Требование</span><span class="sxs-lookup"><span data-stu-id="39cde-118">Requirement</span></span> | <span data-ttu-id="39cde-119">Значение</span><span class="sxs-lookup"><span data-stu-id="39cde-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39cde-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39cde-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39cde-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39cde-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39cde-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39cde-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39cde-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39cde-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39cde-124">Header</span><span class="sxs-lookup"><span data-stu-id="39cde-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39cde-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="39cde-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39cde-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39cde-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cde-127">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="39cde-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

