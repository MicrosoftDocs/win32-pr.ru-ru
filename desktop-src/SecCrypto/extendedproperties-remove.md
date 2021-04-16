---
description: Удаляет расширенное свойство из коллекции.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: Расширенных свойств. Remove, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1774ce0fc8b03bed621c58b0f7a9a0f16a7d4156
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668713"
---
# <a name="extendedpropertiesremove-method"></a>Расширенных свойств. Remove, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Метод **Remove** удаляет расширенное свойство из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropID* \[ окне\]
</dt> <dd>

Значение перечисления [**CAPICOM \_ PropID**](capicom-propid.md) , определяющее идентификаторы свойств CAPICOM для удаляемого расширенного свойства. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**Неизвестный CAPICOM/# \_ PropID \_**</dt> </dl>                                                                       | Тип свойства неизвестен.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**\_ \_ \_ маркер Prov ключа CAPICOM \_ PropID**</dt> </dl>                                             | Маркер контейнера ключей в [*поставщике служб шифрования*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**\_ \_ \_ сведения о Prov ключе CAPICOM PropID \_**</dt> </dl>                                                   | Сведения о контейнере ключей в CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**\_ \_ \_ Хэш-код SHA1 PropID**</dt> </dl>                                                                | Хэш-объект SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**\_prop PropID \_ хэш- \_ Свойства**</dt> </dl>                                                                | Свойства хэш-объекта.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**\_ \_ MD5 \_ -хэш "CAPICOM PropID"**</dt> </dl>                                                                   | Хэш-объект MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**\_ \_ контекст ключа CAPICOM \_ PropID**</dt> </dl>                                                          | [*Контекст*](../secgloss/c-gly.md)ключа.<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**\_ \_ Спецификация ключа CAPICOM \_ PropID**</dt> </dl>                                                                   | Спецификации для ключа.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**IE30 "CAPICOM \_ PropID" \_ \_ зарезервирован**</dt> </dl>                                                    | Сведения о том, зарезервирован ли объект в Internet Explorer 3,0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**\_ \_ \_ зарезервированный хэш-код CAPICOM PropID пубкэй \_**</dt> </dl>                              | Сведения о том, зарезервирован ли хэш открытого ключа.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**\_Использование CAPICOM PropID \_ енхкэй \_**</dt> </dl>                                                       | [*Расширенное использование ключа*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**\_ \_ Использование CTL "CAPICOM PropID" \_**</dt> </dl>                                                                | Использование [*списка доверия сертификатов*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**\_Расположение CAPICOM PropID \_ следующего \_ обновления \_**</dt> </dl>                              | Расположение следующего обновления в [*списке отзыва сертификатов*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**\_ \_ понятное имя CAPICOM PropID \_**</dt> </dl>                                                    | Понятное имя.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**файл подcapicom \_ PropID \_ PVK \_**</dt> </dl>                                                                   | Файл, содержащий закрытый ключ.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**Описание подcapicom \_ PropID \_**</dt> </dl>                                                           | Понятное описание.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**\_ \_ состояние доступа CAPICOM \_ PropID**</dt> </dl>                                                       | Состояние доступа.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**\_ \_ хэш подписи CAPICOM \_ PropID**</dt> </dl>                                                 | Хэш сигнатуры.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**\_ \_ данные смарт- \_ карты CAPICOM PropID \_**</dt> </dl>                                             | Данные смарт-карты.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**\_ \_ Файловая система CAPICOM PropID**</dt> </dl>                                                                                   | Шифрованная файловая система (EFS) (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**\_данные CAPICOM PropID \_ Fortezza \_**</dt> </dl>                                                    | Данные, созданные с помощью криптографических протоколов и алгоритмов, принадлежащих [*национальным институтам стандартов и технологий*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**\_заархивированный CAPICOM PropID \_**</dt> </dl>                                                                    | Сведения о том, архивируется ли объект.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**\_ \_ идентификатор подраздела CAPICOM PropID \_**</dt> </dl>                                                 | Идентификатор ключа.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**\_ \_ Автоматическая регистрация CAPICOM \_ PropID**</dt> </dl>                                                          | Сведения об автоматической регистрации сертификата.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PropID \_ пубкэй \_ ALG, \_ абзац**</dt> </dl>                                             | Параметры для алгоритма открытого ключа.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**\_ \_ перекрестные \_ точки в перекрестный сертификате CAPICOM \_ PropID \_**</dt> </dl>                       | Сведения, используемые для обновления динамических перекрестных сертификатов.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**\_ \_ \_ Хэш MD5 открытого ключа для поставщика CAPICOM \_ \_ \_ -PropID**</dt> </dl>          | Хэш MD5 открытого ключа издателя.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ \_ \_ Хэш-код MD5 для субъекта реестра CAPICOM PropID**</dt> </dl>       | Хэш MD5 открытого ключа субъекта.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**\_Регистрация CAPICOM PropID \_**</dt> </dl>                                                              | Сведения о регистрации сертификата.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**\_ \_ Метка даты CAPICOM \_ PropID**</dt> </dl>                                                             | Метка даты.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**\_ \_ \_ Хэш MD5 серийного \_ номера поставщика CAPICOM \_ \_ -PropID**</dt> </dl> | Хэш MD5 серийного номера издателя.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**CAPICOM \_ PropID \_ имя субъекта \_ \_ MD5 \_ хэш**</dt> </dl>                          | Хэш MD5 имени субъекта.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_ \_ Расширенные \_ сведения об ошибке CAPICOM PropID \_**</dt> </dl>                                 | Расширенные сведения об ошибке.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**\_продление элемента CAPICOM PropID \_**</dt> </dl>                                                                       | Сведения об обновлении [*центра сертификации*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**\_ \_ \_ хэш-код подраздела CAPICOM PropID \_**</dt> </dl>                                       | Заархивированный хэш ключа.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**\_ \_ первый \_ зарезервированный CAPICOM PropID**</dt> </dl>                                                 | Сведения о первом резервировании.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**\_ \_ Последнее \_ зарезервированное CAPICOM PropID**</dt> </dl>                                                    | Сведения о последнем резервировании.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ PropID \_ первый \_ пользователь**</dt> </dl>                                                             | Сведения о первом пользователе.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**\_ \_ последний пользователь CAPICOM \_ PropID**</dt> </dl>                                                                | Сведения о последнем пользователе.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
