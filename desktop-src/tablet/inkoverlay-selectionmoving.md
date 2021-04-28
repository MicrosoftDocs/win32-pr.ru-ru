---
description: Событие InkOverlay. Селектионмовинг — происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Событие InkOverlay. Селектионмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee4784e6b4c475c30d9b2a3ab30fe166ea3d67d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086702"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="118dd-103">Событие InkOverlay. Селектионмовинг</span><span class="sxs-lookup"><span data-stu-id="118dd-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="118dd-104">Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="118dd-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="118dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="118dd-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="118dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="118dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118dd-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="118dd-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="118dd-108">Прямоугольник, в который перемещается выделение после события **селектионмовинг** .</span><span class="sxs-lookup"><span data-stu-id="118dd-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="118dd-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="118dd-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118dd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="118dd-110">Return value</span></span>

<span data-ttu-id="118dd-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="118dd-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="118dd-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="118dd-112">Remarks</span></span>

<span data-ttu-id="118dd-113">Этот метод события определен в \_ \_ интерфейсах диспетчеризации (DISP) иинковерлайевентс и ИИНКПИКТУРИВЕНТС с идентификатором DISPID \_ иоеселектионмовинг.</span><span class="sxs-lookup"><span data-stu-id="118dd-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="118dd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="118dd-114">Requirements</span></span>



| <span data-ttu-id="118dd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="118dd-115">Requirement</span></span> | <span data-ttu-id="118dd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="118dd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="118dd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="118dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="118dd-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="118dd-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="118dd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="118dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="118dd-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="118dd-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="118dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="118dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="118dd-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="118dd-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="118dd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="118dd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="118dd-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="118dd-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="118dd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="118dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118dd-126">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="118dd-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="118dd-127">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="118dd-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="118dd-128">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="118dd-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="118dd-129">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="118dd-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




