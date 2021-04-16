---
description: Происходит при отпускании кнопки мыши при перемещении указателя мыши над элементом управления InkPicture.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Событие InkPicture. MouseUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712215"
---
# <a name="inkpicturemouseup-event"></a><span data-ttu-id="3c707-103">Событие InkPicture. MouseUp</span><span class="sxs-lookup"><span data-stu-id="3c707-103">InkPicture.MouseUp event</span></span>

<span data-ttu-id="3c707-104">Происходит при отпускании кнопки мыши при перемещении указателя мыши над элементом управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3c707-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c707-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c707-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3c707-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c707-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c707-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c707-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c707-108">Нажатая кнопка.</span><span class="sxs-lookup"><span data-stu-id="3c707-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="3c707-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c707-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c707-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3c707-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="3c707-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c707-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c707-112">Координата x (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="3c707-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c707-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="3c707-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c707-114">Координата по оси y (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="3c707-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c707-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3c707-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c707-116">**Вариант \_ Значение TRUE** , чтобы отменить событие MouseUp для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="3c707-116">**VARIANT\_TRUE** to cancel the MouseUp event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c707-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c707-117">Return value</span></span>

<span data-ttu-id="3c707-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3c707-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c707-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c707-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c707-120">Параметры *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с системой координат рукописного пространства.</span><span class="sxs-lookup"><span data-stu-id="3c707-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="3c707-121">Это связано с тем, что это событие заменяет связанное событие мыши приложения, которое не поддерживает перо, и этот тип приложения относится только к пикселям.</span><span class="sxs-lookup"><span data-stu-id="3c707-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="3c707-122">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)и **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="3c707-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="3c707-123">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="3c707-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="3c707-124">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="3c707-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="3c707-125">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипемауседовн.</span><span class="sxs-lookup"><span data-stu-id="3c707-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c707-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3c707-126">Requirements</span></span>



| <span data-ttu-id="3c707-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3c707-127">Requirement</span></span> | <span data-ttu-id="3c707-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3c707-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c707-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c707-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c707-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3c707-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3c707-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c707-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c707-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3c707-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3c707-133">Header</span><span class="sxs-lookup"><span data-stu-id="3c707-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c707-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c707-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c707-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c707-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c707-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c707-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3c707-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c707-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c707-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3c707-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

