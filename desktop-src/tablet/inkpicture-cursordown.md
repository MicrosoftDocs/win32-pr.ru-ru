---
description: Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Событие InkPicture. Курсордовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546554"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="b6f2d-103">Событие InkPicture. Курсордовн</span><span class="sxs-lookup"><span data-stu-id="b6f2d-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="b6f2d-104">Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="b6f2d-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6f2d-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="b6f2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6f2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f2d-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6f2d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2d-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсордовн** .</span><span class="sxs-lookup"><span data-stu-id="b6f2d-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="b6f2d-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6f2d-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2d-110">Объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , который был запущен, когда объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) привел к срабатыванию события **курсордовн** .</span><span class="sxs-lookup"><span data-stu-id="b6f2d-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f2d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6f2d-111">Return value</span></span>

<span data-ttu-id="b6f2d-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b6f2d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f2d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6f2d-113">Remarks</span></span>

<span data-ttu-id="b6f2d-114">Эти методы событий определены в интерфейсах **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="b6f2d-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="b6f2d-115">Интерфейсы **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** реализуют интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ицекурсордовн.</span><span class="sxs-lookup"><span data-stu-id="b6f2d-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="b6f2d-116">Используйте это событие осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.</span><span class="sxs-lookup"><span data-stu-id="b6f2d-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="b6f2d-117">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="b6f2d-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f2d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b6f2d-118">Requirements</span></span>



| <span data-ttu-id="b6f2d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b6f2d-119">Requirement</span></span> | <span data-ttu-id="b6f2d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b6f2d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f2d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6f2d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f2d-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b6f2d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b6f2d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6f2d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f2d-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6f2d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b6f2d-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6f2d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6f2d-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b6f2d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6f2d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6f2d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b6f2d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6f2d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f2d-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b6f2d-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b6f2d-131">**Событие Курсорбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="b6f2d-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b6f2d-132">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="b6f2d-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="b6f2d-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="b6f2d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b6f2d-134">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="b6f2d-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

