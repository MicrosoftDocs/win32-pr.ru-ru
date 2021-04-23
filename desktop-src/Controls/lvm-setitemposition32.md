---
title: Сообщение LVM_SETITEMPOSITION32 (Коммктрл. h)
description: Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Элементы управления Windows для LVM_SETITEMPOSITION32 сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071682"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="d72c1-104">\_Сообщение LVM SETITEMPOSITION32</span><span class="sxs-lookup"><span data-stu-id="d72c1-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="d72c1-105">Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка).</span><span class="sxs-lookup"><span data-stu-id="d72c1-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="d72c1-106">Это сообщение отличается от сообщения [**LVM \_ сетитемпоситион**](lvm-setitemposition.md) тем, что оно использует 32-разрядные координаты.</span><span class="sxs-lookup"><span data-stu-id="d72c1-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="d72c1-107">Это сообщение можно отправить явно или с помощью макроса [**\_ SetItemPosition32 ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .</span><span class="sxs-lookup"><span data-stu-id="d72c1-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d72c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d72c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d72c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d72c1-110">Индекс элемента представления списка, для которого задается позиция.</span><span class="sxs-lookup"><span data-stu-id="d72c1-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="d72c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d72c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d72c1-112">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , содержащую новую позицию элемента, в координатах представления списка.</span><span class="sxs-lookup"><span data-stu-id="d72c1-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d72c1-113">Return value</span></span>

<span data-ttu-id="d72c1-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d72c1-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72c1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d72c1-115">Requirements</span></span>



| <span data-ttu-id="d72c1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d72c1-116">Requirement</span></span> | <span data-ttu-id="d72c1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d72c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d72c1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d72c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d72c1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d72c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d72c1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d72c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d72c1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d72c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d72c1-122">Header</span><span class="sxs-lookup"><span data-stu-id="d72c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d72c1-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d72c1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

