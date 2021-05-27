---
title: Сообщение CDM_GETFOLDERPATH (Коммдлг. h)
description: Возвращает путь к открытой в данный момент папке или каталогу для диалогового окна "Открыть" или "Сохранить как" в стиле обозревателя.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96b8d25714dc3f8bdcf016ac1fd69b2af2414f0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550009"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="f2f6a-104">\_Сообщение CDM GETFOLDERPATH</span><span class="sxs-lookup"><span data-stu-id="f2f6a-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="f2f6a-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="f2f6a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="f2f6a-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="f2f6a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f2f6a-107">Возвращает путь к открытой в данный момент папке или каталогу для диалогового окна " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="f2f6a-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="f2f6a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2f6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f6a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2f6a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2f6a-111">Размер буфера *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f2f6a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2f6a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2f6a-113">Указатель на буфер, который получает путь.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f6a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2f6a-114">Return value</span></span>

<span data-ttu-id="f2f6a-115">Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки пути, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="f2f6a-116">Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="f2f6a-117">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f6a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2f6a-118">Remarks</span></span>

<span data-ttu-id="f2f6a-119">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f2f6a-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="f2f6a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f2f6a-120">Requirements</span></span>



| <span data-ttu-id="f2f6a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f2f6a-121">Requirement</span></span> | <span data-ttu-id="f2f6a-122">Применение</span><span class="sxs-lookup"><span data-stu-id="f2f6a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f6a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2f6a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f6a-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2f6a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2f6a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2f6a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f6a-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2f6a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2f6a-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2f6a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f6a-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2f6a-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f6a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f2f6a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2f6a-130">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="f2f6a-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2f6a-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="f2f6a-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f2f6a-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="f2f6a-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f2f6a-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="f2f6a-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="f2f6a-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f2f6a-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2f6a-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="f2f6a-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

