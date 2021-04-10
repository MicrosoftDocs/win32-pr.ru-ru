---
title: Сообщение BM_SETIMAGE (Winuser. h)
description: Связывает новый образ (значок или растровое изображение) с кнопкой.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Элементы управления Windows для BM_SETIMAGE сообщений
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135367"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="3c5df-104">\_Сообщение BM сетимаже</span><span class="sxs-lookup"><span data-stu-id="3c5df-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="3c5df-105">Связывает новый образ (значок или растровое изображение) с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="3c5df-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c5df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c5df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c5df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5df-108">Тип изображения, связываемого с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="3c5df-108">The type of image to associate with the button.</span></span> <span data-ttu-id="3c5df-109">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3c5df-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="3c5df-110">\_точечный рисунок изображения</span><span class="sxs-lookup"><span data-stu-id="3c5df-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="3c5df-111">\_значок изображения</span><span class="sxs-lookup"><span data-stu-id="3c5df-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="3c5df-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c5df-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5df-113">Маркер (**Хикон** или **хбитмап**) к изображению, связываемый с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="3c5df-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5df-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c5df-114">Return value</span></span>

<span data-ttu-id="3c5df-115">Возвращаемое значение является обработчиком изображения, ранее связанного с кнопкой, если таковая имеется; в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3c5df-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5df-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c5df-116">Remarks</span></span>

<span data-ttu-id="3c5df-117">Внешний вид текста, значка или обоих элементов в элементе управления "Кнопка" зависит от [**\_ значка BS**](button-styles.md) и стилей [**\_ растрового изображения BS**](button-styles.md) , а также от того, вызывается ли сообщение **BM \_ сетимаже** .</span><span class="sxs-lookup"><span data-stu-id="3c5df-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="3c5df-118">Возможны следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="3c5df-118">The possible results are as follows:</span></span>



| <span data-ttu-id="3c5df-119">\_Значок BS или \_ набор битовых карт BS?</span><span class="sxs-lookup"><span data-stu-id="3c5df-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="3c5df-120">\_Вызвана СЕТИМАЖЕ BM?</span><span class="sxs-lookup"><span data-stu-id="3c5df-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="3c5df-121">Результат</span><span class="sxs-lookup"><span data-stu-id="3c5df-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="3c5df-122">Да</span><span class="sxs-lookup"><span data-stu-id="3c5df-122">Yes</span></span>                         | <span data-ttu-id="3c5df-123">Да</span><span class="sxs-lookup"><span data-stu-id="3c5df-123">Yes</span></span>                  | <span data-ttu-id="3c5df-124">Отображать только значок.</span><span class="sxs-lookup"><span data-stu-id="3c5df-124">Show icon only.</span></span>     |
| <span data-ttu-id="3c5df-125">Нет</span><span class="sxs-lookup"><span data-stu-id="3c5df-125">No</span></span>                          | <span data-ttu-id="3c5df-126">Да</span><span class="sxs-lookup"><span data-stu-id="3c5df-126">Yes</span></span>                  | <span data-ttu-id="3c5df-127">Отображение значка и текста.</span><span class="sxs-lookup"><span data-stu-id="3c5df-127">Show icon and text.</span></span> |
| <span data-ttu-id="3c5df-128">Да</span><span class="sxs-lookup"><span data-stu-id="3c5df-128">Yes</span></span>                         | <span data-ttu-id="3c5df-129">Нет</span><span class="sxs-lookup"><span data-stu-id="3c5df-129">No</span></span>                   | <span data-ttu-id="3c5df-130">Показывать только текст.</span><span class="sxs-lookup"><span data-stu-id="3c5df-130">Show text only.</span></span>     |
| <span data-ttu-id="3c5df-131">Нет</span><span class="sxs-lookup"><span data-stu-id="3c5df-131">No</span></span>                          | <span data-ttu-id="3c5df-132">Нет</span><span class="sxs-lookup"><span data-stu-id="3c5df-132">No</span></span>                   | <span data-ttu-id="3c5df-133">Показывать только текст</span><span class="sxs-lookup"><span data-stu-id="3c5df-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="3c5df-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3c5df-134">Requirements</span></span>



| <span data-ttu-id="3c5df-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3c5df-135">Requirement</span></span> | <span data-ttu-id="3c5df-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3c5df-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5df-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c5df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5df-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c5df-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c5df-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c5df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5df-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c5df-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c5df-141">Header</span><span class="sxs-lookup"><span data-stu-id="3c5df-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c5df-142"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c5df-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c5df-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c5df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5df-144">**BM, \_ образ**</span><span class="sxs-lookup"><span data-stu-id="3c5df-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





