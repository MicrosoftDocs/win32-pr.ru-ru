---
description: Флаги, ограничивающие установленные или возвращаемые данные.
title: СРРФ (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080944"
---
# <a name="srrf"></a><span data-ttu-id="bfb09-103">сррф</span><span class="sxs-lookup"><span data-stu-id="bfb09-103">SRRF</span></span>

<span data-ttu-id="bfb09-104">Флаги, ограничивающие установленные или возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="bfb09-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="bfb09-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="bfb09-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="bfb09-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bfb09-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="bfb09-107"><dt>**Сррф \_ RT \_ reg \_ None**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="bfb09-108">Введите REG \_ None.</span><span class="sxs-lookup"><span data-stu-id="bfb09-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="bfb09-109"><dt>**Сррф \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="bfb09-110">Введите REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="bfb09-110">Type REG\_SZ.</span></span> <span data-ttu-id="bfb09-111">\_ \_ Типы SZ Expand автоматически преобразуются в REG- \_ SZ, если не \_ указан флаг сррф NOEXPAND.</span><span class="sxs-lookup"><span data-stu-id="bfb09-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="bfb09-112"><dt>**Сррф \_ \_ \_ \_ SZ с развернутой ПОДразделом RT**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="bfb09-113">Введите REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="bfb09-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="bfb09-114">При получении значения необходимо также получить \_ флаг СРРФ NOEXPAND, иначе [**шрегжетвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) завершится ошибкой с \_ недопустимым \_ параметром.</span><span class="sxs-lookup"><span data-stu-id="bfb09-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="bfb09-115"><dt>**Сррф \_ \_ \_ Двоичный**</dt> <dt>0x00000008</dt> "RT reg"</span><span class="sxs-lookup"><span data-stu-id="bfb09-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="bfb09-116">Введите \_ двоичный файл REG.</span><span class="sxs-lookup"><span data-stu-id="bfb09-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="bfb09-117"><dt>**Сррф \_ \_ \_ Параметр DWORD**</dt> <dt>0x00000010</dt> в RT</span><span class="sxs-lookup"><span data-stu-id="bfb09-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="bfb09-118">Введите REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="bfb09-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="bfb09-119"><dt>**Сррф \_ RT \_ reg \_ Multi \_ SZ**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="bfb09-120">Введите REG \_ Multi \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="bfb09-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="bfb09-121"><dt>**Сррф \_ 0x00000040 \_ \_ QWORD reg**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="bfb09-122">Введите REG \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="bfb09-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="bfb09-123"><dt>**Сррф \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="bfb09-124">REG \_ DWORD и 32-разрядные \_ двоичные типы reg.</span><span class="sxs-lookup"><span data-stu-id="bfb09-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="bfb09-125">Это эквивалентно \_ \_ \_ двоичному параметру сррф RT reg Binary \| сррф \_ RT \_ reg \_ .</span><span class="sxs-lookup"><span data-stu-id="bfb09-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="bfb09-126">Если при извлечении значения двоичные данные значения имеют размер больше 32 бит, он не возвращается.</span><span class="sxs-lookup"><span data-stu-id="bfb09-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="bfb09-127"><dt>**Сррф \_ 0x00000048 \_ QWORD 8**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="bfb09-128">REG \_ QWORD и 64-разрядные \_ двоичные типы reg.</span><span class="sxs-lookup"><span data-stu-id="bfb09-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="bfb09-129">Это эквивалентно \_ \_ двоичному сррф RT REG \_ двоичный \| сррф \_ RT \_ reg \_ .</span><span class="sxs-lookup"><span data-stu-id="bfb09-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="bfb09-130">Если при извлечении значения двоичные данные значения имеют размер больше 64 бит, он не возвращается.</span><span class="sxs-lookup"><span data-stu-id="bfb09-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="bfb09-131"><dt>**Сррф \_ RT \_ ANY**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="bfb09-132">Все типы.</span><span class="sxs-lookup"><span data-stu-id="bfb09-132">All types.</span></span> <span data-ttu-id="bfb09-133">Установите этот флаг, если не \_ задано другое значение сррф RT.</span><span class="sxs-lookup"><span data-stu-id="bfb09-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="bfb09-134"><dt>**Сррф \_ RM — \_ любое**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="bfb09-135">Нет ограничений режима.</span><span class="sxs-lookup"><span data-stu-id="bfb09-135">No mode restriction.</span></span> <span data-ttu-id="bfb09-136">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bfb09-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="bfb09-137"><dt>**Сррф \_ \_Нормальная**</dt> <dt>0x00010000а</dt> RM</span><span class="sxs-lookup"><span data-stu-id="bfb09-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="bfb09-138">Ограничьте режим запуска системы на "нормальная загрузка".</span><span class="sxs-lookup"><span data-stu-id="bfb09-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="bfb09-139"><dt>**Сррф \_ Надежное \_**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="bfb09-140">Ограничьте режим запуска системы на "защищенный режим".</span><span class="sxs-lookup"><span data-stu-id="bfb09-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="bfb09-141"><dt>**Сррф \_ RM \_ сафенетворк**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="bfb09-142">Ограничьте режим запуска системы на "защищенный режим с помощью сети".</span><span class="sxs-lookup"><span data-stu-id="bfb09-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="bfb09-143"><dt>**Сррф \_ РАЗВЕРНУТЬ**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="bfb09-144">Не разворачивайте автоматически \_ строки reg Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="bfb09-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="bfb09-145"><dt>**Сррф \_ ЗЕРУНФАИЛУРЕ**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="bfb09-146">Если при извлечении значения *пвдата* не равно **null**, установите в качестве содержимого буфера *пвдата* все нули при сбое.</span><span class="sxs-lookup"><span data-stu-id="bfb09-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="bfb09-147"><dt>**Сррф \_ НОВИРТ**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="bfb09-148">При получении значения, если запрошенный ключ виртуализирован, \_ не удается найти файл с ошибкой \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bfb09-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="bfb09-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfb09-149">Remarks</span></span>

<span data-ttu-id="bfb09-150">Эти значения определены в Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="bfb09-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb09-151">Требования</span><span class="sxs-lookup"><span data-stu-id="bfb09-151">Requirements</span></span>



| <span data-ttu-id="bfb09-152">Требование</span><span class="sxs-lookup"><span data-stu-id="bfb09-152">Requirement</span></span> | <span data-ttu-id="bfb09-153">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb09-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb09-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfb09-154">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb09-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfb09-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfb09-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfb09-156">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb09-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfb09-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfb09-158">Header</span><span class="sxs-lookup"><span data-stu-id="bfb09-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfb09-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfb09-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb09-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfb09-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb09-161">**шрегсетвалуе**</span><span class="sxs-lookup"><span data-stu-id="bfb09-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="bfb09-162">**шрегжетвалуе**</span><span class="sxs-lookup"><span data-stu-id="bfb09-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




