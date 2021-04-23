---
title: Сообщение LVM_GETHOTITEM (Коммктрл. h)
description: Извлекает индекс горячего элемента. Это сообщение можно отправить явным образом или использовать \_ макрос Жесотитем ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- Элементы управления Windows для LVM_GETHOTITEM сообщений
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137122"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="d7ff8-105">\_Сообщение LVM жесотитем</span><span class="sxs-lookup"><span data-stu-id="d7ff8-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="d7ff8-106">Извлекает индекс горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="d7ff8-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="d7ff8-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жесотитем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .</span><span class="sxs-lookup"><span data-stu-id="d7ff8-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7ff8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7ff8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ff8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7ff8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d7ff8-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d7ff8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d7ff8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7ff8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7ff8-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d7ff8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ff8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7ff8-113">Return value</span></span>

<span data-ttu-id="d7ff8-114">Возвращает индекс неактивного элемента.</span><span class="sxs-lookup"><span data-stu-id="d7ff8-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ff8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ff8-115">Requirements</span></span>



| <span data-ttu-id="d7ff8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ff8-116">Requirement</span></span> | <span data-ttu-id="d7ff8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ff8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ff8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7ff8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ff8-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7ff8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7ff8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7ff8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ff8-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7ff8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7ff8-122">Header</span><span class="sxs-lookup"><span data-stu-id="d7ff8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ff8-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ff8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





