---
title: Сообщение LVM_GETNUMBEROFWORKAREAS (Коммктрл. h)
description: Извлекает количество рабочих областей в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетнумберофворкареас ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Элементы управления Windows для LVM_GETNUMBEROFWORKAREAS сообщений
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989174"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="3d5e3-105">\_Сообщение LVM жетнумберофворкареас</span><span class="sxs-lookup"><span data-stu-id="3d5e3-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="3d5e3-106">Извлекает количество рабочих областей в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="3d5e3-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="3d5e3-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетнумберофворкареас ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .</span><span class="sxs-lookup"><span data-stu-id="3d5e3-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d5e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d5e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d5e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3d5e3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3d5e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d5e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5e3-112">Указатель на значение UINT, которое получает количество рабочих областей в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="3d5e3-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="3d5e3-113">Если в эту переменную помещается ноль, то в настоящее время не заданы никакие рабочие области.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="3d5e3-114">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d5e3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d5e3-115">Return value</span></span>

<span data-ttu-id="3d5e3-116">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d5e3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3d5e3-117">Requirements</span></span>



| <span data-ttu-id="3d5e3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3d5e3-118">Requirement</span></span> | <span data-ttu-id="3d5e3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3d5e3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d5e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5e3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d5e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d5e3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d5e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5e3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d5e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d5e3-124">Header</span><span class="sxs-lookup"><span data-stu-id="3d5e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5e3-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5e3-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5e3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d5e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5e3-127">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="3d5e3-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





