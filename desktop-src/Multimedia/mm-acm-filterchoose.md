---
title: Сообщение MM_ACM_FILTERCHOOSE (MSACM. h)
description: Сообщение MM \_ ACM \_ филтерчусе уведомляет о функции-обработчике диалогового окна акмфилтерчусе перед добавлением элемента в один из трех раскрывающихся списков.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135271"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="33635-104">\_Сообщение mm ACM \_ филтерчусе</span><span class="sxs-lookup"><span data-stu-id="33635-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="33635-105">Сообщение **mm \_ ACM \_ филтерчусе** уведомляет о функции-обработчике диалогового окна [**акмфилтерчусе**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) перед добавлением элемента в один из трех раскрывающихся списков.</span><span class="sxs-lookup"><span data-stu-id="33635-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="33635-106">Это сообщение позволяет приложению настроить параметры, доступные в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="33635-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="33635-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="33635-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33635-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*вдропдовн*</span><span class="sxs-lookup"><span data-stu-id="33635-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="33635-109">Инициализируется раскрывающийся список и операция проверки или добавления.</span><span class="sxs-lookup"><span data-stu-id="33635-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="33635-110">Требование</span><span class="sxs-lookup"><span data-stu-id="33635-110">Requirement</span></span> | <span data-ttu-id="33635-111">Значение</span><span class="sxs-lookup"><span data-stu-id="33635-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33635-112">\_Пользовательская \_ Проверка филтерчусе</span><span class="sxs-lookup"><span data-stu-id="33635-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="33635-113">Параметр *lParam* является указателем на структуру [**вавефилтер**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) , которую необходимо добавить в раскрывающийся список настраиваемое имя.</span><span class="sxs-lookup"><span data-stu-id="33635-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="33635-114">\_Добавление фильтра \_ филтерчусе</span><span class="sxs-lookup"><span data-stu-id="33635-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="33635-115">Параметр *lParam* является указателем на буфер, который принимает структуру [**вавефилтер**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) , которая будет добавлена в раскрывающийся список фильтра.</span><span class="sxs-lookup"><span data-stu-id="33635-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="33635-116">Приложение должно скопировать структуру фильтра для добавления в этот буфер.</span><span class="sxs-lookup"><span data-stu-id="33635-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="33635-117">\_Проверка фильтра \_ филтерчусе</span><span class="sxs-lookup"><span data-stu-id="33635-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="33635-118">Параметр *lParam* является указателем на структуру [**вавефилтер**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) , которую необходимо добавить в раскрывающийся список фильтр.</span><span class="sxs-lookup"><span data-stu-id="33635-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="33635-119">\_Добавление филтерчусе филтертаг \_</span><span class="sxs-lookup"><span data-stu-id="33635-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="33635-120">Параметр *lParam* является указателем на **DWORD** , который принимает тег фильтра звуковой волны, который будет добавлен в раскрывающийся список тег фильтра.</span><span class="sxs-lookup"><span data-stu-id="33635-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="33635-121">\_Проверка филтерчусе филтертаг \_</span><span class="sxs-lookup"><span data-stu-id="33635-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="33635-122">Параметр *lParam* — это тег фильтра звуковой волны, который должен быть указан в раскрывающемся списке тег фильтра.</span><span class="sxs-lookup"><span data-stu-id="33635-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="33635-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*лкустом*</span><span class="sxs-lookup"><span data-stu-id="33635-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="33635-124">Значение, определяемое списком, указанным в параметре **wParam** .</span><span class="sxs-lookup"><span data-stu-id="33635-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33635-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33635-125">Return Value</span></span>

<span data-ttu-id="33635-126">Возвращает **значение true** , если приложение обрабатывает это сообщение или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="33635-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33635-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33635-127">Remarks</span></span>

<span data-ttu-id="33635-128">Если приложение обрабатывает \_ операцию добавления фильтра филтерчусе \_ , размер буфера памяти, указанный в параметре *lParam* , будет определен из функции [**акмметрикс**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="33635-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="33635-129">Если приложение обрабатывает операцию проверки, приложение должно предшествовать возвращаемому значению с параметром **SetWindowLong** (HWND, DWL \_ МСГРЕСУЛТ, (Long) **false**), чтобы диалоговое окно не выходило из списка этого выбора или с **SetWindowLong** (HWND, DWL \_ мсгресулт, (Long)**true**), чтобы разрешить диалоговому окну Вывод этого выбора.</span><span class="sxs-lookup"><span data-stu-id="33635-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="33635-130">При обработке операции добавления приложение должно предшествовать возврату с помощью **SetWindowLong** (HWND, DWL \_ МСГРЕСУЛТ, (Long)**false**), чтобы указать, что больше нет необходимых дополнений или с **SetWindowLong** (HWND, DWL \_ мсгресулт, (Long)**true**), если требуются дополнительные дополнения.</span><span class="sxs-lookup"><span data-stu-id="33635-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="33635-131">Требования</span><span class="sxs-lookup"><span data-stu-id="33635-131">Requirements</span></span>



| <span data-ttu-id="33635-132">Требование</span><span class="sxs-lookup"><span data-stu-id="33635-132">Requirement</span></span> | <span data-ttu-id="33635-133">Значение</span><span class="sxs-lookup"><span data-stu-id="33635-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33635-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33635-134">Minimum supported client</span></span><br/> | <span data-ttu-id="33635-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33635-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="33635-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33635-136">Minimum supported server</span></span><br/> | <span data-ttu-id="33635-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33635-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="33635-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="33635-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="33635-139"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="33635-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33635-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33635-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33635-141">Диспетчер аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="33635-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="33635-142">Сообщения сжатия звука</span><span class="sxs-lookup"><span data-stu-id="33635-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





