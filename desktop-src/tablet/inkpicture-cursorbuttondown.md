---
description: Событие InkPicture. Курсорбуттондовн — возникает, когда класс InkCollector обнаруживает недоступную кнопку курсора.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Событие InkPicture. Курсорбуттондовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2017cd7dc2291bdb29aa01df3d94f20211b7cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116782"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="6d1ea-103">Событие InkPicture. Курсорбуттондовн</span><span class="sxs-lookup"><span data-stu-id="6d1ea-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="6d1ea-104">Происходит, когда [**класс InkCollector**](inkcollector-class.md) обнаруживает недоступную кнопку курсора.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d1ea-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="6d1ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d1ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d1ea-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d1ea-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1ea-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттондовн** .</span><span class="sxs-lookup"><span data-stu-id="6d1ea-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="6d1ea-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d1ea-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1ea-110">Нажатая кнопка.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d1ea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d1ea-111">Return value</span></span>

<span data-ttu-id="6d1ea-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d1ea-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="6d1ea-113">Remarks</span></span>

<span data-ttu-id="6d1ea-114">Кнопка в подсказке пера не работает, когда пользователь перемещает перо на дигитайзер и начинает трассировку штриха.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="6d1ea-115">Кнопка на элементе с назначением не работает при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="6d1ea-116">При нажатии правой кнопки мыши фактически появляется два события **курсорбуттондовн** : одна для нажатой правой кнопки, а другая для нажатой левой кнопки.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="6d1ea-117">Этот метод события определен в интерфейсе диспетчеризации **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсорбуттондовн.</span><span class="sxs-lookup"><span data-stu-id="6d1ea-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d1ea-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6d1ea-118">Requirements</span></span>



| <span data-ttu-id="6d1ea-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6d1ea-119">Requirement</span></span> | <span data-ttu-id="6d1ea-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6d1ea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1ea-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d1ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1ea-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6d1ea-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6d1ea-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d1ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1ea-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d1ea-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6d1ea-125">Header</span><span class="sxs-lookup"><span data-stu-id="6d1ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d1ea-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6d1ea-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6d1ea-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d1ea-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d1ea-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d1ea-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6d1ea-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6d1ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1ea-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6d1ea-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6d1ea-131">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="6d1ea-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="6d1ea-132">**Событие Курсорбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="6d1ea-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="6d1ea-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="6d1ea-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="6d1ea-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="6d1ea-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




