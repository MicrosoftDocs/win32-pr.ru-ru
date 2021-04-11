---
title: Сообщение TVM_CREATEDRAGIMAGE (Коммктрл. h)
description: Создает перетаскивание растрового изображения для указанного элемента в элементе управления "дерево".
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Элементы управления Windows для TVM_CREATEDRAGIMAGE сообщений
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136047"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="02bd8-104">\_Сообщение TVM креатедрагимаже</span><span class="sxs-lookup"><span data-stu-id="02bd8-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="02bd8-105">Создает перетаскивание растрового изображения для указанного элемента в элементе управления "дерево".</span><span class="sxs-lookup"><span data-stu-id="02bd8-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="02bd8-106">Сообщение также создает список изображений для растрового изображения и добавляет его в список изображений.</span><span class="sxs-lookup"><span data-stu-id="02bd8-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="02bd8-107">Приложение может отображать изображение при перетаскивании элемента с помощью функций списка изображений.</span><span class="sxs-lookup"><span data-stu-id="02bd8-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="02bd8-108">Это сообщение можно отправить явно или с помощью макроса [**\_ креатедрагимаже TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="02bd8-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="02bd8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="02bd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bd8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02bd8-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="02bd8-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="02bd8-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="02bd8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02bd8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02bd8-113">Указатель на элемент, который получает новое растровое изображение перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="02bd8-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bd8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02bd8-114">Return value</span></span>

<span data-ttu-id="02bd8-115">Возвращает маркер для списка изображений, к которому был добавлен растровый рисунок при успешном выполнении, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="02bd8-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="02bd8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02bd8-116">Remarks</span></span>

<span data-ttu-id="02bd8-117">При создании элемента управления "дерево-представление" без связанного списка изображений нельзя использовать сообщение **TVM \_ креатедрагимаже** для создания изображения, которое будет отображаться во время операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="02bd8-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="02bd8-118">Необходимо реализовать собственный метод создания курсора перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="02bd8-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="02bd8-119">Приложение несет ответственность за уничтожение списка изображений, когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="02bd8-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="02bd8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="02bd8-120">Requirements</span></span>



| <span data-ttu-id="02bd8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="02bd8-121">Requirement</span></span> | <span data-ttu-id="02bd8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02bd8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02bd8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="02bd8-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02bd8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02bd8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02bd8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="02bd8-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02bd8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02bd8-127">Header</span><span class="sxs-lookup"><span data-stu-id="02bd8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="02bd8-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="02bd8-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





