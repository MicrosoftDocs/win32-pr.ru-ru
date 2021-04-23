---
title: Сообщение WM_CHOOSEFONT_SETFLAGS (Коммдлг. h)
description: Приложение отправляет \_ сообщение WM CHOOSEFONT \_ сетфлагс в диалоговое окно шрифта, чтобы задать параметры вывода для этого диалогового окна.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136699"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="1c311-104">\_Сообщение WM CHOOSEFONT \_ сетфлагс</span><span class="sxs-lookup"><span data-stu-id="1c311-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="1c311-105">Приложение отправляет сообщение **WM \_ CHOOSEFONT \_ сетфлагс** в диалоговое окно **шрифта** , чтобы задать параметры вывода для этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1c311-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="1c311-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c311-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c311-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c311-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c311-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1c311-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1c311-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c311-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c311-110">Указатель на структуру [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , которая содержит новые параметры в элементе **flags** .</span><span class="sxs-lookup"><span data-stu-id="1c311-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c311-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c311-111">Return value</span></span>

<span data-ttu-id="1c311-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1c311-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c311-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c311-113">Remarks</span></span>

<span data-ttu-id="1c311-114">Функция [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) создает диалоговое окно **шрифта** и использует структуру [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для указания начальных значений для элемента **flags** .</span><span class="sxs-lookup"><span data-stu-id="1c311-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="1c311-115">Используйте сообщение **WM \_ CHOOSEFONT \_ сетфлагс** , чтобы указать различные значения для элемента **flags** , пока открыто диалоговое окно **Шрифт** .</span><span class="sxs-lookup"><span data-stu-id="1c311-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="1c311-116">Как правило, вы должны отправить сообщение **WM \_ CHOOSEFONT \_ сетфлагс** из процедуры-обработчика [**кфхукпрок**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="1c311-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c311-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1c311-117">Requirements</span></span>



| <span data-ttu-id="1c311-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1c311-118">Requirement</span></span> | <span data-ttu-id="1c311-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1c311-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c311-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c311-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1c311-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c311-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1c311-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c311-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1c311-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c311-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1c311-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1c311-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c311-125"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c311-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c311-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c311-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c311-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1c311-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c311-128">**кфхукпрок**</span><span class="sxs-lookup"><span data-stu-id="1c311-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="1c311-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="1c311-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="1c311-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="1c311-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="1c311-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1c311-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1c311-132">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="1c311-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

