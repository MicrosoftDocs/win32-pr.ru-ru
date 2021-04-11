---
description: Происходит при движении колесика мыши, когда элемент управления InkPicture имеет фокус.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Событие InkPicture. Маусевхил (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346112"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="d3839-103">Событие InkPicture. Маусевхил</span><span class="sxs-lookup"><span data-stu-id="d3839-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="d3839-104">Происходит при движении колесика мыши, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="d3839-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3839-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3839-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d3839-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3839-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3839-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3839-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-108">Нажатая кнопка.</span><span class="sxs-lookup"><span data-stu-id="d3839-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d3839-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3839-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d3839-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d3839-111">*Дельта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3839-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-112">Расстояние, которое было включено колесиком мыши.</span><span class="sxs-lookup"><span data-stu-id="d3839-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="d3839-113">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d3839-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-114">Координата x (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="d3839-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3839-115">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d3839-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-116">Координата по оси y (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="d3839-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3839-117">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3839-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3839-118">ВАРИАНТ \_ true, чтобы отменить событие **маусевхил** для родительского элемента управления; в противном случае — значение Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="d3839-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3839-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3839-119">Return value</span></span>

<span data-ttu-id="d3839-120">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3839-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3839-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3839-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3839-122">Параметры *x* и *y* задаются в пикселях, а не в HIMETRIC единицах, связанных с системой координат рукописного пространства.</span><span class="sxs-lookup"><span data-stu-id="d3839-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="d3839-123">Это связано с тем, что это событие заменяет связанное событие мыши приложения, которое не поддерживает перо, и этот тип приложения относится только к пикселям.</span><span class="sxs-lookup"><span data-stu-id="d3839-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="d3839-124">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="d3839-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="d3839-125">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипемаусевхил.</span><span class="sxs-lookup"><span data-stu-id="d3839-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3839-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d3839-126">Requirements</span></span>



| <span data-ttu-id="d3839-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d3839-127">Requirement</span></span> | <span data-ttu-id="d3839-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d3839-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3839-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3839-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d3839-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d3839-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d3839-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3839-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d3839-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d3839-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d3839-133">Header</span><span class="sxs-lookup"><span data-stu-id="d3839-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3839-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d3839-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3839-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3839-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3839-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3839-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d3839-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3839-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3839-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d3839-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

