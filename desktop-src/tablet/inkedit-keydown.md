---
description: Происходит, когда пользователь нажимает клавишу, когда элемент управления InkEdit имеет фокус.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Событие InkEdit. KeyDown (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999432"
---
# <a name="inkeditkeydown-event"></a><span data-ttu-id="e6d1b-103">Событие InkEdit. KeyDown</span><span class="sxs-lookup"><span data-stu-id="e6d1b-103">InkEdit.KeyDown event</span></span>

<span data-ttu-id="e6d1b-104">Происходит, когда пользователь нажимает клавишу, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-104">Occurs when the user presses a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6d1b-105">Syntax</span></span>


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="e6d1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6d1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d1b-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="e6d1b-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1b-108">Код виртуального ключа для клавиши, нажатой пользователем.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="e6d1b-109">*шифткэй*</span><span class="sxs-lookup"><span data-stu-id="e6d1b-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1b-110">Член перечисления [**инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , указывающий, какие клавиши-модификаторы следует отменять во время события.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration, that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="e6d1b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e6d1b-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="e6d1b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e6d1b-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="e6d1b-113"><dt>**ИКМ \_ SHIFT**</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1b-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="e6d1b-114">Указывает, что клавиша SHIFT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="e6d1b-115"><dt>**ИКМ \_ Элемент управления**</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1b-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="e6d1b-116">Указывает, что клавиша CTRL использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="e6d1b-117"><dt>**ИКМ \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1b-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="e6d1b-118">Указывает, что клавиша ALT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d1b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6d1b-119">Return value</span></span>

<span data-ttu-id="e6d1b-120">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6d1b-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6d1b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6d1b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6d1b-122">Remarks</span></span>

<span data-ttu-id="e6d1b-123">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="e6d1b-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="e6d1b-124">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйдовн.</span><span class="sxs-lookup"><span data-stu-id="e6d1b-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d1b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e6d1b-125">Requirements</span></span>



| <span data-ttu-id="e6d1b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e6d1b-126">Requirement</span></span> | <span data-ttu-id="e6d1b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e6d1b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d1b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6d1b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d1b-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e6d1b-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6d1b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6d1b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d1b-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6d1b-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e6d1b-132">Header</span><span class="sxs-lookup"><span data-stu-id="e6d1b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d1b-133"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1b-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e6d1b-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6d1b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6d1b-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1b-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e6d1b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6d1b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d1b-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="e6d1b-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e6d1b-138">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="e6d1b-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="e6d1b-139">[**\[Элемент управления InkEdit события KeyPress\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="e6d1b-139">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> <dt>

<span data-ttu-id="e6d1b-140">[**\[Элемент управления InkEdit для события KeyUp\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="e6d1b-140">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

