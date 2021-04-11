---
description: Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Событие InkOverlay. Селектионресизед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272311"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="82004-103">Событие InkOverlay. Селектионресизед</span><span class="sxs-lookup"><span data-stu-id="82004-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="82004-104">Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="82004-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="82004-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82004-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="82004-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82004-107">*Олдселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82004-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82004-108">Ограничивающий прямоугольник выбранной коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , который существовал до запуска события **селектионресизед** .</span><span class="sxs-lookup"><span data-stu-id="82004-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="82004-109">Этот прямоугольник задается в координатах области рукописного ввода, что позволяет выполнять сценарии отмены.</span><span class="sxs-lookup"><span data-stu-id="82004-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82004-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82004-110">Return value</span></span>

<span data-ttu-id="82004-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82004-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82004-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82004-112">Remarks</span></span>

<span data-ttu-id="82004-113">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектионресизед.</span><span class="sxs-lookup"><span data-stu-id="82004-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="82004-114">Требования</span><span class="sxs-lookup"><span data-stu-id="82004-114">Requirements</span></span>



| <span data-ttu-id="82004-115">Требование</span><span class="sxs-lookup"><span data-stu-id="82004-115">Requirement</span></span> | <span data-ttu-id="82004-116">Значение</span><span class="sxs-lookup"><span data-stu-id="82004-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82004-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82004-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82004-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="82004-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="82004-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82004-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82004-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="82004-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="82004-121">Header</span><span class="sxs-lookup"><span data-stu-id="82004-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="82004-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="82004-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82004-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82004-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="82004-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82004-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="82004-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82004-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82004-126">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="82004-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="82004-127">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="82004-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="82004-128">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="82004-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

