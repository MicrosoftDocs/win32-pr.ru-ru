---
description: Происходит, когда пользователь отпускает ключ, когда элемент управления InkEdit имеет фокус.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Событие InkEdit. KeyUp (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546751"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="06299-103">Событие InkEdit. KeyUp</span><span class="sxs-lookup"><span data-stu-id="06299-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="06299-104">Происходит, когда пользователь отпускает ключ, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="06299-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="06299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06299-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="06299-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06299-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="06299-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="06299-108">Код виртуального ключа для клавиши, нажатой пользователем.</span><span class="sxs-lookup"><span data-stu-id="06299-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="06299-109">*шифткэй*</span><span class="sxs-lookup"><span data-stu-id="06299-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="06299-110">Член перечисления [**инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , указывающий, какие клавиши-модификаторы следует отменять во время события.</span><span class="sxs-lookup"><span data-stu-id="06299-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="06299-111">Значение</span><span class="sxs-lookup"><span data-stu-id="06299-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="06299-112">Значение</span><span class="sxs-lookup"><span data-stu-id="06299-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="06299-113"><dt>**ИКМ \_ SHIFT**</dt></span><span class="sxs-lookup"><span data-stu-id="06299-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="06299-114">Указывает, что клавиша SHIFT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="06299-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="06299-115"><dt>**ИКМ \_ Элемент управления**</dt></span><span class="sxs-lookup"><span data-stu-id="06299-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="06299-116">Указывает, что клавиша CTRL использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="06299-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="06299-117"><dt>**ИКМ \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="06299-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="06299-118">Указывает, что клавиша ALT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="06299-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06299-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06299-119">Return value</span></span>

<span data-ttu-id="06299-120">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="06299-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06299-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06299-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06299-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06299-122">Remarks</span></span>

<span data-ttu-id="06299-123">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="06299-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="06299-124">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйуп.</span><span class="sxs-lookup"><span data-stu-id="06299-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="06299-125">Требования</span><span class="sxs-lookup"><span data-stu-id="06299-125">Requirements</span></span>



| <span data-ttu-id="06299-126">Требование</span><span class="sxs-lookup"><span data-stu-id="06299-126">Requirement</span></span> | <span data-ttu-id="06299-127">Значение</span><span class="sxs-lookup"><span data-stu-id="06299-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06299-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06299-128">Minimum supported client</span></span><br/> | <span data-ttu-id="06299-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="06299-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06299-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06299-130">Minimum supported server</span></span><br/> | <span data-ttu-id="06299-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06299-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="06299-132">Header</span><span class="sxs-lookup"><span data-stu-id="06299-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="06299-133"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="06299-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="06299-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06299-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="06299-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06299-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="06299-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06299-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06299-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="06299-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="06299-138">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="06299-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="06299-139">[**\[Элемент управления InkEdit события KeyDown\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="06299-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="06299-140">[**\[Элемент управления InkEdit события KeyPress\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="06299-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

