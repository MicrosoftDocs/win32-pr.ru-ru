---
description: Укажите уровни защиты для системы управления созданием копий \# ,&8212; Аналоговый (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Флаги защиты CGMS-A (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423574"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="d573d-103">Флаги защиты CGMS-A</span><span class="sxs-lookup"><span data-stu-id="d573d-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="d573d-104">Константы в следующей таблице задают уровни защиты для аналоговой системы управления копиями (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="d573d-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="d573d-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="d573d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="d573d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d573d-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="d573d-107"><dt>**ОПМ \_ КГМСА \_ Off**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d573d-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="d573d-108">CGMS-A отключен.</span><span class="sxs-lookup"><span data-stu-id="d573d-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="d573d-109"><dt>**ОПМ \_ КГМСА \_ Copy, \_ свободно**</dt> , <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="d573d-110">Уровень защиты свободно копируется.</span><span class="sxs-lookup"><span data-stu-id="d573d-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="d573d-111"><dt>**ОПМ \_ КГМСА \_ Копировать \_ \_**</dt> больше <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="d573d-112">Уровень защиты больше не копируется.</span><span class="sxs-lookup"><span data-stu-id="d573d-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="d573d-113"><dt>**ОПМ \_ КГМСА \_ копирование \_ одного \_ поколения**</dt> <dt>0x03</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="d573d-114">Уровень защиты — это копирование одного поколения.</span><span class="sxs-lookup"><span data-stu-id="d573d-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="d573d-115"><dt>**ОПМ \_ КГМСА \_ копия \_ никогда не**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="d573d-116">Уровень защиты никогда не копируется.</span><span class="sxs-lookup"><span data-stu-id="d573d-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="d573d-117"><dt>**ОПМ \_ \_ \_ \_ Требуется элемент управления повторного распределения кгмса**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="d573d-118">Требуется элемент управления перераспределением (также называемый *флагом вещания*).</span><span class="sxs-lookup"><span data-stu-id="d573d-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="d573d-119">Этот флаг можно сочетать с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="d573d-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d573d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d573d-120">Remarks</span></span>

<span data-ttu-id="d573d-121">Эти флаги эквивалентны константам перечисления **\_ \_ \_ уровня защиты Копп кгмса** , используемым в протоколе сертифицированной выходной защиты (Копп).</span><span class="sxs-lookup"><span data-stu-id="d573d-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="d573d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d573d-122">Requirements</span></span>



| <span data-ttu-id="d573d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d573d-123">Requirement</span></span> | <span data-ttu-id="d573d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d573d-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d573d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d573d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d573d-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d573d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d573d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d573d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d573d-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d573d-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d573d-129">Header</span><span class="sxs-lookup"><span data-stu-id="d573d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d573d-130"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d573d-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d573d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d573d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d573d-132">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d573d-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




