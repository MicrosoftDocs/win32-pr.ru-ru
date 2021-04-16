---
description: Список структур, используемых с API управления безопасностью.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Структуры управления безопасностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664223"
---
# <a name="security-management-structures"></a>Структуры управления безопасностью

В этом разделе содержатся справочные страницы по следующим группам структур.

-   [Структуры управления политиками LSA](#lsa-policy-management-structures)
-   [Структуры вложений](#attachment-structures)
-   [Более безопасные структуры](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Структуры управления политиками LSA

Функции управления политиками [*локального центра безопасности*](/windows/desktop/SecGloss/l-gly) (LSA) используют следующие структуры.



| Структура                                                                       | Описание                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_сведения о проверке подлинности LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Содержит сведения о проверке подлинности для доверенного домена.                                                                                     |
| [**\_сведения о перечислении LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Содержит указатель на [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**\_атрибуты объекта \_ LSA**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Задает атрибуты соединения с объектом [**политики**](policy-object.md) .                                                       |
| [**\_список доменов, упоминаемых в LSA \_ \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Содержит сведения о доменах, на которые имеются ссылки в операции уточняющего запроса.                                                                      |
| [**\_имя переведено LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Содержит сведения об учетной записи, определяемой идентификатором безопасности.                                                                                   |
| [**\_ИД безопасности переведенного LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Содержит сведения о идентификаторе безопасности, определяющем учетную запись.                                                                                |
| [**LSA \_ переведено \_ SID2**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Содержит сведения о идентификаторе безопасности, определяющем учетную запись.                                                                                |
| [**\_сведения о доверии LSA \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Определяет домен.                                                                                                                          |
| [**\_строка Юникода \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Содержит строку и сведения о длине.                                                                                                 |
| [**\_ \_ сведения о домене учетной записи политики \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Используется для задания и запроса имени и идентификатора безопасности домена учетной записи системы.                                                                        |
| [**\_ \_ сведения о событиях аудита политики \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Используется для задания и запроса правил аудита системы.                                                                                            |
| [**\_ \_ сведения о ДОМЕНЕ DNS политики \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Используется для установки и запроса сведений о службе доменных имен (DNS) о основном домене, связанном с объектом [**политики**](policy-object.md) . |
| [**\_ \_ \_ сведения о роли сервера LSA политики \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Используется для задания и запроса роли сервера LSA.                                                                                              |
| [**\_ \_ сведения об изменении политики**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Используется для запроса сведений о времени создания и последнего изменения базы данных LSA.                                                  |
| [**\_ \_ сведения об учетной записи политики PD \_**](policy-pd-account-info.md)                     | Является устаревшей. Рабочие станции используют имя рабочей станции, за которым следует имя учетной записи $.                                                          |
| [**\_ \_ сведения о основном домене политики \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Является устаревшей. Вместо этого используйте **полициднсдомаининформатион** и структуру [**\_ DNS политики \_ домена \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) .           |
| [**\_ \_ сведения о проверке подлинности доверенного домена \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Используется для получения сведений о проверке подлинности для доверенного домена.                                                                             |
| [**\_ \_ полные \_ сведения о доверенном домене**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Используется для получения полных сведений о доверенном домене.                                                                                 |
| [**\_сведения о доверенном домене \_ \_ Basic**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Сведения о доверенном домене. Эта структура идентична [**\_ \_ сведениям о доверии LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**\_сведения о доверенном домене \_ \_ ex**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Используется для получения расширенных сведений о доверенном домене.                                                                                 |
| [**\_ \_ сведения об имени доверенного домена \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Используется для запроса или задания имени доверенного домена.                                                                                            |
| [**\_сведения о доверенном пароле \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Используется для запроса или установки пароля для доверенного домена.                                                                                       |
| [**\_ \_ сведения о СМЕЩЕНии доверенной POSIX \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Используется для запроса или задания значения, используемого для создания идентификаторов пользователей и групп POSIX.                                                             |



 

Следующие типы структуры устарели или зарезервированы для будущего использования:

-   **\_ \_ \_ сведения о полном запросе \_ аудита политики**
-   **\_ \_ \_ сведения о полном НАБОРе аудита \_ политики**
-   **\_ \_ сведения о журнале аудита политики \_**
-   **\_ \_ сведения о квоте по умолчанию для политики \_**
-   **\_ \_ сведения об источнике РЕПЛИКи политики \_**
-   **\_сведения о доверенных контроллерах \_**

## <a name="attachment-structures"></a>Структуры вложений

Следующие структуры используются вложенными библиотеками конфигурации безопасности и их вспомогательными функциями. Эти структуры определяются в Сцесвк. h.



| Структура                                                        | Описание                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ сведения о конфигурации сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Содержит сведения о конфигурации для службы.                                                                                               |
| [**\_Строка конфигурации \_ сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Содержит сведения о строке данных конфигурации.                                                                                        |
| [**\_ \_ сведения об анализе сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Содержит сведения об анализе.                                                                                                              |
| [**\_строка анализа \_ сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Содержит ключ, значение и длину значения для конкретной строки, заданной структурой [**\_ \_ сведений об анализе сцесвк**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) . |
| [**\_сведения о обратном вызове сцесвк \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Содержит указатель непрозрачной базы данных и указатели на функции обратного вызова для запроса, установки и бесплатной информации.                                          |



 

## <a name="safer-structures"></a>Более безопасные структуры

Следующие структуры и перечисляемые типы используются более безопасно. Они определены в Винсафер. h.



| Структура                                                                | Описание                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_свойства безопасного кода \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Содержит сведения об изображении кода и критерии, которые должны быть проверены на изображении кода. Массив этих структур передается функции [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) .                                                                  |
| [**\_заголовок безопасной идентификации \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Структура заголовков для [**более безопасной \_ \_ идентификации пути**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), [**более безопасной \_ хэш- \_ идентификации**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)и [**более безопасной структуры \_ \_ идентификации урлзоне**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) . |
| [**более безопасная \_ \_ Идентификация пути**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Содержит путь к проверяемому образу кода.                                                                                                                                                                                                      |
| [**БЕЗОПАСная \_ \_ Идентификация хэша**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Определяет хэш изображения кода для проверки.                                                                                                                                                                                                      |
| [**БЕЗОПАСная \_ \_ Идентификация урлзоне**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Определяет зону URL-адреса исходного изображения кода для проверки.                                                                                                                                                                                      |



 

 

 
