---
description: Событие InkOverlay. Курсорбуттонуп — происходит, когда InkCollector обнаруживает, что кнопка курсора находится в установленном положении.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Событие InkOverlay. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086852"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="5e5c2-103">Событие InkOverlay. Курсорбуттонуп</span><span class="sxs-lookup"><span data-stu-id="5e5c2-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="5e5c2-104">Происходит, когда [**InkCollector**](inkcollector-class.md) обнаруживает кнопку курсора, которая находится в up.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e5c2-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="5e5c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e5c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5c2-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e5c2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5c2-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5c2-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="5e5c2-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e5c2-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5c2-110">Кнопка, которая была выпущена.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5c2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e5c2-111">Return value</span></span>

<span data-ttu-id="5e5c2-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5c2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="5e5c2-113">Remarks</span></span>

<span data-ttu-id="5e5c2-114">Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="5e5c2-115">Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="5e5c2-116">Когда вы отпустите правую кнопку мыши, вы получаете два события [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) : одно для правой кнопки вверх, а другое — для кнопки слева.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="5e5c2-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсорбуттонуп.</span><span class="sxs-lookup"><span data-stu-id="5e5c2-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5c2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5e5c2-118">Requirements</span></span>



| <span data-ttu-id="5e5c2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5e5c2-119">Requirement</span></span> | <span data-ttu-id="5e5c2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5e5c2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5c2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e5c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5c2-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5e5c2-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5e5c2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e5c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5c2-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5e5c2-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5e5c2-125">Header</span><span class="sxs-lookup"><span data-stu-id="5e5c2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e5c2-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c2-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5e5c2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e5c2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e5c2-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c2-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5e5c2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5e5c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5c2-130">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5e5c2-131">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="5e5c2-132">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="5e5c2-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5e5c2-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




