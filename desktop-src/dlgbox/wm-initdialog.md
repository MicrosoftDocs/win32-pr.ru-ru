---
title: Сообщение WM_INITDIALOG (Winuser. h)
description: Отправляется в диалоговое окно непосредственно перед отображением диалогового окна. Обычно это сообщение используется в диалоговых окнах для инициализации элементов управления и выполнения любых других задач инициализации, влияющих на внешний вид диалогового окна.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719204"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="8d81d-105">\_Сообщение ИНИТДИАЛОГ WM</span><span class="sxs-lookup"><span data-stu-id="8d81d-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="8d81d-106">Отправляется в диалоговое окно непосредственно перед отображением диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8d81d-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="8d81d-107">Обычно это сообщение используется в диалоговых окнах для инициализации элементов управления и выполнения любых других задач инициализации, влияющих на внешний вид диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8d81d-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="8d81d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d81d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d81d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d81d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d81d-110">Маркер элемента управления для получения фокуса клавиатуры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d81d-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="8d81d-111">Система назначает фокус клавиатуры по умолчанию только в том случае, если процедура диалогового окна возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8d81d-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8d81d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d81d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d81d-113">Дополнительные данные инициализации.</span><span class="sxs-lookup"><span data-stu-id="8d81d-113">Additional initialization data.</span></span> <span data-ttu-id="8d81d-114">Эти данные передаются в систему в качестве параметра *lParam* при вызове функции [**креатедиалогиндиректпарам**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**креатедиалогпарам**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**диалогбоксиндиректпарам**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)или [**диалогбокспарам**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) , используемой для создания диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8d81d-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="8d81d-115">Для страниц свойств этот параметр является указателем на структуру [**пропшитпаже**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) , используемую для создания страницы.</span><span class="sxs-lookup"><span data-stu-id="8d81d-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="8d81d-116">Этот параметр равен нулю, если используется любая другая функция создания диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8d81d-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d81d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d81d-117">Return value</span></span>

<span data-ttu-id="8d81d-118">Процедура диалогового окна должна возвращать **значение true** , чтобы система настроила фокус клавиатуры на элемент управления, заданный параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="8d81d-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="8d81d-119">В противном случае возвращается **значение false** , чтобы система не настраивает фокус клавиатуры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d81d-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="8d81d-120">Процедура диалогового окна должна возвращать значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="8d81d-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="8d81d-121">Значение **\_ мсгресулт DWL** , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8d81d-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d81d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d81d-122">Remarks</span></span>

<span data-ttu-id="8d81d-123">Элемент управления, получивший фокус клавиатуры по умолчанию, всегда является первым элементом управления в диалоговом окне, который является видимым, не отключенным и имеет стиль **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="8d81d-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="8d81d-124">Когда процедура диалогового окна возвращает **значение true**, система проверяет элемент управления, чтобы убедиться, что процедура не отключена.</span><span class="sxs-lookup"><span data-stu-id="8d81d-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="8d81d-125">Если он был отключен, система устанавливает фокус клавиатуры на следующий элемент управления, который является видимым, не отключен и имеет значение **WS \_ TABSTOP**.</span><span class="sxs-lookup"><span data-stu-id="8d81d-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="8d81d-126">Приложение может вернуть **значение false** только в том случае, если оно установило фокус клавиатуры на один из элементов управления диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8d81d-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d81d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8d81d-127">Requirements</span></span>



| <span data-ttu-id="8d81d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8d81d-128">Requirement</span></span> | <span data-ttu-id="8d81d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8d81d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d81d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d81d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8d81d-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d81d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d81d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d81d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8d81d-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d81d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d81d-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d81d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d81d-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d81d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d81d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d81d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d81d-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8d81d-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d81d-138">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="8d81d-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="8d81d-139">**креатедиалогпарам**</span><span class="sxs-lookup"><span data-stu-id="8d81d-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="8d81d-140">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="8d81d-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="8d81d-141">**диалогбокспарам**</span><span class="sxs-lookup"><span data-stu-id="8d81d-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="8d81d-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="8d81d-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="8d81d-143">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8d81d-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d81d-144">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="8d81d-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="8d81d-145">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="8d81d-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8d81d-146">**пропшитпаже**</span><span class="sxs-lookup"><span data-stu-id="8d81d-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

