---
description: Извлекает сведения из сертификата.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Метод ICertificate2:: info'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665317"
---
# <a name="icertificate2getinfo-method"></a>Метод ICertificate2:: info

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод " **info** " извлекает сведения из [*сертификата*](../secgloss/c-gly.md).

## <a name="syntax"></a>Синтаксис


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инфотипе* \[ окне\]
</dt> <dd>

Значение перечисления [**\_ \_ \_ типа CAPICOM CERT info**](capicom-cert-info-type.md) , указывающее тип данных, извлекаемых из сертификата. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                     | Значение                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**\_ \_ \_ имя субъекта сведений об CAPICOM \_ CERT \_**</dt> </dl> | Возвращает отображаемое имя из субъекта сертификата.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**\_ \_ \_ \_ необычное имя поставщика сведений CAPICOM CERT \_**</dt> </dl>    | Возвращает отображаемое имя издателя сертификата.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**\_ \_ \_ \_ имя электронной почты субъекта сведений об CAPICOM CERT \_**</dt> </dl>    | Возвращает адрес электронной почты субъекта сертификата.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**CAPICOM \_ CERT \_ info \_ \_ имя электронной почты поставщика \_**</dt> </dl>       | Возвращает адрес электронной почты издателя сертификата.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**CAPICOM \_ \_ сведения о сертификате \_ субъект \_ имени участника-пользователя**</dt> </dl>                          | Возвращает имя участника-пользователя для субъекта сертификата. Представлено в CAPICOM 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**\_ \_ \_ имя участника-пользователя для заверителя сертификата \_ CAPICOM**</dt> </dl>                             | Возвращает имя участника-пользователя (UPN) издателя сертификата. Представлено в CAPICOM 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**\_ \_ \_ имя DNS субъекта сведений об \_ CAPICOM CERT \_**</dt> </dl>          | Возвращает DNS-имя субъекта сертификата. Представлено в CAPICOM 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**\_ \_ \_ \_ имя DNS-сервера поставщика сведений CAPICOM CERT \_**</dt> </dl>             | Возвращает DNS-имя издателя сертификата. Представлено в CAPICOM 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка, содержащая запрошенные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
