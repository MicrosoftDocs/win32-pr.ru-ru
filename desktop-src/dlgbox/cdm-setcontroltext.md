---
title: Сообщение CDM_SETCONTROLTEXT (Коммдлг. h)
description: Задает текст для указанного элемента управления в диалоговом окне "Открыть" или "Сохранить как" в стиле обозревателя.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d75bb3d3ac486bbb43545df80c67383a7655b8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590891"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="a20fb-104">\_Сообщение CDM сетконтролтекст</span><span class="sxs-lookup"><span data-stu-id="a20fb-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="a20fb-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="a20fb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="a20fb-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="a20fb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a20fb-107">Задает текст для указанного элемента управления в диалоговом окне " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="a20fb-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="a20fb-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="a20fb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="a20fb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a20fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20fb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a20fb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a20fb-111">Идентификатор элемента управления, для которого задается текст.</span><span class="sxs-lookup"><span data-stu-id="a20fb-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="a20fb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a20fb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a20fb-113">Новый текст для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a20fb-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20fb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a20fb-114">Return value</span></span>

<span data-ttu-id="a20fb-115">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a20fb-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a20fb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a20fb-116">Remarks</span></span>

<span data-ttu-id="a20fb-117">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a20fb-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="a20fb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a20fb-118">Requirements</span></span>



| <span data-ttu-id="a20fb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a20fb-119">Requirement</span></span> | <span data-ttu-id="a20fb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a20fb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a20fb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a20fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a20fb-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a20fb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a20fb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a20fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a20fb-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a20fb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a20fb-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a20fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a20fb-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a20fb-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20fb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a20fb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a20fb-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a20fb-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a20fb-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a20fb-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a20fb-130">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="a20fb-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a20fb-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a20fb-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="a20fb-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a20fb-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a20fb-133">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="a20fb-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

