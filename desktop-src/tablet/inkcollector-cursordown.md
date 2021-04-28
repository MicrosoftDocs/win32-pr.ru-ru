---
description: Событие InkCollector. Курсордовн — происходит, когда подсказка курсора обращается к планшету с дигитайзером.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Событие InkCollector. Курсордовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110302"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="23877-103">Событие InkCollector. Курсордовн</span><span class="sxs-lookup"><span data-stu-id="23877-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="23877-104">Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="23877-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="23877-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23877-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="23877-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23877-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23877-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23877-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсордовн** .</span><span class="sxs-lookup"><span data-stu-id="23877-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="23877-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23877-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23877-110">Объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , который был запущен, когда объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) привел к срабатыванию события **курсордовн** .</span><span class="sxs-lookup"><span data-stu-id="23877-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23877-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23877-111">Return value</span></span>

<span data-ttu-id="23877-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="23877-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23877-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="23877-113">Remarks</span></span>

<span data-ttu-id="23877-114">Этот метод события определен в \_ иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс.</span><span class="sxs-lookup"><span data-stu-id="23877-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="23877-115">\_интерфейсы иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс реализуют интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ицекурсордовн.</span><span class="sxs-lookup"><span data-stu-id="23877-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="23877-116">Используйте это событие осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.</span><span class="sxs-lookup"><span data-stu-id="23877-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="23877-117">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="23877-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="23877-118">Требования</span><span class="sxs-lookup"><span data-stu-id="23877-118">Requirements</span></span>



| <span data-ttu-id="23877-119">Требование</span><span class="sxs-lookup"><span data-stu-id="23877-119">Requirement</span></span> | <span data-ttu-id="23877-120">Значение</span><span class="sxs-lookup"><span data-stu-id="23877-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23877-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23877-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23877-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23877-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="23877-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23877-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23877-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23877-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="23877-125">Header</span><span class="sxs-lookup"><span data-stu-id="23877-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23877-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23877-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="23877-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23877-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="23877-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23877-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="23877-129">См. также</span><span class="sxs-lookup"><span data-stu-id="23877-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23877-130">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="23877-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="23877-131">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="23877-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="23877-132">**Событие Курсорбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="23877-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="23877-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="23877-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="23877-134">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="23877-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

