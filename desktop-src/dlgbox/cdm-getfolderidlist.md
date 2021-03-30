---
title: Сообщение CDM_GETFOLDERIDLIST (Коммдлг. h)
description: Извлекает адрес списка идентификаторов элементов, соответствующего папке, открытой в обозревателе в диалоговом окне «Открыть» или «сохранить как» в настоящий момент.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ac82a628d6fcace6863abb30e5703af02a948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803556"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="81433-104">\_Сообщение CDM жетфолдеридлист</span><span class="sxs-lookup"><span data-stu-id="81433-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="81433-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81433-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="81433-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="81433-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="81433-107">Извлекает адрес списка идентификаторов элементов, соответствующего папке, открытой в обозревателе в диалоговом окне « **Открыть** » или « **Сохранить как** » в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="81433-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="81433-108">Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.</span><span class="sxs-lookup"><span data-stu-id="81433-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="81433-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="81433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81433-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81433-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81433-111">Размер буфера *lParam* в байтах.</span><span class="sxs-lookup"><span data-stu-id="81433-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="81433-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81433-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81433-113">Указатель на буфер, который получает список идентификаторов элементов.</span><span class="sxs-lookup"><span data-stu-id="81433-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81433-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81433-114">Return value</span></span>

<span data-ttu-id="81433-115">Если сообщение прошло удачно, возвращаемое значение равно размеру (в байтах) списка идентификаторов элементов.</span><span class="sxs-lookup"><span data-stu-id="81433-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="81433-116">Это либо число байтов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="81433-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="81433-117">При возникновении ошибки возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="81433-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="81433-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81433-118">Remarks</span></span>

<span data-ttu-id="81433-119">Соответствующий макрос выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="81433-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="81433-120">Требования</span><span class="sxs-lookup"><span data-stu-id="81433-120">Requirements</span></span>



| <span data-ttu-id="81433-121">Требование</span><span class="sxs-lookup"><span data-stu-id="81433-121">Requirement</span></span> | <span data-ttu-id="81433-122">Значение</span><span class="sxs-lookup"><span data-stu-id="81433-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81433-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81433-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81433-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81433-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="81433-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81433-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81433-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81433-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81433-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="81433-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="81433-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81433-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81433-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81433-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="81433-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="81433-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81433-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="81433-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="81433-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="81433-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="81433-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="81433-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="81433-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="81433-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81433-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="81433-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

