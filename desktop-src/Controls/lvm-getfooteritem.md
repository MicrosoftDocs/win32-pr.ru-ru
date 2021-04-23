---
title: Сообщение LVM_GETFOOTERITEM (Коммктрл. h)
description: Возвращает сведения о элементе нижнего колонтитула в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеритем ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Элементы управления Windows для LVM_GETFOOTERITEM сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071116"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="17bff-105">\_Сообщение LVM жетфутеритем</span><span class="sxs-lookup"><span data-stu-id="17bff-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="17bff-106">Возвращает сведения о элементе нижнего колонтитула в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="17bff-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="17bff-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеритем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .</span><span class="sxs-lookup"><span data-stu-id="17bff-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17bff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="17bff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bff-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17bff-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bff-110">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="17bff-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="17bff-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="17bff-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17bff-112">Указатель на структуру [**лвфутеритем**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) для получения значения для элементов **State** и/или **псзтекст** в соответствии со значением элемента **маски** .</span><span class="sxs-lookup"><span data-stu-id="17bff-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="17bff-113">Вызывающий процесс отвечает за выделение этой структуры и установку ее членов для указания получателю возвращаемой информации.</span><span class="sxs-lookup"><span data-stu-id="17bff-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="17bff-114">Дополнительные сведения см. в разделе **лвфутеритем**.</span><span class="sxs-lookup"><span data-stu-id="17bff-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bff-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17bff-115">Return value</span></span>

<span data-ttu-id="17bff-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="17bff-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="17bff-117">Требования</span><span class="sxs-lookup"><span data-stu-id="17bff-117">Requirements</span></span>



| <span data-ttu-id="17bff-118">Требование</span><span class="sxs-lookup"><span data-stu-id="17bff-118">Requirement</span></span> | <span data-ttu-id="17bff-119">Значение</span><span class="sxs-lookup"><span data-stu-id="17bff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17bff-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17bff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17bff-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17bff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17bff-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17bff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17bff-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17bff-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17bff-124">Header</span><span class="sxs-lookup"><span data-stu-id="17bff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17bff-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="17bff-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





