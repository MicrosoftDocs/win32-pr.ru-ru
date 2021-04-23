---
description: Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Событие InkPicture. Селектионресизинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999429"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="2e623-103">Событие InkPicture. Селектионресизинг</span><span class="sxs-lookup"><span data-stu-id="2e623-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="2e623-104">Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="2e623-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e623-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e623-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="2e623-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e623-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e623-107">*Курселектионрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e623-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e623-108">Ограничивающий прямоугольник выделения после события **селектионресизинг** .</span><span class="sxs-lookup"><span data-stu-id="2e623-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="2e623-109">Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="2e623-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e623-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e623-110">Return value</span></span>

<span data-ttu-id="2e623-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2e623-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e623-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e623-112">Remarks</span></span>

<span data-ttu-id="2e623-113">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионресизинг.</span><span class="sxs-lookup"><span data-stu-id="2e623-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e623-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2e623-114">Requirements</span></span>



| <span data-ttu-id="2e623-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2e623-115">Requirement</span></span> | <span data-ttu-id="2e623-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2e623-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e623-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e623-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e623-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e623-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2e623-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e623-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e623-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e623-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2e623-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e623-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e623-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e623-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e623-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e623-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2e623-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e623-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e623-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2e623-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="2e623-127">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="2e623-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="2e623-128">**Класс Инкректангле**</span><span class="sxs-lookup"><span data-stu-id="2e623-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




