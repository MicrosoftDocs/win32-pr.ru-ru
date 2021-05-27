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
ms.openlocfilehash: 27eff7e9a14f39554fa6c1a69846bbaca7c39990
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548879"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="37d2f-104">\_Сообщение CDM</span><span class="sxs-lookup"><span data-stu-id="37d2f-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="37d2f-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="37d2f-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="37d2f-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="37d2f-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="37d2f-107">Извлекает имя файла (не включая путь) текущего выбранного файла в диалоговом окне Обозреватель — **Открытие** или **Сохранение как** .</span><span class="sxs-lookup"><span data-stu-id="37d2f-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="37d2f-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="37d2f-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="37d2f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="37d2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d2f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37d2f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37d2f-111">Размер буфера *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="37d2f-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="37d2f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37d2f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37d2f-113">Указатель на буфер, который получает имя файла.</span><span class="sxs-lookup"><span data-stu-id="37d2f-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d2f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37d2f-114">Return value</span></span>

<span data-ttu-id="37d2f-115">Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки имени файла, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="37d2f-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="37d2f-116">Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="37d2f-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="37d2f-117">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="37d2f-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="37d2f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37d2f-118">Remarks</span></span>

<span data-ttu-id="37d2f-119">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="37d2f-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="37d2f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="37d2f-120">Requirements</span></span>



| <span data-ttu-id="37d2f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="37d2f-121">Requirement</span></span> | <span data-ttu-id="37d2f-122">Применение</span><span class="sxs-lookup"><span data-stu-id="37d2f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d2f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37d2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37d2f-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37d2f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37d2f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37d2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37d2f-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37d2f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37d2f-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="37d2f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d2f-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37d2f-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37d2f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="37d2f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="37d2f-130">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="37d2f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37d2f-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="37d2f-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="37d2f-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="37d2f-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="37d2f-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="37d2f-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="37d2f-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="37d2f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="37d2f-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="37d2f-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

