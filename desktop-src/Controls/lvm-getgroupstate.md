---
title: Сообщение LVM_GETGROUPSTATE (Коммктрл. h)
description: Возвращает состояние указанной группы. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупстате ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Элементы управления Windows для LVM_GETGROUPSTATE сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489267"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="4eb55-105">\_Сообщение LVM жетграупстате</span><span class="sxs-lookup"><span data-stu-id="4eb55-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="4eb55-106">Возвращает состояние указанной группы.</span><span class="sxs-lookup"><span data-stu-id="4eb55-106">Gets the state for a specified group.</span></span> <span data-ttu-id="4eb55-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетграупстате ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .</span><span class="sxs-lookup"><span data-stu-id="4eb55-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4eb55-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eb55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb55-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb55-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb55-110">Задает Group By **играупид** (см. структуру [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="4eb55-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="4eb55-111">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb55-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb55-112">Указывает извлекаемые значения состояния.</span><span class="sxs-lookup"><span data-stu-id="4eb55-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="4eb55-113">Это сочетание флагов, перечисленных для элемента **State** элемента [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span><span class="sxs-lookup"><span data-stu-id="4eb55-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb55-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eb55-114">Return value</span></span>

<span data-ttu-id="4eb55-115">Возвращает сочетание заданных значений состояния.</span><span class="sxs-lookup"><span data-stu-id="4eb55-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="4eb55-116">Например, если параметр *lParam* лвгс \_ свернут и возвращенное значение равно нулю, то лвгс \_ свернутое состояние не задано.</span><span class="sxs-lookup"><span data-stu-id="4eb55-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="4eb55-117">Если группа не найдена, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="4eb55-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb55-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb55-118">Requirements</span></span>



| <span data-ttu-id="4eb55-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb55-119">Requirement</span></span> | <span data-ttu-id="4eb55-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb55-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb55-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb55-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4eb55-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4eb55-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb55-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4eb55-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4eb55-125">Header</span><span class="sxs-lookup"><span data-stu-id="4eb55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb55-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb55-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





