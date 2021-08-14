---
description: Возвращает состояние допустимости цепочки или определенного сертификата в цепочке.
title: 'Свойство IChain2:: Status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769554"
---
# <a name="ichain2status-property"></a>Свойство IChain2:: Status

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Status** получает состояние действия цепочки или определенного сертификата в цепочке.

## <a name="syntax"></a>Синтаксис


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Значение свойства

Значение **типа Long** , представляющее индикатор состояния допустимости цепочки или указанного сертификата. В следующей таблице приводятся возможные значения. Это свойство будет содержать нуль, если цепочка или указанный сертификат являются допустимыми. В противном случае это свойство будет содержать сочетание одного или нескольких из следующих значений.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ \_ \_ \_ \_ Недопустимое время доверия** (&H00000001)


</dt> <dd>

Этот сертификат или один из сертификатов в цепочке сертификатов имеет недопустимый срок действия.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ ДОВЕРИЕ \_ не \_ является \_ \_ вложенным во временную** (&H00000002)


</dt> <dd>

Сертификаты в цепочке не вложены в неправильное время.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Отношение \_ доверия \_ отозвано** (&H00000004)


</dt> <dd>

Отношение доверия для этого сертификата или одного из сертификатов в цепочке сертификатов было отозвано.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ ДОВЕРИЕ \_ \_ не является \_ \_ допустимой сигнатурой** (&H00000008)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов не имеет действительной подписи.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ Отношение доверия недопустимо \_ \_ \_ \_ для \_ использования** (&H00000010)


</dt> <dd>

Сертификат или цепочка сертификатов не являются допустимыми для предполагаемого использования.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ недоверенным \_ корнем** (&H00000020)


</dt> <dd>

Сертификат или цепочка сертификатов основаны на недоверенном корне.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_ \_ \_ Неизвестное состояние отзыва доверия** (&H00000040)


</dt> <dd>

Состояние отзыва сертификата или одного из сертификатов в цепочке сертификатов неизвестно.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Отношение доверия \_ является \_ циклическим** (&H00000080)


</dt> <dd>

Один из сертификатов в цепочке выдан [*центром сертификации*](../secgloss/c-gly.md) , которому был сертифицирован исходный сертификат.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_Недопустимое \_ расширение доверия** (&H00000100)


</dt> <dd>

Один из сертификатов имеет недопустимое расширение.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ \_ ограничениям политики** (&H00000200)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений политики, а один из выданных сертификатов имеет неразрешенное расширение сопоставления политик или не имеет необходимого расширения политик выдачи.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ базовым \_ ограничениям** (&H00000400)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение базовых ограничений, а либо сертификат не может использоваться для выдаче других сертификатов, либо превышена длина пути цепочки.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ \_ ограничениям имен** (&H00000800)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет недопустимое расширение ограничений имен.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ Отношение \_ доверия \_ не \_ поддерживает \_ \_ ограничение имен** (&H00001000)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, которое содержит неподдерживаемые поля. Поля минимум и максимум не поддерживаются. Таким, минимальное значение всегда должно быть нулевым, а максимальное — нет. Для другого имени поддерживается только имя участника-пользователя. Следующие варианты альтернативного имени не поддерживаются:

-   X400 адрес
-   Имя субъекта EDI
-   Зарегистрированный идентификатор

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ Отношение \_ доверия \_ не \_ определило \_ \_ ограничение имени** (&H00002000)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, а для одного из вариантов имени в конечном сертификате отсутствует ограничение имени.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ не имеет \_ разрешенного \_ \_ ограничения имен** (&H00004000)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, и для одного из вариантов имени в конечном сертификате не предусмотрено допустимое ограничение имени.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Отношение доверия \_ имеет \_ исключенное \_ \_ ограничение имени** (&H00008000)


</dt> <dd>

Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, и один из вариантов имени в конечном сертификате явно исключается.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ АВТОНОМным \_ отзывом** (&H01000000)


</dt> <dd>

Состояние отзыва сертификата или одного из сертификатов в цепочке сертификатов — «вне сети» или «устарело».

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ \_Политика доверия \_ без \_ \_ политики цепочки выдачи** (&H02000000)


</dt> <dd>

У конечного сертификата нет результирующих политик выдачи, и у одного из выдающих сертификатов ЦС есть расширение ограничений политики, которое ему требуется.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ частичной \_ цепочкой** (&H00010000)


</dt> <dd>

Цепочка сертификатов не конкурирует.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ ДОВЕРЕНный \_ CTL доверия \_ \_ не является \_ \_ допустимым временем** (&H00020000)


</dt> <dd>

Список доверия сертификатов, используемый для создания этой цепочки, не является допустимым временем.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ \_CTL доверия \_ \_ не является \_ \_ допустимым сигнатурой** (&H00040000)


</dt> <dd>

Список доверия сертификатов, используемый для создания этой цепочки, не имеет действительной подписи.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ \_CTL доверия \_ \_ не \_ подходит \_ для \_ использования** (&H00080000)


</dt> <dd>

Список доверия сертификатов, используемый для создания этой цепочки, недопустим для этого использования.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
