---
title: Сообщение CDM_GETFILEPATH (Коммдлг. h)
description: Получает путь и имя выбранного файла в диалоговом окне Обозреватель — открытие или сохранение как.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d531999757d46e127b73584adf1b563e64ea25b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548669"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="b74eb-104">Сообщение CDM. \_</span><span class="sxs-lookup"><span data-stu-id="b74eb-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="b74eb-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="b74eb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="b74eb-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="b74eb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b74eb-107">Получает путь и имя выбранного файла в диалоговом окне Обозреватель — **Открытие** или **Сохранение как** .</span><span class="sxs-lookup"><span data-stu-id="b74eb-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="b74eb-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="b74eb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="b74eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b74eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b74eb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b74eb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b74eb-111">Размер буфера *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="b74eb-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="b74eb-112">Для версии ANSI это число байтов; для версии Юникода это число символов.</span><span class="sxs-lookup"><span data-stu-id="b74eb-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="b74eb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b74eb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b74eb-114">Указатель на буфер, который получает имя файла и путь.</span><span class="sxs-lookup"><span data-stu-id="b74eb-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b74eb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b74eb-115">Return value</span></span>

<span data-ttu-id="b74eb-116">Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) имени файла и строки пути, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="b74eb-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="b74eb-117">Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="b74eb-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="b74eb-118">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="b74eb-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b74eb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b74eb-119">Remarks</span></span>

<span data-ttu-id="b74eb-120">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b74eb-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="b74eb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b74eb-121">Requirements</span></span>



| <span data-ttu-id="b74eb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b74eb-122">Requirement</span></span> | <span data-ttu-id="b74eb-123">Применение</span><span class="sxs-lookup"><span data-stu-id="b74eb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b74eb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b74eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b74eb-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b74eb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b74eb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b74eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b74eb-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b74eb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b74eb-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b74eb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b74eb-129"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b74eb-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74eb-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b74eb-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b74eb-131">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="b74eb-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b74eb-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b74eb-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b74eb-133">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="b74eb-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b74eb-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b74eb-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b74eb-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b74eb-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b74eb-136">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="b74eb-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

