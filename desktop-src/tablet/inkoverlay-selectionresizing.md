---
description: Событие InkOverlay. Селектионресизинг — происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Событие InkOverlay. Селектионресизинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b5577f83c14ccc2e998fb4257344729e2219a2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086682"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="c0390-103">Событие InkOverlay. Селектионресизинг</span><span class="sxs-lookup"><span data-stu-id="c0390-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="c0390-104">Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="c0390-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0390-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0390-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="c0390-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0390-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0390-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0390-108">Ограничивающий прямоугольник выделения после события **селектионресизинг** .</span><span class="sxs-lookup"><span data-stu-id="c0390-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="c0390-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="c0390-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0390-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0390-110">Return value</span></span>

<span data-ttu-id="c0390-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c0390-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0390-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0390-112">Remarks</span></span>

<span data-ttu-id="c0390-113">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектионресизинг.</span><span class="sxs-lookup"><span data-stu-id="c0390-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0390-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c0390-114">Requirements</span></span>



| <span data-ttu-id="c0390-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c0390-115">Requirement</span></span> | <span data-ttu-id="c0390-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0390-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0390-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0390-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0390-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c0390-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c0390-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0390-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0390-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0390-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c0390-121">Header</span><span class="sxs-lookup"><span data-stu-id="c0390-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0390-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c0390-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c0390-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0390-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0390-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0390-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c0390-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c0390-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0390-126">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="c0390-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c0390-127">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="c0390-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="c0390-128">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="c0390-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




