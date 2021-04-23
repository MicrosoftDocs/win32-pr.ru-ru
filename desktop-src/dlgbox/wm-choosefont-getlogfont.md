---
title: Сообщение WM_CHOOSEFONT_GETLOGFONT (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ жетлогфонт в диалоговое окно шрифта для получения сведений о текущем выборе шрифта пользователем.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691881"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="750b9-104">\_Сообщение WM CHOOSEFONT \_ жетлогфонт</span><span class="sxs-lookup"><span data-stu-id="750b9-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="750b9-105">Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** в диалоговое окно **шрифта** для получения сведений о текущем выборе шрифта пользователем.</span><span class="sxs-lookup"><span data-stu-id="750b9-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="750b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="750b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="750b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750b9-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="750b9-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="750b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="750b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750b9-110">Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , которая получает сведения о текущем выборе шрифта пользователем.</span><span class="sxs-lookup"><span data-stu-id="750b9-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750b9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="750b9-111">Return value</span></span>

<span data-ttu-id="750b9-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="750b9-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="750b9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="750b9-113">Remarks</span></span>

<span data-ttu-id="750b9-114">Функция [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) создает диалоговое окно **шрифта** .</span><span class="sxs-lookup"><span data-stu-id="750b9-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="750b9-115">Когда пользователь закрывает диалоговое окно « **Шрифт** », функция **ChooseFont** возвращает сведения о выборе шрифта пользователем в структуре [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="750b9-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="750b9-116">Элемент **лплогфонт** структуры **CHOOSEFONT** является указателем на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="750b9-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="750b9-117">Используйте сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** для получения сведений о текущем выборе шрифта пользователя, когда открыто диалоговое окно **Шрифт** .</span><span class="sxs-lookup"><span data-stu-id="750b9-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="750b9-118">Например, если включить кнопку **Применить** в диалоговом окне **Шрифт** , отправьте сообщение, чтобы получить сведения о шрифте, которые будут применены к текущему выделению текста.</span><span class="sxs-lookup"><span data-stu-id="750b9-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="750b9-119">Как правило, вы включаете процедуру обработчика [*кфхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) для обработки [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) для кнопки **Применить** .</span><span class="sxs-lookup"><span data-stu-id="750b9-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="750b9-120">Когда пользователь нажимает кнопку " **Применить** ", процедура-обработчик отправляет сообщение **WM \_ CHOOSEFONT \_ жетлогфонт** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="750b9-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="750b9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="750b9-121">Requirements</span></span>



| <span data-ttu-id="750b9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="750b9-122">Requirement</span></span> | <span data-ttu-id="750b9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="750b9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750b9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="750b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="750b9-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="750b9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="750b9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="750b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="750b9-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="750b9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="750b9-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="750b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="750b9-129"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="750b9-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750b9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="750b9-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="750b9-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="750b9-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="750b9-132">**кфхукпрок**</span><span class="sxs-lookup"><span data-stu-id="750b9-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="750b9-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="750b9-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="750b9-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="750b9-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="750b9-135">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="750b9-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="750b9-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="750b9-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="750b9-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="750b9-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="750b9-138">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="750b9-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="750b9-139">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="750b9-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

