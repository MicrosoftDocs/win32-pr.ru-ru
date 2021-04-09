---
title: Сообщение CDM_GETSPEC (Коммдлг. h)
description: Извлекает имя файла (не включая путь) текущего выбранного файла в диалоговом окне Обозреватель — открытие или сохранение как.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- CDM_GETSPEC диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135014"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="11eb2-104">\_Сообщение CDM</span><span class="sxs-lookup"><span data-stu-id="11eb2-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="11eb2-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11eb2-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="11eb2-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="11eb2-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="11eb2-107">Извлекает имя файла (не включая путь) текущего выбранного файла в диалоговом окне Обозреватель — **Открытие** или **Сохранение как** .</span><span class="sxs-lookup"><span data-stu-id="11eb2-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="11eb2-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="11eb2-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="11eb2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="11eb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11eb2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11eb2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11eb2-111">Размер буфера *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="11eb2-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="11eb2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11eb2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11eb2-113">Указатель на буфер, который получает имя файла.</span><span class="sxs-lookup"><span data-stu-id="11eb2-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11eb2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11eb2-114">Return value</span></span>

<span data-ttu-id="11eb2-115">Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки имени файла, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="11eb2-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="11eb2-116">Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="11eb2-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="11eb2-117">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="11eb2-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="11eb2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11eb2-118">Remarks</span></span>

<span data-ttu-id="11eb2-119">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="11eb2-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="11eb2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="11eb2-120">Requirements</span></span>



| <span data-ttu-id="11eb2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="11eb2-121">Requirement</span></span> | <span data-ttu-id="11eb2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="11eb2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11eb2-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11eb2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="11eb2-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11eb2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="11eb2-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11eb2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="11eb2-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11eb2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11eb2-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11eb2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="11eb2-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11eb2-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11eb2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11eb2-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="11eb2-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="11eb2-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11eb2-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="11eb2-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="11eb2-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="11eb2-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="11eb2-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="11eb2-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="11eb2-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="11eb2-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11eb2-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="11eb2-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

