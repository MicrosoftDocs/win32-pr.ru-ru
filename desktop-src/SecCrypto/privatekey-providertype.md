---
description: Извлекает значение \_ \_ ПЕРЕЧИСЛЕНИЯ типа CAPICOM Prov, которое указывает тип поставщика.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: PrivateKey. ProviderType, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665178"
---
# <a name="privatekeyprovidertype-property"></a>PrivateKey. ProviderType, свойство

\[Свойство **ProviderType** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **ProviderType** извлекает значение перечисления [**\_ \_ типа CAPICOM Prov**](capicom-prov-type.md) , которое указывает тип поставщика.

## <a name="syntax"></a>Синтаксис


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**\_ \_ типа CAPICOM Prov**](capicom-prov-type.md) , указывающее тип поставщика. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ Full**</dt> </dl>                 | Полный [*поставщик служб шифрования*](../secgloss/c-gly.md) [*RSA*](../secgloss/r-gly.md) (CSP). Этот тип поставщика поддерживает [*цифровые подписи*](../secgloss/d-gly.md) и [*Шифрование*](../secgloss/e-gly.md)данных.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SIG**</dt> </dl>                    | Подмножество CSP RSA, которое поддерживает только те функции и алгоритмы, которые необходимы для хэширования и цифровых подписей.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | CSP [*стандарта цифровой подписи*](../secgloss/d-gly.md) (DSS). Этот тип поставщика поддерживает только хэши и Цифровые подписи. DSS использует [*алгоритм цифровых подписей*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Prov \_ Fortezza**</dt> </dl>                  | CSP, содержащий криптографические протоколы и алгоритмы, принадлежащие [*национальным институтам стандартов и технологий*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Exchange**</dt> </dl>        | CSP, предназначенный для криптографических потребностей приложения Microsoft Exchange Mail и других приложений, совместимых с Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ Prov \_ SSL**</dt> </dl>                                 | CSP, поддерживающий протокол [*SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SChannel**</dt> </dl>     | CSP, поддерживающий протоколы RSA и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS \_ DH**</dt> </dl>                       | CSP, поддерживающий [*стандартную поддержку цифровых подписей*](../secgloss/d-gly.md) (DSS) и протокол [*Диффи-Хелмана*](../secgloss/d-gly.md) .<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ , \_ подпись**</dt> </dl>    | CSP, который поддерживает функции алгоритма цифровых подписей на основе эллиптических кривых (ECDSA) и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ екнра \_ SIG**</dt> </dl>    | CSP, поддерживающий эллиптическую кривую Nyberg-Rueppel аналоговые (ЕКНРА) функции и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ Full**</dt> </dl> | CSP, поддерживающий полное значение ECDSA.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ екнра \_ Full**</dt> </dl> | CSP, поддерживающий полную ЕКНРА.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ DH \_ SChannel**</dt> </dl>        | CSP, поддерживающий протоколы [*Диффи-Хелмана*](../secgloss/d-gly.md) и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ спирус \_ Линкс**</dt> </dl>     | CSP, поддерживающий устройство СПИРУС Линкс Card.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ РНГ**</dt> </dl>                                 | CSP, обрабатывающий генерацию случайных чисел.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ sec**</dt> </dl>              | CSP, обеспечивающий безопасность Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ заменить \_ OWF**</dt> </dl>        | CSP, поддерживающий замену способа, в котором односторонние форматы (Овфс) создаются из паролей.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | CSP, поддерживающий цифровые подписи и шифрование данных с помощью алгоритма [*AES*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
