---
title: Сообщение LVM_SETHOTITEM (Коммктрл. h)
description: Задает активный элемент для элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сесотитем ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Элементы управления Windows для LVM_SETHOTITEM сообщений
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801108"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="8017e-105">\_Сообщение LVM сесотитем</span><span class="sxs-lookup"><span data-stu-id="8017e-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="8017e-106">Задает активный элемент для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="8017e-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="8017e-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сесотитем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .</span><span class="sxs-lookup"><span data-stu-id="8017e-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8017e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8017e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8017e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8017e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8017e-110">Отсчитываемый от нуля индекс элемента, который должен быть установлен в качестве горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="8017e-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="8017e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8017e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8017e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8017e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8017e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8017e-113">Return value</span></span>

<span data-ttu-id="8017e-114">Возвращает индекс элемента, который ранее был неактивен.</span><span class="sxs-lookup"><span data-stu-id="8017e-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="8017e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8017e-115">Requirements</span></span>



| <span data-ttu-id="8017e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8017e-116">Requirement</span></span> | <span data-ttu-id="8017e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8017e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8017e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8017e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8017e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8017e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8017e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8017e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8017e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8017e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8017e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8017e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8017e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8017e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





