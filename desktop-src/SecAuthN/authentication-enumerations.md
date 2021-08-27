---
description: Перечисляет перечисления, используемые в API проверки подлинности.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Перечисления проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc42553074b79726c9d1b70bfc6292f4acf44df225fa1f86c7f7a28289ec8ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101324"
---
# <a name="authentication-enumerations"></a>Перечисления проверки подлинности

Перечисления проверки подлинности делятся на категории по использованию следующим образом.

-   [Перечисления управления учетными данными](#credentials-management-enumerations)
-   [Перечисления LSA](#lsa-enumerations)
-   [Перечисления поставщика сети](#network-provider-enumerations)
-   [Перечисления для поставщиков поддержки безопасности учетных данных (CredSSP)](#credential-security-support-provider-credssp-enumerations)
-   [Другие перечисления](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Перечисления управления учетными данными

Управление учетными данными использует следующие перечисления.



| Перечисление                                            | Описание                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_тип маршалирования для CRED \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Содержит типы учетных данных, которые можно маршалировать с помощью [**кредмаршалкредентиал**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) или распаковать с помощью [**кредунмаршалкредентиал**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).<br/> |
| [**\_Тип защиты \_ cred**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Указывает контекст безопасности, в котором шифруются учетные данные при использовании функции [**кредпротект**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) .<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Перечисления LSA

LSA использует следующие перечисления.



| Перечисление                                                                                   | Описание                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Тип отправки входа \_ Kerberos**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Перечисляет тип запрашиваемого входа.<br/>                                                                                                                                                                                                                  |
| [**\_ \_ тип буфера профиля \_ Kerberos**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Выводит тип возвращаемого профиля входа.<br/>                                                                                                                                                                                                                 |
| [**\_ \_ тип сообщения протокола \_ Kerberos**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Перечисляет типы сообщений, которые могут быть отправлены в пакет проверки подлинности [*Kerberos*](/windows/desktop/SecGloss/k-gly) путем вызова [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**\_ \_ \_ \_ тип записи конфликта доверия LSA лесов \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Определяет типы конфликтов, которые могут возникнуть между записями доверия между лесами LSA.<br/>                                                                                                                                                                           |
| [**\_ \_ \_ тип записи доверия LSA \_ лесов**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Определяет тип записи доверия леса LSA.<br/>                                                                                                                                                                                                           |
| [**\_ \_ тип сведений о ТОКЕНе LSA \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Задает уровни сведений, которые могут быть добавлены в маркер входа.<br/>                                                                                                                                                                                |
| [**\_ \_ \_ Тип отправки входа MSV1 \_ 0**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Перечисляет тип запрашиваемого входа.<br/>                                                                                                                                                                                                                  |
| [**\_ \_ \_ Тип буфера профиля MSV1 \_ 0**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Отображает тип возвращаемого профиля входа.<br/>                                                                                                                                                                                                                 |
| [**\_ \_ \_ Тип сообщения протокола MSV1 \_ 0**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Перечисляет типы сообщений, которые могут быть отправлены в [ \_ пакет проверки подлинности MSV1 0](msv1-0-authentication-package.md) путем вызова [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**\_ \_ класс сведений о домене политики \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Определяет тип сведений о домене политики.<br/>                                                                                                                                                                                                            |
| [**\_тип входа в систему безопасности \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Указывает тип входа, запрашиваемый процессом входа в систему.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Перечисления поставщика сети

Поставщик сети использует следующие перечисления.



| Перечисление                                                                       | Описание                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_класс расширенной \_ информации SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Тип перечисления, указывающий тип данных, которые необходимо задать или получить для [*пакета безопасности*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**\_тип имени \_ SECPKG**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Значение перечисления, указывающее тип имени, указанного для учетной записи.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Перечисления для поставщиков поддержки безопасности учетных данных (CredSSP)

CredSSP использует следующие перечисления.



| Перечисление                                          | Описание                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_Тип отправки \_ кредспп**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Указывает тип учетных данных, указанных структурой [**\_ cred CREDSSP**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) .<br/> |



 

## <a name="other-enumerations"></a>Другие перечисления

Ниже приведены другие перечисления, используемые при проверке подлинности.



| Перечисление                                                   | Описание                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_тип удостоверения**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Указывает тип идентификаторов для перечисления.<br/>                                                                                                                                                                  |
| [**\_ \_ Тип отправки входа \_ PKU2U**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Указывает тип сообщения для входа, переданного в [**структуру \_ \_ \_ входа сертификата S4U PKU2U**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) .<br/>                                                                                |
| [**\_ \_ состояние ЛКТ SECPKG \_ attr**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Указывает, является ли маркер последнего вызова функции [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) последним токеном от клиента.<br/>                               |
| [**\_класс SECPKG CRED \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Указывает тип учетных данных, используемых в контексте клиента. Перечисление [**\_ \_ класса SECPKG CRED**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) используется в структуре [**секпкгконтекст \_ крединфо**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) .<br/> |



 

 

