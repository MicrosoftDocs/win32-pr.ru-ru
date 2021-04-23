---
description: Происходит при удалении одного или нескольких штрихов из коллекции Инкстрокес.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Событие Инкстрокес. Строкесремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349892"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="230ca-103">Инкстрокес. Строкесремовед, событие</span><span class="sxs-lookup"><span data-stu-id="230ca-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="230ca-104">Происходит при удалении одного или нескольких штрихов из коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="230ca-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="230ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="230ca-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="230ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="230ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230ca-107">*Строкеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="230ca-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230ca-108">Целочисленный массив идентификаторов для каждого объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , удаляемого при возникновении этого события.</span><span class="sxs-lookup"><span data-stu-id="230ca-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="230ca-109">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="230ca-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230ca-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="230ca-110">Return value</span></span>

<span data-ttu-id="230ca-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="230ca-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="230ca-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="230ca-112">Remarks</span></span>

<span data-ttu-id="230ca-113">Этот метод события определен в \_ интерфейсе иинкевентс.</span><span class="sxs-lookup"><span data-stu-id="230ca-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="230ca-114">\_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ сестрокесремовед.</span><span class="sxs-lookup"><span data-stu-id="230ca-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="230ca-115">Требования</span><span class="sxs-lookup"><span data-stu-id="230ca-115">Requirements</span></span>



| <span data-ttu-id="230ca-116">Требование</span><span class="sxs-lookup"><span data-stu-id="230ca-116">Requirement</span></span> | <span data-ttu-id="230ca-117">Значение</span><span class="sxs-lookup"><span data-stu-id="230ca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="230ca-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="230ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="230ca-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="230ca-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="230ca-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="230ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="230ca-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="230ca-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="230ca-122">Header</span><span class="sxs-lookup"><span data-stu-id="230ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="230ca-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="230ca-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="230ca-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="230ca-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="230ca-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230ca-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="230ca-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="230ca-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="230ca-127">[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="230ca-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="230ca-128">[**Удалить метод \[ Инкстрокес Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="230ca-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="230ca-129">**Класс Инкдисп**</span><span class="sxs-lookup"><span data-stu-id="230ca-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

