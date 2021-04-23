---
title: Сообщение HDM_CREATEDRAGIMAGE (Коммктрл. h)
description: Создает полупрозрачную версию изображения элемента для использования в качестве изображения для перетаскивания. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса креатедрагимаже.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Элементы управления Windows для HDM_CREATEDRAGIMAGE сообщений
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071782"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="3e8c3-105">\_Сообщение КРЕАТЕДРАГИМАЖЕ HDM</span><span class="sxs-lookup"><span data-stu-id="3e8c3-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="3e8c3-106">Создает полупрозрачную версию изображения элемента для использования в качестве изображения для перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="3e8c3-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="3e8c3-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ креатедрагимаже**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="3e8c3-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e8c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e8c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e8c3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8c3-110">Отсчитываемый от нуля индекс элемента в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="3e8c3-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="3e8c3-111">Изображение, назначенное этому элементу, является основанием для прозрачного изображения.</span><span class="sxs-lookup"><span data-stu-id="3e8c3-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="3e8c3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e8c3-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3e8c3-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3e8c3-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8c3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e8c3-114">Return value</span></span>

<span data-ttu-id="3e8c3-115">Возвращает маркер в список изображений, содержащий новый образ в качестве единственного элемента.</span><span class="sxs-lookup"><span data-stu-id="3e8c3-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8c3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3e8c3-116">Requirements</span></span>



| <span data-ttu-id="3e8c3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3e8c3-117">Requirement</span></span> | <span data-ttu-id="3e8c3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3e8c3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8c3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e8c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8c3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e8c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e8c3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e8c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8c3-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e8c3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e8c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e8c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e8c3-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8c3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





