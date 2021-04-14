---
description: Обращается к существующему контейнеру ключей. Этот метод связывает контейнер ключей с сертификатом, который соответствует закрытому ключу, путем добавления \_ \_ свойства идентификатора Prov info для ключа сертификата \_ \_ \_ с использованием указанных сведений.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: PrivateKey. Open, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665441"
---
# <a name="privatekeyopen-method"></a>PrivateKey. Open, метод

\[Метод **Open** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Open** обращается к существующему [*контейнеру ключей*](../secgloss/k-gly.md). Этот метод связывает контейнер ключей с [*сертификатом*](../secgloss/c-gly.md) , который соответствует [*закрытому ключу*](../secgloss/p-gly.md) , путем добавления \_ \_ свойства идентификатора Prov info для ключа сертификата \_ \_ \_ с использованием указанных сведений.

## <a name="syntax"></a>Синтаксис


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ContainerName* \[ окне\]
</dt> <dd>

Строка, содержащая имя контейнера ключей.

</dd> <dt>

*ProviderName* \[ в необязательное\]
</dt> <dd>

Строка, содержащая имя поставщика. Значение по умолчанию — CAPICOM \_ Prov \_ MS \_ Enhanced \_ Prov. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                      | Значение                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ Prov**</dt> </dl>                                          | Базовый поставщик служб шифрования Майкрософт.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Enhanced \_ Prov**</dt> </dl>                           | Улучшенный поставщик служб шифрования Майкрософт.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ strong \_ Prov**</dt> </dl>                                 | Поставщик строгой криптографии (Майкрософт).<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ RSA \_ SIG \_ Prov**</dt> </dl>                | Поставщик криптографической подписи RSA (Майкрософт).<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ RSA \_ SChannel \_ Prov**</dt> </dl> | Поставщик криптографии Microsoft RSA SChannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ \_ Prov**</dt> </dl>                             | Поставщик служб шифрования Microsoft Base DSS.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ DSS \_ \_ Prov**</dt> </dl>                   | Microsoft Base DSS и поставщик служб шифрования Diffie-Hellman.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ ЕНХ \_ DSS \_ DH \_ Prov**</dt> </dl>                   | Microsoft Enhanced DSS и поставщик служб шифрования Diffie-Hellman.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ DH \_ SChannel \_ Prov**</dt> </dl>    | Поставщик криптографии Диффи-Хелмана Microsoft DH.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ бросить \_ Prov**</dt> </dl>                                    | Базовый поставщик служб шифрования смарт-карт (Майкрософт).<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ ЕНХ \_ RSA \_ AES \_ Prov**</dt> </dl>                | Улучшенный поставщик служб шифрования RSA и AES Майкрософт.<br/>            |



 

</dd> <dt>

*ProviderType* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**\_ \_ типа CAPICOM Prov**](capicom-prov-type.md) , указывающее тип поставщика. Значение по умолчанию — CAPICOM \_ Prov \_ RSA \_ Full. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ Full**</dt> </dl>                 | Полный [*поставщик служб шифрования*](../secgloss/c-gly.md) [*RSA*](../secgloss/r-gly.md) (CSP). Этот тип поставщика поддерживает [*цифровые подписи*](../secgloss/d-gly.md) и [*Шифрование*](../secgloss/e-gly.md)данных.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SIG**</dt> </dl>                    | Подмножество CSP RSA, которое поддерживает только те функции и алгоритмы, которые необходимы для [*хэширования*](../secgloss/h-gly.md) и [*цифровых подписей*](../secgloss/d-gly.md).<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | CSP [*стандарта цифровой подписи*](../secgloss/d-gly.md) (DSS). Этот тип поставщика поддерживает только хэши и Цифровые подписи. DSS использует [*алгоритм цифровых подписей*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Prov \_ Fortezza**</dt> </dl>                  | CSP, содержащий криптографические протоколы и алгоритмы, принадлежащие [*национальным институтам стандартов и технологий*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Exchange**</dt> </dl>        | CSP, который поддерживает приложение Microsoft Exchange Mail и другие приложения, совместимые с Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ Prov \_ SSL**</dt> </dl>                                 | CSP, поддерживающий протокол [*SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SChannel**</dt> </dl>     | CSP, поддерживающий протоколы RSA и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS \_ DH**</dt> </dl>                       | CSP, поддерживающий протоколы DSS и [*Диффи-Хелмана*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ , \_ подпись**</dt> </dl>    | CSP, который поддерживает функции алгоритма цифровых подписей на основе эллиптических кривых (ECDSA) и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ екнра \_ SIG**</dt> </dl>    | CSP, поддерживающий эллиптическую кривую Nyberg-Rueppel аналоговые (ЕКНРА) функции и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ Full**</dt> </dl> | CSP, поддерживающий полное значение ECDSA.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ екнра \_ Full**</dt> </dl> | CSP, поддерживающий полную ЕКНРА.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ DH \_ SChannel**</dt> </dl>        | CSP, поддерживающий протоколы [*Диффи-Хелмана*](../secgloss/d-gly.md) и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ спирус \_ Линкс**</dt> </dl>     | CSP, поддерживающий устройство СПИРУС Линкс Card.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ РНГ**</dt> </dl>                                 | CSP, обрабатывающий генерацию случайных чисел.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ sec**</dt> </dl>              | CSP, обеспечивающий безопасность Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ заменить \_ OWF**</dt> </dl>        | CSP, поддерживающий замену способа, с помощью которого односторонние форматы создаются из паролей.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | CSP, поддерживающий цифровые подписи и шифрование данных с помощью алгоритма AES ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[ в необязательное\]
</dt> <dd>

Значение перечисления " [**CAPICOM \_ key \_ Spec**](capicom-key-spec.md) ", указывающее тип закрытого ключа. Значение по умолчанию — \_ сигнатура элемента CAPICOM key \_ Spec \_ . Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                        | Значение                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**\_ \_ КЭЙЕКСЧАНЖЕ спецификация CAPICOM \_**</dt> </dl> | Ключ можно использовать для шифрования и подписывания.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**\_ \_ подпись спецификации CAPICOM \_**</dt> </dl>       | Ключ можно использовать только для подписывания.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**CAPICOM \_ Store \_ Location**](capicom-store-location.md) , указывающее расположение хранилища, в котором находится ключ. Значение по умолчанию — "CAPICOM \_ Current \_ user \_ Store". Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                              | Значение                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_хранилище CAPICOM Memory \_**</dt> </dl>                                                | Хранилище является хранилищем памяти. Любые изменения в содержимом хранилища не сохраняются.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**хранилище CAPICOM на \_ локальном \_ компьютере \_**</dt> </dl>                          | Это хранилище локального компьютера. Хранилища локальных компьютеров могут быть хранилищами для чтения и записи только в том случае, если у пользователя есть разрешения на чтение и запись. Если у пользователя есть разрешения на чтение и запись и если хранилище открыто для чтения и записи, то изменения в содержимом хранилища сохраняются.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_хранилище CAPICOM текущего \_ пользователя \_**</dt> </dl>                             | Хранилище является хранилищем текущего пользователя. Хранилище текущего пользователя может быть хранилищем для чтения и записи. Если это так, изменения в содержимом хранилища сохраняются.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ Active \_ Directory \_ пользовательское \_ хранилище**</dt> </dl> | Магазин является хранилищем Active Directory. Хранилища Active Directory могут быть открыты только в режиме только для чтения. Сертификаты нельзя добавлять в хранилища Active Directory или удалять из них.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_хранилище CAPICOM смарт- \_ карты \_ пользователя \_**</dt> </dl>                   | Магазин — это группа существующих смарт-карт. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*бчеккексистенце* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, будет ли CAPICOM пытаться получить доступ к ключу. Если **значение — true**, CAPICOM пытается получить доступ к ключу. Если ключ защищен пользователем или на смарт-карте или другом устройстве, может быть создано диалоговое окно. Значение по умолчанию равно **False**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод возвращает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
