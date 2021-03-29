---
title: Сообщение CDM_HIDECONTROL (Коммдлг. h)
description: Скрывает указанный элемент управления в диалоговом окне "Открыть" или "Сохранить как" в стиле обозревателя.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661917"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="8fca5-104">\_Сообщение CDM хидеконтрол</span><span class="sxs-lookup"><span data-stu-id="8fca5-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="8fca5-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fca5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="8fca5-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="8fca5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="8fca5-107">Скрывает указанный элемент управления в диалоговом окне " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="8fca5-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="8fca5-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="8fca5-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="8fca5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fca5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fca5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fca5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fca5-111">Идентификатор элемента управления, который должен быть скрыт.</span><span class="sxs-lookup"><span data-stu-id="8fca5-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="8fca5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fca5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fca5-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="8fca5-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fca5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fca5-114">Return value</span></span>

<span data-ttu-id="8fca5-115">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8fca5-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fca5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fca5-116">Remarks</span></span>

<span data-ttu-id="8fca5-117">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8fca5-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="8fca5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8fca5-118">Requirements</span></span>



| <span data-ttu-id="8fca5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8fca5-119">Requirement</span></span> | <span data-ttu-id="8fca5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8fca5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fca5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fca5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fca5-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8fca5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8fca5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fca5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fca5-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8fca5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fca5-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8fca5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fca5-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fca5-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fca5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fca5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8fca5-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8fca5-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8fca5-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8fca5-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="8fca5-130">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="8fca5-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="8fca5-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="8fca5-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="8fca5-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8fca5-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8fca5-133">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="8fca5-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

