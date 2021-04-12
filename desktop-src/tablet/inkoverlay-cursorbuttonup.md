---
description: Происходит, когда InkCollector обнаруживает кнопку курсора, которая находится в up.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Событие InkOverlay. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348675"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="17c3d-103">Событие InkOverlay. Курсорбуттонуп</span><span class="sxs-lookup"><span data-stu-id="17c3d-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="17c3d-104">Происходит, когда [**InkCollector**](inkcollector-class.md) обнаруживает кнопку курсора, которая находится в up.</span><span class="sxs-lookup"><span data-stu-id="17c3d-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17c3d-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="17c3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17c3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c3d-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17c3d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c3d-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="17c3d-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="17c3d-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17c3d-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c3d-110">Кнопка, которая была выпущена.</span><span class="sxs-lookup"><span data-stu-id="17c3d-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c3d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17c3d-111">Return value</span></span>

<span data-ttu-id="17c3d-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="17c3d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c3d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17c3d-113">Remarks</span></span>

<span data-ttu-id="17c3d-114">Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="17c3d-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="17c3d-115">Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.</span><span class="sxs-lookup"><span data-stu-id="17c3d-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="17c3d-116">Когда вы отпустите правую кнопку мыши, вы получаете два события [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) : одно для правой кнопки вверх, а другое — для кнопки слева.</span><span class="sxs-lookup"><span data-stu-id="17c3d-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="17c3d-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсорбуттонуп.</span><span class="sxs-lookup"><span data-stu-id="17c3d-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c3d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="17c3d-118">Requirements</span></span>



| <span data-ttu-id="17c3d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="17c3d-119">Requirement</span></span> | <span data-ttu-id="17c3d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="17c3d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c3d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17c3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="17c3d-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="17c3d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="17c3d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17c3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="17c3d-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="17c3d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="17c3d-125">Header</span><span class="sxs-lookup"><span data-stu-id="17c3d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="17c3d-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17c3d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17c3d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17c3d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="17c3d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17c3d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="17c3d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17c3d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c3d-130">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="17c3d-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="17c3d-131">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="17c3d-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="17c3d-132">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="17c3d-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="17c3d-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="17c3d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="17c3d-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="17c3d-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




