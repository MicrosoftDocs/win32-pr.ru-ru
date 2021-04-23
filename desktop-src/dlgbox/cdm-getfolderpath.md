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
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590941"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="f6cfb-104">\_Сообщение CDM GETFOLDERPATH</span><span class="sxs-lookup"><span data-stu-id="f6cfb-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="f6cfb-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="f6cfb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="f6cfb-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="f6cfb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f6cfb-107">Возвращает путь к открытой в данный момент папке или каталогу для диалогового окна " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="f6cfb-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="f6cfb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6cfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6cfb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6cfb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cfb-111">Размер буфера *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f6cfb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6cfb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cfb-113">Указатель на буфер, который получает путь.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6cfb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6cfb-114">Return value</span></span>

<span data-ttu-id="f6cfb-115">Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки пути, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="f6cfb-116">Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="f6cfb-117">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="f6cfb-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6cfb-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6cfb-118">Remarks</span></span>

<span data-ttu-id="f6cfb-119">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f6cfb-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="f6cfb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f6cfb-120">Requirements</span></span>



| <span data-ttu-id="f6cfb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f6cfb-121">Requirement</span></span> | <span data-ttu-id="f6cfb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f6cfb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6cfb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6cfb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6cfb-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6cfb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f6cfb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6cfb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6cfb-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6cfb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6cfb-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f6cfb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6cfb-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6cfb-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6cfb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6cfb-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6cfb-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f6cfb-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6cfb-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="f6cfb-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f6cfb-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="f6cfb-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f6cfb-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="f6cfb-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="f6cfb-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f6cfb-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6cfb-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="f6cfb-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

