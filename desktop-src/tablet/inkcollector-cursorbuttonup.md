---
description: Происходит, когда InkCollector обнаруживает кнопку курсора, которая находится в up.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Событие InkCollector. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701373"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="a4724-103">Событие InkCollector. Курсорбуттонуп</span><span class="sxs-lookup"><span data-stu-id="a4724-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="a4724-104">Происходит, когда [**InkCollector**](inkcollector-class.md) обнаруживает кнопку курсора, которая находится в up.</span><span class="sxs-lookup"><span data-stu-id="a4724-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4724-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4724-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="a4724-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4724-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4724-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4724-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4724-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="a4724-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="a4724-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4724-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4724-110">Кнопка, которая была выпущена.</span><span class="sxs-lookup"><span data-stu-id="a4724-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4724-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4724-111">Return value</span></span>

<span data-ttu-id="a4724-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a4724-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4724-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4724-113">Remarks</span></span>

<span data-ttu-id="a4724-114">Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="a4724-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="a4724-115">Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.</span><span class="sxs-lookup"><span data-stu-id="a4724-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="a4724-116">Когда вы отпустите правую кнопку мыши, вы получаете два события **курсорбуттонуп** : одно для правой кнопки вверх, а другое — для кнопки слева.</span><span class="sxs-lookup"><span data-stu-id="a4724-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="a4724-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсорбуттонуп.</span><span class="sxs-lookup"><span data-stu-id="a4724-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4724-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a4724-118">Requirements</span></span>



| <span data-ttu-id="a4724-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a4724-119">Requirement</span></span> | <span data-ttu-id="a4724-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a4724-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4724-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4724-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4724-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a4724-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a4724-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4724-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4724-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a4724-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a4724-125">Header</span><span class="sxs-lookup"><span data-stu-id="a4724-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4724-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a4724-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a4724-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4724-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4724-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4724-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a4724-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4724-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4724-130">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="a4724-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a4724-131">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="a4724-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="a4724-132">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="a4724-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="a4724-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="a4724-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="a4724-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="a4724-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




