---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при изменении фокуса ввода до того, как объект Пенинпутпанел смог вставить входные данные пользователя в присоединенный элемент управления.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Событие Пенинпутпанел. Инпутфаилед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693724"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="d5fae-104">Пенинпутпанел. Инпутфаилед, событие</span><span class="sxs-lookup"><span data-stu-id="d5fae-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="d5fae-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d5fae-105">Deprecated.</span></span> <span data-ttu-id="d5fae-106">[**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d5fae-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="d5fae-107">Происходит при изменении фокуса ввода до того, как объект [**пенинпутпанел**](peninputpanel-class.md) смог вставить входные данные пользователя в присоединенный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5fae-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5fae-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="d5fae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5fae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5fae-110">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fae-111">Маркер окна элемента управления, вызвавшего объект [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fae-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d5fae-112">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fae-113">Виртуальный ключ, соответствующий нажатой клавише.</span><span class="sxs-lookup"><span data-stu-id="d5fae-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d5fae-114">*Текстовая надпись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fae-115">Строка, которая должна быть вставлена в элемент управления, представленный параметром *HWND* при возникновении события **инпутфаилед** .</span><span class="sxs-lookup"><span data-stu-id="d5fae-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="d5fae-116">Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d5fae-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fae-117">*Шифткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fae-118">Состояние модификаторов клавиатуры, включая SHIFT, CAPS, CTRL и ALT.</span><span class="sxs-lookup"><span data-stu-id="d5fae-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5fae-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5fae-119">Return value</span></span>

<span data-ttu-id="d5fae-120">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5fae-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5fae-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5fae-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fae-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5fae-122">Remarks</span></span>

<span data-ttu-id="d5fae-123">Событие **инпутфаилед** возникает при изменении фокуса ввода до вставки пользовательского ввода в присоединенный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5fae-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="d5fae-124">Например, если пользователь вводит рукописный ввод в панель рукописного ввода, а затем переключается на другой элемент управления "поле ввода" до того, как распознаватель уже готов, это событие срабатывает.</span><span class="sxs-lookup"><span data-stu-id="d5fae-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="d5fae-125">С помощью маркера окна, переданного в это событие, можно выбрать вставку текста самостоятельно при возникновении этого события.</span><span class="sxs-lookup"><span data-stu-id="d5fae-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="d5fae-126">Начиная с Microsoft Windows XP Tablet PC Edition 2005, событие **инпутфаилед** больше не применяется.</span><span class="sxs-lookup"><span data-stu-id="d5fae-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="d5fae-127">Текст всегда вставляется перед изменением фокуса.</span><span class="sxs-lookup"><span data-stu-id="d5fae-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5fae-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d5fae-128">Requirements</span></span>



| <span data-ttu-id="d5fae-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d5fae-129">Requirement</span></span> | <span data-ttu-id="d5fae-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d5fae-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fae-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5fae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fae-132">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5fae-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5fae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fae-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d5fae-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5fae-135">Header</span><span class="sxs-lookup"><span data-stu-id="d5fae-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5fae-136"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5fae-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5fae-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5fae-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5fae-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5fae-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5fae-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5fae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fae-140">**пенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="d5fae-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




