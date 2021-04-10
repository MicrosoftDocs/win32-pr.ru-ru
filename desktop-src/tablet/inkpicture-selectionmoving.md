---
description: Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Событие InkPicture. Селектионмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081453"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="87ef3-103">Событие InkPicture. Селектионмовинг</span><span class="sxs-lookup"><span data-stu-id="87ef3-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="87ef3-104">Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="87ef3-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ef3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87ef3-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="87ef3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87ef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ef3-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87ef3-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ef3-108">Прямоугольник, в который перемещается выделение после события **селектионмовинг** .</span><span class="sxs-lookup"><span data-stu-id="87ef3-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="87ef3-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="87ef3-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ef3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87ef3-110">Return value</span></span>

<span data-ttu-id="87ef3-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="87ef3-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ef3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87ef3-112">Remarks</span></span>

<span data-ttu-id="87ef3-113">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионмовинг.</span><span class="sxs-lookup"><span data-stu-id="87ef3-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ef3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="87ef3-114">Requirements</span></span>



| <span data-ttu-id="87ef3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="87ef3-115">Requirement</span></span> | <span data-ttu-id="87ef3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="87ef3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ef3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87ef3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87ef3-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87ef3-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="87ef3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87ef3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87ef3-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87ef3-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="87ef3-121">Header</span><span class="sxs-lookup"><span data-stu-id="87ef3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ef3-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87ef3-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87ef3-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87ef3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="87ef3-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ef3-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="87ef3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87ef3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ef3-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="87ef3-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="87ef3-127">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="87ef3-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="87ef3-128">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="87ef3-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




