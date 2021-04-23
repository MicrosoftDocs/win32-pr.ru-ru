---
title: Сообщение LVM_GETFOCUSEDGROUP (Коммктрл. h)
description: Возвращает группу, в которой находится фокус. Отправьте это сообщение явным образом или с помощью \_ макроса Жетфокуседграуп ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Элементы управления Windows для LVM_GETFOCUSEDGROUP сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489057"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="45fb7-105">\_Сообщение LVM жетфокуседграуп</span><span class="sxs-lookup"><span data-stu-id="45fb7-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="45fb7-106">Возвращает группу, в которой находится фокус.</span><span class="sxs-lookup"><span data-stu-id="45fb7-106">Gets the group that has the focus.</span></span> <span data-ttu-id="45fb7-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфокуседграуп ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .</span><span class="sxs-lookup"><span data-stu-id="45fb7-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="45fb7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="45fb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45fb7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="45fb7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="45fb7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="45fb7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45fb7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="45fb7-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="45fb7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fb7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45fb7-113">Return value</span></span>

<span data-ttu-id="45fb7-114">Возвращает индекс группы с состоянием ЛВГС \_ Focused или-1, если нет группы с состоянием лвгс \_ Focused.</span><span class="sxs-lookup"><span data-stu-id="45fb7-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fb7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="45fb7-115">Requirements</span></span>



| <span data-ttu-id="45fb7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="45fb7-116">Requirement</span></span> | <span data-ttu-id="45fb7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="45fb7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45fb7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45fb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45fb7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45fb7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45fb7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45fb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45fb7-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45fb7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45fb7-122">Header</span><span class="sxs-lookup"><span data-stu-id="45fb7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45fb7-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="45fb7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





