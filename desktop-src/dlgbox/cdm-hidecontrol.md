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
ms.openlocfilehash: 7c0f2f41017373d9064da8f1024066f131063d9d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590881"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="86fac-104">\_Сообщение CDM хидеконтрол</span><span class="sxs-lookup"><span data-stu-id="86fac-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="86fac-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="86fac-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="86fac-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="86fac-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="86fac-107">Скрывает указанный элемент управления в диалоговом окне " **Открыть** " или " **Сохранить как** " в стиле обозревателя.</span><span class="sxs-lookup"><span data-stu-id="86fac-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="86fac-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="86fac-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="86fac-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="86fac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86fac-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86fac-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86fac-111">Идентификатор элемента управления, который должен быть скрыт.</span><span class="sxs-lookup"><span data-stu-id="86fac-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="86fac-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86fac-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86fac-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="86fac-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86fac-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86fac-114">Return value</span></span>

<span data-ttu-id="86fac-115">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="86fac-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fac-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="86fac-116">Remarks</span></span>

<span data-ttu-id="86fac-117">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="86fac-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="86fac-118">Требования</span><span class="sxs-lookup"><span data-stu-id="86fac-118">Requirements</span></span>



| <span data-ttu-id="86fac-119">Требование</span><span class="sxs-lookup"><span data-stu-id="86fac-119">Requirement</span></span> | <span data-ttu-id="86fac-120">Значение</span><span class="sxs-lookup"><span data-stu-id="86fac-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86fac-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86fac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86fac-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86fac-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="86fac-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86fac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86fac-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86fac-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86fac-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="86fac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86fac-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86fac-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fac-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86fac-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="86fac-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="86fac-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86fac-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="86fac-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="86fac-130">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="86fac-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="86fac-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="86fac-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="86fac-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="86fac-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86fac-133">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="86fac-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

