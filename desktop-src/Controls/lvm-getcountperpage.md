---
title: Сообщение LVM_GETCOUNTPERPAGE (Коммктрл. h)
description: Вычисляет количество элементов, которые могут быть размещены вертикально в видимой области элемента управления "представление списка" в списке или представлении отчетов. Учитываются только полностью видимые элементы. Это сообщение можно отправить явно или с помощью \_ макроса Жеткаунтперпаже ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Элементы управления Windows для LVM_GETCOUNTPERPAGE сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071122"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="bcb8c-106">\_Сообщение LVM жеткаунтперпаже</span><span class="sxs-lookup"><span data-stu-id="bcb8c-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="bcb8c-107">Вычисляет количество элементов, которые могут быть размещены вертикально в видимой области элемента управления "представление списка" в списке или представлении отчетов.</span><span class="sxs-lookup"><span data-stu-id="bcb8c-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="bcb8c-108">Учитываются только полностью видимые элементы.</span><span class="sxs-lookup"><span data-stu-id="bcb8c-108">Only fully visible items are counted.</span></span> <span data-ttu-id="bcb8c-109">Это сообщение можно отправить явно или с помощью макроса [**\_ жеткаунтперпаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .</span><span class="sxs-lookup"><span data-stu-id="bcb8c-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcb8c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcb8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb8c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcb8c-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcb8c-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bcb8c-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcb8c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcb8c-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcb8c-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bcb8c-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb8c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcb8c-115">Return value</span></span>

<span data-ttu-id="bcb8c-116">Возвращает количество полностью видимых элементов в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="bcb8c-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="bcb8c-117">Если текущее представление является значком или небольшим значком, возвращаемое значение — это общее число элементов в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="bcb8c-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb8c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bcb8c-118">Requirements</span></span>



| <span data-ttu-id="bcb8c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bcb8c-119">Requirement</span></span> | <span data-ttu-id="bcb8c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bcb8c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb8c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcb8c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb8c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcb8c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcb8c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcb8c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb8c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcb8c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcb8c-125">Header</span><span class="sxs-lookup"><span data-stu-id="bcb8c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb8c-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb8c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





