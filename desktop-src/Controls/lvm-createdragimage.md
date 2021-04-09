---
title: Сообщение LVM_CREATEDRAGIMAGE (Коммктрл. h)
description: Создает список изображений для перетаскивания для указанного элемента. Это сообщение можно отправить явно или с помощью \_ макроса Креатедрагимаже ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Элементы управления Windows для LVM_CREATEDRAGIMAGE сообщений
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135139"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="d3b72-105">\_Сообщение LVM креатедрагимаже</span><span class="sxs-lookup"><span data-stu-id="d3b72-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="d3b72-106">Создает список изображений для перетаскивания для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="d3b72-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="d3b72-107">Это сообщение можно отправить явно или с помощью макроса [**\_ креатедрагимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="d3b72-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3b72-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3b72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3b72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b72-110">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="d3b72-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="d3b72-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3b72-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b72-112">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает начальное расположение верхнего левого угла изображения в координатах представления.</span><span class="sxs-lookup"><span data-stu-id="d3b72-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b72-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3b72-113">Return value</span></span>

<span data-ttu-id="d3b72-114">Возвращает маркер в список изображений перетаскивания в случае успеха или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d3b72-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b72-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3b72-115">Remarks</span></span>

<span data-ttu-id="d3b72-116">Приложение несет ответственность за уничтожение списка изображений, когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="d3b72-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b72-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d3b72-117">Requirements</span></span>



| <span data-ttu-id="d3b72-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d3b72-118">Requirement</span></span> | <span data-ttu-id="d3b72-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d3b72-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b72-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3b72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b72-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3b72-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3b72-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3b72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b72-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3b72-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3b72-124">Header</span><span class="sxs-lookup"><span data-stu-id="d3b72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b72-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b72-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

