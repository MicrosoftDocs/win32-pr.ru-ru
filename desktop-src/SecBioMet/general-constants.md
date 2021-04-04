---
title: Общие константы (Винбио \_ types. h)
description: Укажите максимальную длину SID, дескрипторы, идентификаторы, максимальную длину строки и максимальный размер буфера выборки.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988652"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="4db2f-103">Общие константы (Винбио \_ types. h)</span><span class="sxs-lookup"><span data-stu-id="4db2f-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="4db2f-104">Во всех биометрическая платформа Windows используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="4db2f-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="4db2f-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="4db2f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4db2f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4db2f-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="4db2f-107"><dt>**\_максимальный \_ размер SID \_ безопасности**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="4db2f-108">Максимальная длина значения идентификатора безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="4db2f-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="4db2f-109">В настоящее время это 68.</span><span class="sxs-lookup"><span data-stu-id="4db2f-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="4db2f-110"><dt>**\_идентификатор единицы \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="4db2f-111">ИДЕНТИФИКАЦИОНный номер биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="4db2f-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="4db2f-112"><dt>**\_обработчик сеанса \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="4db2f-113">Длинное целое число без знака, содержащее маркер открытого биометрического сеанса.</span><span class="sxs-lookup"><span data-stu-id="4db2f-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="4db2f-114"><dt>**\_обработчик винбио Framework \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="4db2f-115">Длинное целое число без знака, содержащее маркер открытого сеанса инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4db2f-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="4db2f-116"><dt>**\_UUID винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="4db2f-117">Идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="4db2f-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="4db2f-118"><dt>**\_строка винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="4db2f-119">Массив байтов, содержащий строку в Юникоде, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="4db2f-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="4db2f-120"><dt>**Винбио \_ Максимальная \_ \_ Длина строки**</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="4db2f-121">Максимальная длина **\_ строкового значения винбио** .</span><span class="sxs-lookup"><span data-stu-id="4db2f-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="4db2f-122">В настоящее время это 256.</span><span class="sxs-lookup"><span data-stu-id="4db2f-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="4db2f-123"><dt>**Винбио \_ МАКСИМАЛЬНЫЙ \_ \_ \_ Размер буфера выборки**</dt> ( <dt>0x7FFFFFFF</dt> )</span><span class="sxs-lookup"><span data-stu-id="4db2f-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="4db2f-124">Максимальное число байт в одной биометрической записи данных.</span><span class="sxs-lookup"><span data-stu-id="4db2f-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="4db2f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4db2f-125">Requirements</span></span>



| <span data-ttu-id="4db2f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4db2f-126">Requirement</span></span> | <span data-ttu-id="4db2f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4db2f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db2f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4db2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4db2f-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4db2f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4db2f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4db2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4db2f-131">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4db2f-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4db2f-132">Header</span><span class="sxs-lookup"><span data-stu-id="4db2f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db2f-133"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4db2f-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db2f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db2f-135">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="4db2f-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





