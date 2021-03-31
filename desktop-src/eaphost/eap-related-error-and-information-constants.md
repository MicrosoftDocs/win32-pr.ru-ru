---
title: Связанные с EAP константы и сведения об ошибках (Еафостеррор. h)
description: Отдельные группы констант, связанных с EAP и данными, общие для всех технологий API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071714"
---
# <a name="eap-related-error-and-information-constants"></a>Константы, относящиеся к EAP и сведения об ошибках

Отдельные группы констант, связанных с EAP и данными, общие для всех технологий API EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**\_сначала EAP E с \_ EAPHOST \_**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с EAPHost, будет вызвана между **EAP \_ e \_ EAPHost \_ First** и **\_ \_ \_ последней EAP e EAPHost**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**Последнее время в EAP \_ E \_ \_** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с EAPHost, будет вызвана между **EAP \_ e \_ EAPHost \_ First** и **\_ \_ \_ последней EAP e EAPHost**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**сначала требуется протокол EAP \_ I \_ \_** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Определяет границу информационных отчетов; все события, связанные с EAPHost, будут регистрироваться между **EAP \_ i \_ EAPHost \_ First** и с **EAP \_ i \_ EAPHost \_ последней**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**\_ \_ \_ Дата последнего протокола EAP I**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Определяет границу информационных отчетов; все события, связанные с EAPHost, будут регистрироваться между **EAP \_ i \_ EAPHost \_ First** и с **EAP \_ i \_ EAPHost \_ последней**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_ \_ хранилище сертификатов EAP \_ E \_ недоступно**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Ни средство проверки подлинности, ни одноранговые узлы не могут получить доступ к хранилищу сертификатов.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ не установлен метод метода EAPHOST EAP E \_**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Запрошенный метод EAP не установлен.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_ \_ \_ \_ \_ Сброс узла метода \_ EAP E EAPHOST сторонних**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



Узел стороннего метода не отвечает и перезапускается автоматически.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ еапкек \_ недоступен**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost не удается связаться с [клиентом принудительного применения карантина](/windows/desktop/NAP/nap-client-architecture) EAP (Кек) на клиенте с поддержкой [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_ \_ \_ неизвестное удостоверение "EAP E EAPHOST" \_**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost возвращает эту ошибку, если проверка подлинности после отправки удостоверения одноранговой сети завершается ошибкой.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_ \_ Ошибка проверки подлинности EAP E \_**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost возвращает эту ошибку при сбое проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ сбой СОГЛАСОВАНия EAP \_ с EAP**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost регистрирует это информационное событие, если клиент и сервер не настроены с совместимыми типами EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ Недопустимый пакет метода \_ EAP E**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Метод EAP получил пакет EAP, который не может быть обработан. Другое имя для **\_ метода EAP E в \_ \_ методе EAPHOST \_ \_** — недопустимый пакет **\_ метода EAP \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ \_ Удаленный \_ Недопустимый \_ пакет для EAP E**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost получил пакет, который не может быть обработан. Другое имя для **EAP \_ E \_ EAPHOST \_ Remote \_ Недопустимый \_ пакет** — **\_ Недопустимый \_ пакет EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ \_ неправильный формат XML EAP E EAPHOST \_** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Сбой проверки схемы конфигурации EAPHost.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**\_ \_ Конфигурация метода EAP \_ E \_ \_ не \_ поддерживает \_ единый вход**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 или более поздней версии: метод EAP не поддерживает единый вход (SSO) для указанной конфигурации.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_операция с методом протокола EAPHOST EAP E \_ \_ \_ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost возвращает эту ошибку, если настроенный метод EAP не поддерживает запрошенную операцию (вызов процедуры).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_Пользователь EAP \_ E \_ First**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Определяет границу отчетов об ошибках; любое сообщение об ошибке, связанное с пользователем, будет происходить между **\_ пользователем EAP e \_ \_ First** и **\_ \_ \_ последним пользователем EAP e**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**время \_ \_ последнего пользователя \_ EAP** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Определяет границу отчетов об ошибках; любое сообщение об ошибке, связанное с пользователем, будет происходить между **\_ пользователем EAP e \_ \_ First** и **\_ \_ \_ последним пользователем EAP e**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**\_ \_ \_ ПРЕДВАРИТЕЛЬный Пользователь EAP**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Определяет границу информационных отчетов; регистрация в журнале событий, связанных с EAP, будет осуществляться между **пользователем с EAP \_ i \_ \_ первым** и **\_ \_ \_ последним пользователем EAP i**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ последний пользователь EAP \_**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Определяет границу информационных отчетов; регистрация в журнале событий, связанных с EAP, будет осуществляться между **пользователем с EAP \_ i \_ \_ первым** и **\_ \_ \_ последним пользователем EAP i**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_сертификат EAP \_ E \_ user \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost не удалось найти сертификат пользователя для проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ \_ Недопустимый сертификат \_ пользователя EAP E**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Сертификат пользователя для проверки подлинности не имеет правильного набора расширенного использования ключа (EKU).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**\_ \_ \_ срок действия сертификата пользователя EAP E \_ истек**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



В EAPhost обнаружен сертификат пользователя с истекшим сроком действия.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ \_ отозванный сертификат пользователя EAP E \_**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Сертификат пользователя, используемый для проверки подлинности, был отозван.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_ \_ \_ \_ другая ошибка EAP E user \_ CERT**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



В сертификате пользователя, используемом для проверки подлинности, произошла неизвестная ошибка.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ сертификат пользователя EAP \_ E \_ отклонен** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



Средство проверки подлинности отклонило сертификат пользователя.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ \_ другая ошибка УЧЕТной записи пользователя EAP \_**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Ошибка EAP была получена после обмена удостоверениями, что указывает на вероятность проблемы с учетной записью пользователя, выполняющего проверку подлинности.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ \_ учетные данные пользователя EAP E \_ отклонены**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



Средство проверки подлинности отклонило учетные данные пользователя для аутентификации.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_пароль EAP \_ E \_ имя \_ пользователя \_ отклонен**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 или более поздней версии: проверка подлинности не удалась. Средство проверки подлинности отклонило учетные данные пользователя.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ без \_ считывателя смарт- \_ карт \_**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 или более поздней версии: устройство чтения смарт-карт не найдено.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_ \_ Сначала сервер EAP \_ E**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с сервером, возникает между сервером **EAP \_ e \_ \_ First** и **\_ сервером EAP e \_ \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_Сервер EAP \_ E \_ Last**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с сервером, возникает между сервером **EAP \_ e \_ \_ First** и **\_ сервером EAP e \_ \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ сертификат сервера EAP \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost не удалось найти сертификат сервера для проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ \_ Недопустимый сертификат \_ сервера EAP E**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Сертификат сервера, который пользователь выполняет для проверки подлинности, не имеет правильного набора расширенного использования ключа (EKU).


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_ \_ \_ \_ истек срок действия сертификата сервера EAP E**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



В EAPhost обнаружен сертификат сервера с истекшим сроком действия.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ сертификат сервера EAP \_ E \_ отозван**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Сертификат сервера, используемый для проверки подлинности, был отозван.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ другая \_ Ошибка сертификата сервера EAP E**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



В сертификате сервера произошла неизвестная ошибка.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ сначала пользователь EAP E \_ root \_ CERT \_**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с корневым сертификатом пользователя, будет находиться между **\_ \_ \_ \_ \_ первым** и корневым сертификатом пользователя **EAP \_ \_ \_ \_ \_** e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ корневой сертификат пользователя EAP E — \_ \_ \_ последний**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Определяет границу отчетов об ошибках; Любая ошибка, связанная с корневым сертификатом пользователя, будет находиться между **\_ \_ \_ \_ \_ первым** и корневым сертификатом пользователя **EAP \_ \_ \_ \_ \_** e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ корневой сертификат пользователя EAP E \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost не удалось найти сертификат в доверенном корневом хранилище сертификатов для проверки сертификата пользователя.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ \_ недопустимый корневой \_ сертификат пользователя \_ EAP E**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



Не удалось выполнить проверку подлинности, так как корневой сертификат, используемый для этой сети, недопустим.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_ \_ \_ срок действия корневого сертификата пользователя EAP E \_ \_ истек**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Истек срок действия доверенного корневого сертификата, необходимого для проверки сертификата пользователя.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ \_ сначала следует корневой \_ сертификат сервера EAP E \_**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Определяет границу отчетов об ошибках; все ошибки, связанные с корневым сертификатом сервера, происходят сначала между **\_ \_ \_ корневым \_ \_ сертификатом EAP e Server** и **\_ \_ \_ корневым \_ сертификатом \_ EAP e Server**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ последний корневой \_ сертификат сервера EAP E \_**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Определяет границу отчетов об ошибках; все ошибки, связанные с корневым сертификатом сервера, происходят сначала между **\_ \_ \_ корневым \_ \_ сертификатом EAP e Server** и **\_ \_ \_ корневым \_ сертификатом \_ EAP e Server**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ корневой сертификат сервера EAP E \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost не удалось найти корневой сертификат в доверенном корневом хранилище сертификатов для проверки сертификации сервера.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ \_ недопустимый корневой \_ сертификат сервера \_ EAP E** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



Не удалось выполнить проверку подлинности, так как сертификат сервера, необходимый для этой сети на компьютере сервера, является недопустимым.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ \_ требуется имя корневого \_ сертификата \_ сервера \_ EAP E**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



Не удалось выполнить проверку подлинности, так как для сертификата на сервере не указано имя сервера.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Существуют альтернативные имена для некоторых ошибок:

-   Другое имя для **\_ метода EAP E в \_ \_ методе EAPHOST \_ \_** — недопустимый пакет **\_ метода EAP \_ \_**.
-   Другое имя для **EAP \_ E \_ EAPHOST \_ Remote \_ Недопустимый \_ пакет** — **\_ Недопустимый \_ пакет EAP**.

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

 

