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
# <a name="eap_cert-error-constants"></a>\_Константы ошибки сертификата EAP

Эти константы определяют ошибки, связанные с сертификатами, общие для всех технологий API EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_первый сертификат \_ EAP**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка сертификата будет происходить между **\_ \_ \_ первым** и **\_ \_ \_ последним** сертификатом EAP.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_последний сертификат \_ EAP**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка сертификата будет происходить между **\_ \_ \_ первым** и **\_ \_ \_ последним** сертификатом EAP.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_сертификат EAP \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Сертификат пользователя не найден.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_Недопустимый сертификат EAP \_**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Недопустимый сертификат пользователя.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_ \_ срок действия сертификата EAP истек**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



Срок действия сертификата пользователя истек.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_ \_ отозванный сертификат EAP**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Сертификат пользователя был отозван.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ другая ошибка сертификата \_ EAP**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Произошла неизвестная ошибка, связанная с сертификатом.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_сертификат EAP \_ отклонен**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Сертификат пользователя был отклонен.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_ \_ требуется имя сертификата \_ EAP**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Для сертификата пользователя требуется имя.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_Общие сведения о протоколе EAP \_ \_ First**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Определяет границу отчетов об ошибках; любая общая ошибка EAP будет происходить между **\_ протоколами EAP \_ General \_ First** и **\_ EAP \_ General \_ Last**.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_Общее время \_ последнего EAP**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Определяет границу отчетов об ошибках; любая общая ошибка EAP будет происходить между **\_ протоколами EAP \_ General \_ First** и **\_ EAP \_ General \_ Last**.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Еафостеррор. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие константы EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

 

 





