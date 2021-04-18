---
title: '\_Константы ошибки сертификата EAP (еафостеррор. h)'
description: Определите ошибки, связанные с сертификатами, общие для всех технологий API EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533902"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="d10aa-103">\_Константы ошибки сертификата EAP</span><span class="sxs-lookup"><span data-stu-id="d10aa-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="d10aa-104">Эти константы определяют ошибки, связанные с сертификатами, общие для всех технологий API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d10aa-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="d10aa-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_первый сертификат \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-106">0x0</span><span class="sxs-lookup"><span data-stu-id="d10aa-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-107">Определяет границу отчетов об ошибках; Любая ошибка сертификата будет происходить между **\_ \_ \_ первым** и **\_ \_ \_ последним** сертификатом EAP.</span><span class="sxs-lookup"><span data-stu-id="d10aa-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_последний сертификат \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-109">0xF</span><span class="sxs-lookup"><span data-stu-id="d10aa-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-110">Определяет границу отчетов об ошибках; Любая ошибка сертификата будет происходить между **\_ \_ \_ первым** и **\_ \_ \_ последним** сертификатом EAP.</span><span class="sxs-lookup"><span data-stu-id="d10aa-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_сертификат EAP \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="d10aa-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-112">0x1</span><span class="sxs-lookup"><span data-stu-id="d10aa-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-113">Сертификат пользователя не найден.</span><span class="sxs-lookup"><span data-stu-id="d10aa-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_Недопустимый сертификат EAP \_**</span><span class="sxs-lookup"><span data-stu-id="d10aa-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-115">0x2</span><span class="sxs-lookup"><span data-stu-id="d10aa-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-116">Недопустимый сертификат пользователя.</span><span class="sxs-lookup"><span data-stu-id="d10aa-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_ \_ срок действия сертификата EAP истек**</span><span class="sxs-lookup"><span data-stu-id="d10aa-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-118">0x3</span><span class="sxs-lookup"><span data-stu-id="d10aa-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-119">Срок действия сертификата пользователя истек.</span><span class="sxs-lookup"><span data-stu-id="d10aa-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_ \_ отозванный сертификат EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-121">0x4</span><span class="sxs-lookup"><span data-stu-id="d10aa-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-122">Сертификат пользователя был отозван.</span><span class="sxs-lookup"><span data-stu-id="d10aa-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ другая ошибка сертификата \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-124">0x5</span><span class="sxs-lookup"><span data-stu-id="d10aa-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-125">Произошла неизвестная ошибка, связанная с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="d10aa-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_сертификат EAP \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="d10aa-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-127">0x6</span><span class="sxs-lookup"><span data-stu-id="d10aa-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-128">Сертификат пользователя был отклонен.</span><span class="sxs-lookup"><span data-stu-id="d10aa-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_ \_ требуется имя сертификата \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-130">0x7</span><span class="sxs-lookup"><span data-stu-id="d10aa-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-131">Для сертификата пользователя требуется имя.</span><span class="sxs-lookup"><span data-stu-id="d10aa-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_Общие сведения о протоколе EAP \_ \_ First**</span><span class="sxs-lookup"><span data-stu-id="d10aa-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-133">0x10</span><span class="sxs-lookup"><span data-stu-id="d10aa-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-134">Определяет границу отчетов об ошибках; любая общая ошибка EAP будет происходить между **\_ протоколами EAP \_ General \_ First** и **\_ EAP \_ General \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="d10aa-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d10aa-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_Общее время \_ последнего EAP**</span><span class="sxs-lookup"><span data-stu-id="d10aa-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10aa-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="d10aa-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="d10aa-137">Определяет границу отчетов об ошибках; любая общая ошибка EAP будет происходить между **\_ протоколами EAP \_ General \_ First** и **\_ EAP \_ General \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="d10aa-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d10aa-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d10aa-138">Requirements</span></span>



| <span data-ttu-id="d10aa-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d10aa-139">Requirement</span></span> | <span data-ttu-id="d10aa-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d10aa-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10aa-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d10aa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d10aa-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d10aa-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d10aa-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d10aa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d10aa-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d10aa-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d10aa-145">Header</span><span class="sxs-lookup"><span data-stu-id="d10aa-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10aa-146"><dt>Еафостеррор. h</dt></span><span class="sxs-lookup"><span data-stu-id="d10aa-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10aa-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d10aa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10aa-148">Общие константы EAPHost</span><span class="sxs-lookup"><span data-stu-id="d10aa-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





