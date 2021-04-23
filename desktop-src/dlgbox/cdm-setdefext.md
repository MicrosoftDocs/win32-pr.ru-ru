---
title: Сообщение CDM_SETDEFEXT (Коммдлг. h)
description: Задает расширение имени файла по умолчанию для диалогового окна "Открыть" или "Сохранить как" в стиле обозревателя.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590861"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="1b1a5-104">\_Сообщение CDM сетдефекст</span><span class="sxs-lookup"><span data-stu-id="1b1a5-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="1b1a5-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="1b1a5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="1b1a5-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="1b1a5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1b1a5-107">Задает расширение имени файла по умолчанию для диалогового окна " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="1b1a5-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="1b1a5-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="1b1a5-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="1b1a5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b1a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1a5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b1a5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a5-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1b1a5-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1b1a5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b1a5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a5-113">Указатель на новое расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="1b1a5-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="1b1a5-114">Не должен включать точку (.).</span><span class="sxs-lookup"><span data-stu-id="1b1a5-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1a5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b1a5-115">Return value</span></span>

<span data-ttu-id="1b1a5-116">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1b1a5-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b1a5-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b1a5-117">Remarks</span></span>

<span data-ttu-id="1b1a5-118">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b1a5-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="1b1a5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1b1a5-119">Requirements</span></span>



| <span data-ttu-id="1b1a5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1b1a5-120">Requirement</span></span> | <span data-ttu-id="1b1a5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1b1a5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1a5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b1a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1a5-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b1a5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b1a5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b1a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1a5-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b1a5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b1a5-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1b1a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1a5-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b1a5-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1a5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b1a5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b1a5-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1b1a5-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1b1a5-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1b1a5-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1b1a5-131">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="1b1a5-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1b1a5-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="1b1a5-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="1b1a5-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1b1a5-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1b1a5-134">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="1b1a5-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

