---
description: Происходит при добавлении штриха к объекту Инкдисп.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Событие Инкдисп. Инкаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072719"
---
# <a name="inkdispinkadded-event"></a><span data-ttu-id="5704f-103">Инкдисп. Инкаддед, событие</span><span class="sxs-lookup"><span data-stu-id="5704f-103">InkDisp.InkAdded event</span></span>

<span data-ttu-id="5704f-104">Происходит при добавлении штриха к объекту [**инкдисп**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5704f-104">Occurs when a stroke is added to the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5704f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5704f-105">Syntax</span></span>


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="5704f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5704f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5704f-107">*Строкеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5704f-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5704f-108">Целочисленный массив данных идентификатора штриха для всех штрихов, добавленных при возникновении этого события.</span><span class="sxs-lookup"><span data-stu-id="5704f-108">The integer array of stroke ID information for all of the strokes that have been added when this event occurs.</span></span>

<span data-ttu-id="5704f-109">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="5704f-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5704f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5704f-110">Return value</span></span>

<span data-ttu-id="5704f-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5704f-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5704f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5704f-112">Remarks</span></span>

<span data-ttu-id="5704f-113">Если вы используете объект [**InkOverlay**](inkoverlay-class.md) или элемент управления [InkPicture](inkpicture-control-reference.md) (где [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) равно [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) и [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) равно [**строкирасе**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) и передайте резинку по штриху, вы получаете следующую последовательность событий:</span><span class="sxs-lookup"><span data-stu-id="5704f-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   [<span data-ttu-id="5704f-114">**инкделетед**</span><span class="sxs-lookup"><span data-stu-id="5704f-114">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)
-   <span data-ttu-id="5704f-115">**инкаддед**</span><span class="sxs-lookup"><span data-stu-id="5704f-115">**InkAdded**</span></span>
-   [<span data-ttu-id="5704f-116">**инкделетед**</span><span class="sxs-lookup"><span data-stu-id="5704f-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)

<span data-ttu-id="5704f-117">Дополнительные события **инкаддед** и [**инкделетед**](inkdisp-inkdeleted.md) происходят потому, что базовый код добавляет внутренний невидимый росчерк для отслеживания ластика.</span><span class="sxs-lookup"><span data-stu-id="5704f-117">The additional **InkAdded** and [**InkDeleted**](inkdisp-inkdeleted.md) events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="5704f-118">Этот метод события определен в \_ интерфейсе иинкевентс.</span><span class="sxs-lookup"><span data-stu-id="5704f-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="5704f-119">\_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иеинкаддед.</span><span class="sxs-lookup"><span data-stu-id="5704f-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkAdded.</span></span>

<span data-ttu-id="5704f-120">Событие **инкаддед** срабатывает даже в режиме выбора или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="5704f-120">The **InkAdded** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="5704f-121">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="5704f-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="5704f-122">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="5704f-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="5704f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5704f-123">Requirements</span></span>



| <span data-ttu-id="5704f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5704f-124">Requirement</span></span> | <span data-ttu-id="5704f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5704f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5704f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5704f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5704f-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5704f-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5704f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5704f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5704f-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5704f-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5704f-130">Header</span><span class="sxs-lookup"><span data-stu-id="5704f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5704f-131"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5704f-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5704f-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5704f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5704f-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5704f-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5704f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5704f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5704f-135">**Класс Инкдисп**</span><span class="sxs-lookup"><span data-stu-id="5704f-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="5704f-136">[**\[Класс InkOverlay свойства EditingMode\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="5704f-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="5704f-137">[**\[Класс InkOverlay свойства ерасермоде\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="5704f-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="5704f-138">**Событие Инкделетед**</span><span class="sxs-lookup"><span data-stu-id="5704f-138">**InkDeleted Event**</span></span>](inkdisp-inkdeleted.md)
</dt> <dt>

[<span data-ttu-id="5704f-139">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="5704f-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5704f-140">Справочник по элементу управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="5704f-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5704f-141">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="5704f-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

