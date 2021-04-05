---
description: Задает шрифт, используемый элементом управления при рисовании текста.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Сообщение WM_SETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998570"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="fcc2d-103">\_Сообщение СЕТФОНТ WM</span><span class="sxs-lookup"><span data-stu-id="fcc2d-103">WM\_SETFONT message</span></span>

<span data-ttu-id="fcc2d-104">Задает шрифт, используемый элементом управления при рисовании текста.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="fcc2d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcc2d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc2d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcc2d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc2d-107">Маркер для шрифта (**хфонт**).</span><span class="sxs-lookup"><span data-stu-id="fcc2d-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="fcc2d-108">Если этот параметр имеет **значение NULL**, элемент управления использует системный шрифт по умолчанию для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="fcc2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcc2d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc2d-110">Слово *lParam* в низком порядке указывает, должен ли элемент управления перерисоваться сразу после установки шрифта.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="fcc2d-111">Если этот параметр имеет **значение true**, элемент управления перерисовывает сам себя.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc2d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcc2d-112">Return value</span></span>

<span data-ttu-id="fcc2d-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-113">Type: **LRESULT**</span></span>

<span data-ttu-id="fcc2d-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc2d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcc2d-115">Remarks</span></span>

<span data-ttu-id="fcc2d-116">Сообщение **WM \_ сетфонт** применяется ко всем элементам управления, а не только к тем, которые находятся в диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="fcc2d-117">Самое лучшее время, когда владелец элемента управления диалогового окна задает шрифт элемента управления, — когда он получает сообщение [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc2d-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="fcc2d-118">Приложение должно вызвать функцию [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) , чтобы удалить шрифт, когда он больше не нужен; Например, после уничтожения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="fcc2d-119">Размер элемента управления не изменяется в результате получения этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="fcc2d-120">Чтобы избежать усечения текста, который не умещается в границах элемента управления, приложение должно исправить размер окна элемента управления до того, как оно установит шрифт.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="fcc2d-121">Когда в диалоговом окне используется [стиль \_ сетфонт DS](../dlgbox/about-dialog-boxes.md) для задания текста в элементах управления, система перед созданием элементов управления отправляет сообщение **WM \_ сетфонт** в процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="fcc2d-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="fcc2d-122">Приложение может создать диалоговое окно, содержащее \_ стиль DS сетфонт, вызвав одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="fcc2d-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="fcc2d-123">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="fcc2d-124">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="fcc2d-125">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="fcc2d-126">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="fcc2d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fcc2d-127">Requirements</span></span>



| <span data-ttu-id="fcc2d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fcc2d-128">Requirement</span></span> | <span data-ttu-id="fcc2d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fcc2d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc2d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcc2d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc2d-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fcc2d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fcc2d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcc2d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc2d-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fcc2d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcc2d-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fcc2d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcc2d-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcc2d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc2d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcc2d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcc2d-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc2d-138">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="fcc2d-139">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="fcc2d-140">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="fcc2d-141">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="fcc2d-142">**длгтемплате**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="fcc2d-143">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="fcc2d-144">**WM, \_ Шрифт**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="fcc2d-145">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="fcc2d-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc2d-147">Windows</span><span class="sxs-lookup"><span data-stu-id="fcc2d-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="fcc2d-148">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc2d-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="fcc2d-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
