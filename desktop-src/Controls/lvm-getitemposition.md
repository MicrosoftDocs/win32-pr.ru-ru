---
title: Сообщение LVM_GETITEMPOSITION (Коммктрл. h)
description: Возвращает позицию элемента представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемпоситион ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Элементы управления Windows для LVM_GETITEMPOSITION сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892453"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="7d8b2-105">\_Сообщение LVM жетитемпоситион</span><span class="sxs-lookup"><span data-stu-id="7d8b2-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="7d8b2-106">Возвращает позицию элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="7d8b2-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="7d8b2-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемпоситион ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .</span><span class="sxs-lookup"><span data-stu-id="7d8b2-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d8b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d8b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d8b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8b2-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="7d8b2-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d8b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8b2-112">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает позицию верхнего левого угла элемента в координатах представления.</span><span class="sxs-lookup"><span data-stu-id="7d8b2-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8b2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d8b2-113">Return value</span></span>

<span data-ttu-id="7d8b2-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7d8b2-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8b2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7d8b2-115">Requirements</span></span>



| <span data-ttu-id="7d8b2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7d8b2-116">Requirement</span></span> | <span data-ttu-id="7d8b2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8b2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d8b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8b2-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d8b2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d8b2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d8b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8b2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d8b2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d8b2-122">Header</span><span class="sxs-lookup"><span data-stu-id="7d8b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d8b2-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8b2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

