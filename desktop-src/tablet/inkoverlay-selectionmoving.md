---
description: Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Событие InkOverlay. Селектионмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702861"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="ce75a-103">Событие InkOverlay. Селектионмовинг</span><span class="sxs-lookup"><span data-stu-id="ce75a-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="ce75a-104">Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="ce75a-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce75a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce75a-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="ce75a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce75a-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce75a-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce75a-108">Прямоугольник, в который перемещается выделение после события **селектионмовинг** .</span><span class="sxs-lookup"><span data-stu-id="ce75a-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="ce75a-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="ce75a-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce75a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce75a-110">Return value</span></span>

<span data-ttu-id="ce75a-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ce75a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce75a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce75a-112">Remarks</span></span>

<span data-ttu-id="ce75a-113">Этот метод события определен в \_ \_ интерфейсах диспетчеризации (DISP) иинковерлайевентс и ИИНКПИКТУРИВЕНТС с идентификатором DISPID \_ иоеселектионмовинг.</span><span class="sxs-lookup"><span data-stu-id="ce75a-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce75a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ce75a-114">Requirements</span></span>



| <span data-ttu-id="ce75a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ce75a-115">Requirement</span></span> | <span data-ttu-id="ce75a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ce75a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce75a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce75a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce75a-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ce75a-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ce75a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce75a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce75a-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce75a-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ce75a-121">Header</span><span class="sxs-lookup"><span data-stu-id="ce75a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce75a-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ce75a-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce75a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce75a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce75a-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce75a-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ce75a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce75a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce75a-126">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ce75a-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="ce75a-127">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ce75a-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="ce75a-128">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="ce75a-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="ce75a-129">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="ce75a-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




