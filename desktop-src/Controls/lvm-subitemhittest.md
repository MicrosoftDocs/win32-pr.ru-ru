---
title: Сообщение LVM_SUBITEMHITTEST (Коммктрл. h)
description: Определяет, какой элемент представления списка или подэлемент находится в заданной позиции. Это сообщение можно отправить явно или с помощью \_ макроса Субитемхиттест ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Элементы управления Windows для LVM_SUBITEMHITTEST сообщений
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489258"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="fc128-105">\_Сообщение LVM субитемхиттест</span><span class="sxs-lookup"><span data-stu-id="fc128-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="fc128-106">Определяет, какой элемент представления списка или подэлемент находится в заданной позиции.</span><span class="sxs-lookup"><span data-stu-id="fc128-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="fc128-107">Это сообщение можно отправить явно или с помощью макроса [**\_ субитемхиттест ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .</span><span class="sxs-lookup"><span data-stu-id="fc128-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc128-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc128-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc128-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc128-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc128-110">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="fc128-110">Must be 0.</span></span> <span data-ttu-id="fc128-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="fc128-111">**Windows Vista.**</span></span> <span data-ttu-id="fc128-112">Должен быть равен-1, если требуется извлечь элемент **играуп** объекта *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fc128-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="fc128-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc128-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc128-114">Указатель на структуру [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="fc128-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="fc128-115">Для структуры [**точек**](/previous-versions//dd162805(v=vs.85)) в **лвхиттестинфо** должны быть заданы клиентские координаты для проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="fc128-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc128-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc128-116">Return value</span></span>

<span data-ttu-id="fc128-117">Возвращает индекс элемента или подэлемента, который был протестирован, если он есть, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fc128-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="fc128-118">Если элемент или подэлемент имеет заданные координаты, поля структуры [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) будут заполнены соответствующими сведениями о попадании.</span><span class="sxs-lookup"><span data-stu-id="fc128-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc128-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fc128-119">Requirements</span></span>



| <span data-ttu-id="fc128-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fc128-120">Requirement</span></span> | <span data-ttu-id="fc128-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fc128-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc128-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc128-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc128-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc128-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc128-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc128-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc128-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc128-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc128-126">Header</span><span class="sxs-lookup"><span data-stu-id="fc128-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc128-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc128-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

