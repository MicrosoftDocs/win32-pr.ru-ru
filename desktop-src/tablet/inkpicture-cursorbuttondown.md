---
description: Происходит, когда класс InkCollector обнаруживает недоступную кнопку курсора.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Событие InkPicture. Курсорбуттондовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266153"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="64868-103">Событие InkPicture. Курсорбуттондовн</span><span class="sxs-lookup"><span data-stu-id="64868-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="64868-104">Происходит, когда [**класс InkCollector**](inkcollector-class.md) обнаруживает недоступную кнопку курсора.</span><span class="sxs-lookup"><span data-stu-id="64868-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="64868-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64868-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="64868-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64868-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64868-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64868-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттондовн** .</span><span class="sxs-lookup"><span data-stu-id="64868-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="64868-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64868-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64868-110">Нажатая кнопка.</span><span class="sxs-lookup"><span data-stu-id="64868-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64868-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64868-111">Return value</span></span>

<span data-ttu-id="64868-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="64868-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64868-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64868-113">Remarks</span></span>

<span data-ttu-id="64868-114">Кнопка в подсказке пера не работает, когда пользователь перемещает перо на дигитайзер и начинает трассировку штриха.</span><span class="sxs-lookup"><span data-stu-id="64868-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="64868-115">Кнопка на элементе с назначением не работает при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="64868-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="64868-116">При нажатии правой кнопки мыши фактически появляется два события **курсорбуттондовн** : одна для нажатой правой кнопки, а другая для нажатой левой кнопки.</span><span class="sxs-lookup"><span data-stu-id="64868-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="64868-117">Этот метод события определен в интерфейсе диспетчеризации **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсорбуттондовн.</span><span class="sxs-lookup"><span data-stu-id="64868-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="64868-118">Требования</span><span class="sxs-lookup"><span data-stu-id="64868-118">Requirements</span></span>



| <span data-ttu-id="64868-119">Требование</span><span class="sxs-lookup"><span data-stu-id="64868-119">Requirement</span></span> | <span data-ttu-id="64868-120">Значение</span><span class="sxs-lookup"><span data-stu-id="64868-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64868-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64868-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64868-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="64868-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="64868-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64868-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64868-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="64868-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="64868-125">Header</span><span class="sxs-lookup"><span data-stu-id="64868-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="64868-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64868-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64868-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64868-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="64868-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64868-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="64868-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64868-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64868-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="64868-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="64868-131">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="64868-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="64868-132">**Событие Курсорбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="64868-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="64868-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="64868-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="64868-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="64868-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




