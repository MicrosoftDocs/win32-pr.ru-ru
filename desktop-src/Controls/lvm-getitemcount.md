---
title: Сообщение LVM_GETITEMCOUNT (Коммктрл. h)
description: Извлекает количество элементов в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса GetItemCount ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Элементы управления Windows для LVM_GETITEMCOUNT сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803394"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="6b382-105">\_Сообщение LVM GETITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b382-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="6b382-106">Извлекает количество элементов в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="6b382-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="6b382-107">Это сообщение можно отправить явно или с помощью макроса [**\_ GetItemCount ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="6b382-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b382-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b382-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b382-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b382-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6b382-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6b382-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6b382-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b382-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6b382-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6b382-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b382-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b382-113">Return value</span></span>

<span data-ttu-id="6b382-114">Возвращает число элементов.</span><span class="sxs-lookup"><span data-stu-id="6b382-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b382-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6b382-115">Requirements</span></span>



| <span data-ttu-id="6b382-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6b382-116">Requirement</span></span> | <span data-ttu-id="6b382-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6b382-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b382-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b382-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b382-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b382-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b382-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b382-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b382-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b382-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b382-122">Header</span><span class="sxs-lookup"><span data-stu-id="6b382-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b382-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b382-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





