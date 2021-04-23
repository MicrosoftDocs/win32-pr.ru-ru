---
description: Происходит при добавлении одного или нескольких объектов Иинкстрокедисп в коллекцию Инкстрокес.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Событие InkPicture. Строкесаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712494"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="1d0f8-103">Событие InkPicture. Строкесаддед</span><span class="sxs-lookup"><span data-stu-id="1d0f8-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="1d0f8-104">Происходит при добавлении одного или нескольких объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d0f8-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d0f8-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="1d0f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d0f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0f8-107">*Строкеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d0f8-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0f8-108">Целочисленный массив идентификаторов для каждого объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , добавляемого при возникновении этого события.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="1d0f8-109">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1d0f8-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0f8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d0f8-110">Return value</span></span>

<span data-ttu-id="1d0f8-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0f8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d0f8-112">Remarks</span></span>

<span data-ttu-id="1d0f8-113">Этот метод события определен в интерфейсе **\_ иинкстрокесевентс** .</span><span class="sxs-lookup"><span data-stu-id="1d0f8-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="1d0f8-114">Интерфейс **\_ иинкстрокесевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ сестрокесаддед.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0f8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1d0f8-115">Requirements</span></span>



| <span data-ttu-id="1d0f8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1d0f8-116">Requirement</span></span> | <span data-ttu-id="1d0f8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1d0f8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0f8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d0f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0f8-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1d0f8-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1d0f8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d0f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0f8-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d0f8-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1d0f8-122">Header</span><span class="sxs-lookup"><span data-stu-id="1d0f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d0f8-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1d0f8-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d0f8-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d0f8-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1d0f8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d0f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0f8-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1d0f8-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

