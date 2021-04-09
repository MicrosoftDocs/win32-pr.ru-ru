---
title: Сообщение LVM_ISITEMVISIBLE (Коммктрл. h)
description: Указывает, является ли видимым элемент в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Иситемвисибле ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Элементы управления Windows для LVM_ISITEMVISIBLE сообщений
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892433"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="ef8c6-105">\_Сообщение LVM иситемвисибле</span><span class="sxs-lookup"><span data-stu-id="ef8c6-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="ef8c6-106">Указывает, является ли видимым элемент в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="ef8c6-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="ef8c6-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ иситемвисибле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="ef8c6-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef8c6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef8c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8c6-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef8c6-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8c6-110">Индекс элемента в элементе управления List-View.</span><span class="sxs-lookup"><span data-stu-id="ef8c6-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="ef8c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef8c6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ef8c6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ef8c6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8c6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef8c6-113">Return value</span></span>

<span data-ttu-id="ef8c6-114">Возвращает **значение true** , если видимое, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ef8c6-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8c6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ef8c6-115">Requirements</span></span>



| <span data-ttu-id="ef8c6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ef8c6-116">Requirement</span></span> | <span data-ttu-id="ef8c6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ef8c6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8c6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef8c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8c6-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef8c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef8c6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef8c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8c6-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef8c6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef8c6-122">Header</span><span class="sxs-lookup"><span data-stu-id="ef8c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef8c6-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef8c6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





