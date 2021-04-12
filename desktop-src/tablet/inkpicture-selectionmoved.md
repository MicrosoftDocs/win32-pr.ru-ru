---
description: Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Событие InkPicture. Селектионмовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346875"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="092f9-103">Событие InkPicture. Селектионмовед</span><span class="sxs-lookup"><span data-stu-id="092f9-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="092f9-104">Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="092f9-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="092f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="092f9-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="092f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="092f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092f9-107">*Олдселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="092f9-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="092f9-108">Ограничивающий прямоугольник выбранной коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , который существовал до запуска события **селектионмовед** .</span><span class="sxs-lookup"><span data-stu-id="092f9-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="092f9-109">Этот прямоугольник задается в координатах области рукописного ввода, что позволяет выполнять сценарии отмены.</span><span class="sxs-lookup"><span data-stu-id="092f9-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092f9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="092f9-110">Return value</span></span>

<span data-ttu-id="092f9-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="092f9-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="092f9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="092f9-112">Remarks</span></span>

<span data-ttu-id="092f9-113">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионмовед.</span><span class="sxs-lookup"><span data-stu-id="092f9-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="092f9-114">Чтобы получить новый ограничивающий прямоугольник коллекции штрихов, которые были перемещены, вызовите метод [**Selection. жетбаундингбокс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="092f9-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="092f9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="092f9-115">Requirements</span></span>



| <span data-ttu-id="092f9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="092f9-116">Requirement</span></span> | <span data-ttu-id="092f9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="092f9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092f9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="092f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="092f9-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="092f9-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="092f9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="092f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="092f9-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="092f9-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="092f9-122">Header</span><span class="sxs-lookup"><span data-stu-id="092f9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="092f9-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="092f9-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="092f9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="092f9-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="092f9-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="092f9-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="092f9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="092f9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092f9-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="092f9-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="092f9-128">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="092f9-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="092f9-129">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="092f9-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

