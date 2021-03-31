---
title: Сообщение MM_ACM_FORMATCHOOSE (MSACM. h)
description: Сообщение MM \_ ACM \_ форматчусе уведомляет о функции диалогового окна акмформатчусе перед добавлением элемента в один из трех раскрывающихся списков.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804091"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="36217-104">\_Сообщение mm ACM \_ форматчусе</span><span class="sxs-lookup"><span data-stu-id="36217-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="36217-105">Сообщение **mm \_ ACM \_ форматчусе** уведомляет о функции диалогового окна [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) перед добавлением элемента в один из трех раскрывающихся списков.</span><span class="sxs-lookup"><span data-stu-id="36217-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="36217-106">Это сообщение позволяет приложению настроить параметры, доступные в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="36217-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="36217-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36217-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36217-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*вдропдовн*</span><span class="sxs-lookup"><span data-stu-id="36217-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="36217-109">Инициализируется раскрывающийся список и операция проверки или добавления.</span><span class="sxs-lookup"><span data-stu-id="36217-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="36217-110">Требование</span><span class="sxs-lookup"><span data-stu-id="36217-110">Requirement</span></span> | <span data-ttu-id="36217-111">Значение</span><span class="sxs-lookup"><span data-stu-id="36217-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36217-112">\_Пользовательская \_ Проверка форматчусе</span><span class="sxs-lookup"><span data-stu-id="36217-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="36217-113">Параметр *lParam* является указателем на структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) , которую необходимо добавить в раскрывающийся список настраиваемое имя.</span><span class="sxs-lookup"><span data-stu-id="36217-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="36217-114">ФОРМАТЧУСЕ \_ Формат \_ добавления</span><span class="sxs-lookup"><span data-stu-id="36217-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="36217-115">Параметр *lParam* является указателем на буфер, который принимает структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) , которая будет добавлена в раскрывающийся список формат.</span><span class="sxs-lookup"><span data-stu-id="36217-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="36217-116">Приложение должно скопировать структуру формата для добавления в этот буфер.</span><span class="sxs-lookup"><span data-stu-id="36217-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="36217-117">\_Проверка формата \_ форматчусе</span><span class="sxs-lookup"><span data-stu-id="36217-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="36217-118">Параметр *lParam* является указателем на структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) , которую необходимо добавить в раскрывающийся список формат.</span><span class="sxs-lookup"><span data-stu-id="36217-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="36217-119">\_Добавление форматчусе форматтаг \_</span><span class="sxs-lookup"><span data-stu-id="36217-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="36217-120">Параметр *lParam* является указателем на переменную, которая принимает тег формата звуковой волны, который будет добавлен в раскрывающийся список тегов формата.</span><span class="sxs-lookup"><span data-stu-id="36217-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="36217-121">\_Проверка форматчусе форматтаг \_</span><span class="sxs-lookup"><span data-stu-id="36217-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="36217-122">Параметр *lParam* — это тег формата звуковой волны, который должен быть указан в раскрывающемся списке тег формата.</span><span class="sxs-lookup"><span data-stu-id="36217-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="36217-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*лкустом*</span><span class="sxs-lookup"><span data-stu-id="36217-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="36217-124">Значение, определенное элементом управления ListBox, указанным в параметре **wParam** .</span><span class="sxs-lookup"><span data-stu-id="36217-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36217-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36217-125">Return Value</span></span>

<span data-ttu-id="36217-126">Возвращает **значение true** , если приложение обрабатывает это сообщение или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36217-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36217-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36217-127">Remarks</span></span>

<span data-ttu-id="36217-128">Если приложение обрабатывает \_ операцию добавления формата филтерчусе \_ , размер буфера памяти, указанный в параметре *lParam* , будет определен из функции [**акмметрикс**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="36217-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="36217-129">Если приложение обрабатывает операцию проверки, оно может препятствовать перечислению этого выбора в диалоговом окне, вызвав функцию **SetWindowLong** с параметром *ниндекс* , равным DWL \_ мсгресулт, а *лневлонг* — значение **false** (приведение к типу данных **Long** ).</span><span class="sxs-lookup"><span data-stu-id="36217-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="36217-130">Чтобы разрешить диалоговому окну выводить список этих элементов, вызовите эту функцию с параметром *лневлонг* , имеющим значение **true**.</span><span class="sxs-lookup"><span data-stu-id="36217-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="36217-131">Если приложение обрабатывает операцию добавления, оно может указать, что больше не требуется дополнительных дополнений, вызвав функцию **SetWindowLong** с параметром *ниндекс* , равным DWL \_ Мсгресулт, а *лневлонг* — **значение false** (приведение к типу данных **Long** ).</span><span class="sxs-lookup"><span data-stu-id="36217-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="36217-132">Чтобы указать, что требуются дополнительные дополнения, вызовите эту функцию с параметром *лневлонг* , имеющим значение **true**.</span><span class="sxs-lookup"><span data-stu-id="36217-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36217-133">Требования</span><span class="sxs-lookup"><span data-stu-id="36217-133">Requirements</span></span>



| <span data-ttu-id="36217-134">Требование</span><span class="sxs-lookup"><span data-stu-id="36217-134">Requirement</span></span> | <span data-ttu-id="36217-135">Значение</span><span class="sxs-lookup"><span data-stu-id="36217-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36217-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36217-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36217-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36217-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="36217-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36217-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36217-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36217-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36217-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36217-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="36217-141"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="36217-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36217-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36217-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36217-143">Диспетчер аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="36217-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="36217-144">Сообщения сжатия звука</span><span class="sxs-lookup"><span data-stu-id="36217-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

