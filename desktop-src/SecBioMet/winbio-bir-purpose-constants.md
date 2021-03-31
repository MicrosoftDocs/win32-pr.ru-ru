---
title: Константы WINBIO_BIR_PURPOSE (Винбио \_ types. h)
description: Укажите цель, для которой предназначена запись биометрической информации (Бир) или для которой она подходит.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988711"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="4d4e1-103">\_ \_ Константы назначения Бир винбио</span><span class="sxs-lookup"><span data-stu-id="4d4e1-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="4d4e1-104">Следующие флаги используются членом **назначения** структуры [**\_ \_ заголовков винбио Бир**](winbio-bir-header.md) для указания цели, для которой предназначена запись биометрической информации (Бир) или для которой она подходит.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="4d4e1-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4d4e1-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="4d4e1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4d4e1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="4d4e1-107"><dt>**ВИНБИО \_ нет \_ \_ доступных целей**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="4d4e1-108">Назначение не указано.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="4d4e1-109"><dt>**\_Проверка цели \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="4d4e1-110">Проверьте удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="4d4e1-111"><dt>**\_назначение винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="4d4e1-112">Определяет пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="4d4e1-113"><dt>**\_Регистрация цели \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="4d4e1-114">Регистрация пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="4d4e1-115"><dt>**ВИНБИО \_ цель \_ регистрации \_ для \_ проверки**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="4d4e1-116">Запишите образец биометрической метрики и определите, соответствует ли образец указанному удостоверению пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="4d4e1-117"><dt>**\_Регистрация назначения \_ винбио \_ для \_ идентификации**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="4d4e1-118">Запишите образец биометрической метрики и определите, соответствует ли он существующему биометрической шаблону.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="4d4e1-119"><dt>**\_Аудит назначения \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="4d4e1-120">Дополнительные сведения, которые можно использовать для ведения журнала или для вывода.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="4d4e1-121">Это значение игнорируется на входе всеми функциями.</span><span class="sxs-lookup"><span data-stu-id="4d4e1-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="4d4e1-122">На выходе он будет доступен только в том случае, если он поддерживается биометрической единицей, и вы указали **\_ флаг данных винбио \_ \_ RAW** в параметре *flags* функции [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .</span><span class="sxs-lookup"><span data-stu-id="4d4e1-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4d4e1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4d4e1-123">Requirements</span></span>



| <span data-ttu-id="4d4e1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4d4e1-124">Requirement</span></span> | <span data-ttu-id="4d4e1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4d4e1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4e1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d4e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4d4e1-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d4e1-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4d4e1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d4e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4d4e1-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4e1-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4d4e1-130">Header</span><span class="sxs-lookup"><span data-stu-id="4d4e1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d4e1-131"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e1-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d4e1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d4e1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4e1-133">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="4d4e1-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="4d4e1-134">**\_заголовок винбио Бир \_**</span><span class="sxs-lookup"><span data-stu-id="4d4e1-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





