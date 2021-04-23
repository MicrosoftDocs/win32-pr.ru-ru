---
description: Происходит при изменении выделения рукописного ввода внутри элемента управления InkPicture, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Событие InkPicture. Селектиончангинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912907"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="1c1dc-103">Событие InkPicture. Селектиончангинг</span><span class="sxs-lookup"><span data-stu-id="1c1dc-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="1c1dc-104">Происходит при изменении выделения рукописного ввода внутри элемента управления [InkPicture](inkpicture-control-reference.md) , например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="1c1dc-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c1dc-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="1c1dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c1dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1dc-107">*Невселектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c1dc-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1dc-108">Новая коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которая выбрана.</span><span class="sxs-lookup"><span data-stu-id="1c1dc-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1dc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c1dc-109">Return value</span></span>

<span data-ttu-id="1c1dc-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1c1dc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c1dc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c1dc-111">Remarks</span></span>

<span data-ttu-id="1c1dc-112">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектиончангинг.</span><span class="sxs-lookup"><span data-stu-id="1c1dc-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1dc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1c1dc-113">Requirements</span></span>



| <span data-ttu-id="1c1dc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1c1dc-114">Requirement</span></span> | <span data-ttu-id="1c1dc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1c1dc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1dc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c1dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1dc-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c1dc-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1c1dc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c1dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1dc-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c1dc-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1c1dc-120">Header</span><span class="sxs-lookup"><span data-stu-id="1c1dc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1dc-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c1dc-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c1dc-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c1dc-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c1dc-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1dc-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1c1dc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c1dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1dc-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1c1dc-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="1c1dc-126">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="1c1dc-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

