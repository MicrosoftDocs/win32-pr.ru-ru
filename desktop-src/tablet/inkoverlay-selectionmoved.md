---
description: Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Событие InkOverlay. Селектионмовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348665"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="fe04d-103">Событие InkOverlay. Селектионмовед</span><span class="sxs-lookup"><span data-stu-id="fe04d-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="fe04d-104">Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="fe04d-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe04d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe04d-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="fe04d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe04d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe04d-107">*Олдселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe04d-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe04d-108">Ограничивающий прямоугольник выбранной коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , который существовал до запуска события **селектионмовед** .</span><span class="sxs-lookup"><span data-stu-id="fe04d-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="fe04d-109">Этот прямоугольник задается в координатах области рукописного ввода, что позволяет выполнять сценарии отмены.</span><span class="sxs-lookup"><span data-stu-id="fe04d-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe04d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe04d-110">Return value</span></span>

<span data-ttu-id="fe04d-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fe04d-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe04d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe04d-112">Remarks</span></span>

<span data-ttu-id="fe04d-113">Метод события TЭтот определяется в \_ иинковерлайевентс и \_ иинкпиктуривентс интерфейсах диспетчеризации (DISP) с идентификатором DISPID \_ иоеселектионмовед.</span><span class="sxs-lookup"><span data-stu-id="fe04d-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="fe04d-114">Чтобы получить новый ограничивающий прямоугольник коллекции штрихов, которые были перемещены, вызовите метод [**Selection. жетбаундингбокс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="fe04d-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe04d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fe04d-115">Requirements</span></span>



| <span data-ttu-id="fe04d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fe04d-116">Requirement</span></span> | <span data-ttu-id="fe04d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fe04d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe04d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe04d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe04d-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe04d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fe04d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe04d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe04d-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe04d-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fe04d-122">Header</span><span class="sxs-lookup"><span data-stu-id="fe04d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe04d-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fe04d-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fe04d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe04d-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe04d-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe04d-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fe04d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe04d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe04d-127">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="fe04d-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="fe04d-128">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="fe04d-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="fe04d-129">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="fe04d-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

