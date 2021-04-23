---
title: Сообщение HDM_GETITEMCOUNT (Коммктрл. h)
description: Возвращает число элементов в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Элементы управления Windows для HDM_GETITEMCOUNT сообщений
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136435"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="3eec2-105">\_Сообщение GETITEMCOUNT HDM</span><span class="sxs-lookup"><span data-stu-id="3eec2-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="3eec2-106">Возвращает число элементов в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="3eec2-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="3eec2-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="3eec2-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3eec2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3eec2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eec2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3eec2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3eec2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3eec2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3eec2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3eec2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3eec2-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3eec2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eec2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3eec2-113">Return value</span></span>

<span data-ttu-id="3eec2-114">Возвращает количество элементов в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3eec2-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eec2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3eec2-115">Requirements</span></span>



| <span data-ttu-id="3eec2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3eec2-116">Requirement</span></span> | <span data-ttu-id="3eec2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3eec2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eec2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3eec2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3eec2-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3eec2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3eec2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3eec2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3eec2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3eec2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3eec2-122">Header</span><span class="sxs-lookup"><span data-stu-id="3eec2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eec2-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eec2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





