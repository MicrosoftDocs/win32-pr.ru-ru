---
title: Сообщение WM_CHOOSEFONT_SETLOGFONT (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ сетлогфонт в диалоговое окно шрифта, чтобы задать текущие сведения о логическом шрифте.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803088"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="ee680-104">\_Сообщение WM CHOOSEFONT \_ сетлогфонт</span><span class="sxs-lookup"><span data-stu-id="ee680-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="ee680-105">Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** в диалоговое окно **шрифта** , чтобы задать текущие сведения о логическом шрифте.</span><span class="sxs-lookup"><span data-stu-id="ee680-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="ee680-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee680-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee680-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee680-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee680-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ee680-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee680-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee680-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee680-110">Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую сведения о текущем логическом шрифте.</span><span class="sxs-lookup"><span data-stu-id="ee680-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee680-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee680-111">Return value</span></span>

<span data-ttu-id="ee680-112">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ee680-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee680-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee680-113">Remarks</span></span>

<span data-ttu-id="ee680-114">При вызове функции [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для создания диалогового окна **шрифта** можно использовать элемент **лплогфонт** структуры [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , чтобы указать структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую начальные значения для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ee680-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="ee680-115">Используйте сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** , чтобы указать структуру **LOGFONT** с разными значениями, пока открыто диалоговое окно **Шрифт** .</span><span class="sxs-lookup"><span data-stu-id="ee680-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="ee680-116">Как правило, сообщение **WM \_ CHOOSEFONT \_ сетлогфонт** отправляется из процедуры-обработчика [**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="ee680-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="ee680-117">Процедура-обработчик также может отправить сообщения [**WM \_ CHOOSEFONT \_ жетлогфонт**](wm-choosefont-getlogfont.md) и [**WM \_ CHOOSEFONT \_ сетфлагс**](wm-choosefont-setflags.md) .</span><span class="sxs-lookup"><span data-stu-id="ee680-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee680-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ee680-118">Requirements</span></span>



| <span data-ttu-id="ee680-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ee680-119">Requirement</span></span> | <span data-ttu-id="ee680-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ee680-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee680-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee680-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee680-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee680-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ee680-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee680-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee680-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee680-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee680-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ee680-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee680-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee680-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee680-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee680-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee680-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ee680-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee680-129">**кфхукпрок**</span><span class="sxs-lookup"><span data-stu-id="ee680-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="ee680-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="ee680-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="ee680-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="ee680-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="ee680-132">**WM \_ CHOOSEFONT \_ жетлогфонт**</span><span class="sxs-lookup"><span data-stu-id="ee680-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="ee680-133">**WM \_ CHOOSEFONT \_ сетфлагс**</span><span class="sxs-lookup"><span data-stu-id="ee680-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="ee680-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ee680-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee680-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="ee680-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="ee680-136">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="ee680-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ee680-137">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="ee680-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

