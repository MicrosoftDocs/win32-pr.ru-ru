---
description: Происходит, когда InkCollector обнаруживает кнопку курсора, которая находится в up.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Событие InkPicture. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6dbee586b3179f35593c95c2d62109a379c3216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912344"
---
# <a name="inkpicturecursorbuttonup-event"></a><span data-ttu-id="700a3-103">Событие InkPicture. Курсорбуттонуп</span><span class="sxs-lookup"><span data-stu-id="700a3-103">InkPicture.CursorButtonUp event</span></span>

<span data-ttu-id="700a3-104">Происходит, когда [**InkCollector**](inkcollector-class.md) обнаруживает кнопку курсора, которая находится в up.</span><span class="sxs-lookup"><span data-stu-id="700a3-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="700a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="700a3-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="700a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="700a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700a3-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="700a3-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700a3-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="700a3-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="700a3-109">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="700a3-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700a3-110">Кнопка, которая была выпущена.</span><span class="sxs-lookup"><span data-stu-id="700a3-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="700a3-111">Return value</span></span>

<span data-ttu-id="700a3-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="700a3-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="700a3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="700a3-113">Remarks</span></span>

<span data-ttu-id="700a3-114">Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="700a3-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="700a3-115">Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.</span><span class="sxs-lookup"><span data-stu-id="700a3-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="700a3-116">Когда вы отпустите правую кнопку мыши, вы получаете два события **курсорбуттонуп** : одно для правой кнопки вверх, а другое — для кнопки слева.</span><span class="sxs-lookup"><span data-stu-id="700a3-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="700a3-117">Этот метод события определен в DISP-интерфейсах **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсорбуттонуп.</span><span class="sxs-lookup"><span data-stu-id="700a3-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="700a3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="700a3-118">Requirements</span></span>



| <span data-ttu-id="700a3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="700a3-119">Requirement</span></span> | <span data-ttu-id="700a3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="700a3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="700a3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="700a3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="700a3-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="700a3-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="700a3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="700a3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="700a3-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="700a3-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="700a3-125">Header</span><span class="sxs-lookup"><span data-stu-id="700a3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="700a3-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="700a3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="700a3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="700a3-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="700a3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="700a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700a3-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="700a3-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="700a3-131">**Событие Курсорбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="700a3-131">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="700a3-132">**Событие Курсордовн**</span><span class="sxs-lookup"><span data-stu-id="700a3-132">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="700a3-133">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="700a3-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="700a3-134">**Интерфейс Иинккурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="700a3-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




