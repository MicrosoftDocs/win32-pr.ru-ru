---
description: Событие InkPicture. Селектионмовинг — происходит, когда расположение текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Событие InkPicture. Селектионмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee50fe1115ce72dff0674ad4e6c2457500c7de8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086462"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="1c50e-103">Событие InkPicture. Селектионмовинг</span><span class="sxs-lookup"><span data-stu-id="1c50e-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="1c50e-104">Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="1c50e-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c50e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c50e-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="1c50e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c50e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c50e-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c50e-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c50e-108">Прямоугольник, в который перемещается выделение после события **селектионмовинг** .</span><span class="sxs-lookup"><span data-stu-id="1c50e-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="1c50e-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="1c50e-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c50e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c50e-110">Return value</span></span>

<span data-ttu-id="1c50e-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1c50e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c50e-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="1c50e-112">Remarks</span></span>

<span data-ttu-id="1c50e-113">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионмовинг.</span><span class="sxs-lookup"><span data-stu-id="1c50e-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c50e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1c50e-114">Requirements</span></span>



| <span data-ttu-id="1c50e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1c50e-115">Requirement</span></span> | <span data-ttu-id="1c50e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1c50e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c50e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c50e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c50e-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c50e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1c50e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c50e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c50e-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c50e-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1c50e-121">Header</span><span class="sxs-lookup"><span data-stu-id="1c50e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c50e-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c50e-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c50e-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c50e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c50e-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c50e-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1c50e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1c50e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c50e-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1c50e-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="1c50e-127">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="1c50e-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="1c50e-128">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="1c50e-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




