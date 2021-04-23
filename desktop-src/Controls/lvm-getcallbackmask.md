---
title: Сообщение LVM_GETCALLBACKMASK (Коммктрл. h)
description: Возвращает маску обратного вызова для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жеткаллбаккмаск ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- Элементы управления Windows для LVM_GETCALLBACKMASK сообщений
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489069"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="ba8d0-105">\_Сообщение LVM жеткаллбаккмаск</span><span class="sxs-lookup"><span data-stu-id="ba8d0-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="ba8d0-106">Возвращает маску обратного вызова для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="ba8d0-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="ba8d0-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жеткаллбаккмаск ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="ba8d0-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba8d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba8d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba8d0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba8d0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ba8d0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ba8d0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba8d0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ba8d0-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ba8d0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8d0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba8d0-113">Return value</span></span>

<span data-ttu-id="ba8d0-114">Возвращает маску обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ba8d0-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ba8d0-115">Requirements</span></span>



| <span data-ttu-id="ba8d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ba8d0-116">Requirement</span></span> | <span data-ttu-id="ba8d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ba8d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8d0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba8d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8d0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba8d0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba8d0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba8d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8d0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba8d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba8d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="ba8d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba8d0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8d0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





