---
description: Происходит, когда изменяется размер элемента управления InkPicture (при изменении значений свойств Width и/или Height).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Событие InkPicture. Resize (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081248"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="e7378-103">Событие InkPicture. Resize</span><span class="sxs-lookup"><span data-stu-id="e7378-103">InkPicture.Resize event</span></span>

<span data-ttu-id="e7378-104">Происходит, когда изменяется размер элемента управления [InkPicture](inkpicture-control-reference.md) (при изменении значений свойств Width и/или Height).</span><span class="sxs-lookup"><span data-stu-id="e7378-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7378-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7378-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="e7378-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7378-107">*Слева*</span><span class="sxs-lookup"><span data-stu-id="e7378-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="e7378-108">Число пикселей от левой стороны окна, которое содержит элемент управления слева от элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7378-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e7378-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="e7378-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="e7378-110">Число пикселей от верхнего края окна, которое содержит элемент управления в верхней части элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7378-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e7378-111">*Right*</span><span class="sxs-lookup"><span data-stu-id="e7378-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="e7378-112">Число пикселей от левой стороны окна, которое содержит элемент управления справа от элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7378-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e7378-113">*Нижнее*</span><span class="sxs-lookup"><span data-stu-id="e7378-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="e7378-114">Число пикселей от верхнего края окна, которое содержит элемент управления в нижней части элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7378-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7378-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7378-115">Return value</span></span>

<span data-ttu-id="e7378-116">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e7378-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7378-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7378-117">Remarks</span></span>

<span data-ttu-id="e7378-118">Новая ширина элемента управления в пикселях будет равна разности между параметрами *right* и *Left* .</span><span class="sxs-lookup"><span data-stu-id="e7378-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="e7378-119">Аналогичным образом Новая высота будет равна разности между *нижней* и *верхней границами*.</span><span class="sxs-lookup"><span data-stu-id="e7378-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="e7378-120">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="e7378-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e7378-121">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ ипересизе**.</span><span class="sxs-lookup"><span data-stu-id="e7378-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7378-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e7378-122">Requirements</span></span>



| <span data-ttu-id="e7378-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e7378-123">Requirement</span></span> | <span data-ttu-id="e7378-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e7378-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7378-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7378-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7378-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e7378-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e7378-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7378-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7378-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7378-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e7378-129">Header</span><span class="sxs-lookup"><span data-stu-id="e7378-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7378-130"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7378-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7378-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7378-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7378-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7378-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e7378-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7378-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7378-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e7378-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




