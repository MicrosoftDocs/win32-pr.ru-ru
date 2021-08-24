---
description: Описание кодов ошибок 8200-8999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Коды системных ошибок (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: e9fd65025c3d51575cb0ece83cba14e0c62980d11a60ec6cb351919b6c7714c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572964"
---
# <a name="system-error-codes-8200-8999"></a>Коды системных ошибок (8200-8999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 8200 – 8999. Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**Ошибка \_ DS \_ не \_ установлена**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Произошла ошибка при установке службы каталогов. Дополнительные сведения см. в журнале событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**Ошибка проверки \_ членства в DS в \_ \_ \_ локальной среде**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Служба каталогов проверила членство в группах локально.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**Ошибка \_ DS \_ без \_ атрибута \_ или \_ значения**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



Указанный атрибут или значение службы каталогов не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**Ошибка \_ DS \_ недопустимого \_ \_ синтаксиса атрибута**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



В службе каталогов указан недопустимый синтаксис атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**\_тип атрибута ошибки DS не \_ \_ \_ определен**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



Тип атрибута, указанный для службы каталогов, не определен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**\_существует ошибка \_ атрибута \_ или \_ значения \_ DS**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



Указанный атрибут или значение службы каталогов уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**Ошибка \_ DS \_ Busy**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



Служба каталогов занята.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**Ошибка \_ DS \_ недоступна**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



Служба каталогов недоступна.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**Ошибка \_ DS \_ — \_ не \_ выделено ни одного RID**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Служба каталогов не смогла выделить относительный идентификатор.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**Ошибка \_ DS \_ , \_ другие \_ идентификаторы RID**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Служба каталогов исчерпала пул относительных идентификаторов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**Ошибка \_ DS \_ — \_ неправильный \_ владелец роли**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



Не удалось выполнить запрошенную операцию, так как служба каталогов не является главной для этого типа операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**Ошибка \_ при \_ инициализации ридмгр DS \_ \_**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Службе каталогов не удалось инициализировать подсистему, которая выделяет относительные идентификаторы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**Ошибка \_ при \_ \_ нарушении класса obj DS \_**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



Запрошенная операция не удовлетворяет одному или нескольким ограничениям, связанным с классом объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**Ошибка \_ DS \_ \_ не удается \_ на \_ неконечных**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Служба каталогов может выполнить запрошенную операцию только для конечного объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**Ошибка \_ DS не \_ удается \_ на \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Службе каталогов не удается выполнить запрошенную операцию с атрибутом RDN объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**Ошибка \_ DS \_ не \_ удается \_ \_ класс obj класса mod**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Служба каталогов обнаружила попытку изменить класс объекта объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**Ошибка \_ \_ перемещения перекрестной \_ модели DOM для \_ DS \_**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Не удалось выполнить запрошенную операцию междоменного перемещения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**Ошибка \_ \_ сборки мусора DS \_ не \_ доступна**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Не удалось связаться с сервером глобального каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_Общая \_ Политика ошибок**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



Объект политики является общим и может быть изменен только в корне.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_объект политики \_ ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



Объект политики не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_Политика ошибок \_ только \_ в \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



Запрошенные сведения о политике находятся только в службе каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**\_продвижение ошибки \_ активно**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Повышение роли контроллера домена сейчас активно.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**Ошибка \_ без \_ повышения \_ активности**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Повышение роли контроллера домена сейчас неактивно.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**Ошибка \_ \_ операций DS Operations \_**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Произошла ошибка операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**Ошибка \_ \_ протокола DS \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Произошла ошибка протокола.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**\_ \_ превышена ошибка тимелимит DS \_**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



Превышено предельное время для этого запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**\_ \_ превышена ошибка сизелимит DS \_**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



Превышен предельный размер для этого запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_ \_ \_ превышен предел администратора DS \_**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Превышено административное ограничение для этого запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**Ошибка \_ DS \_ Compare \_ false**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



Ответ сравнения был ложным.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**Ошибка \_ DS \_ Compare \_ true**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



Ответ сравнения был истинным.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**Ошибка \_ \_ \_ \_ не поддерживается метод проверки подлинности DS \_**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



Запрошенный метод проверки подлинности не поддерживается сервером.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**\_ \_ требуется строгая \_ Проверка подлинности DS \_**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Для этого сервера требуется более безопасный метод проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**Ошибка \_ \_ \_ проверки подлинности DS**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Недопустимая проверка подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**Ошибка \_ \_ проверки подлинности DS \_**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Неизвестный механизм проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Ссылка на ошибку \_ DS \_**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



С сервера была возвращена отсылка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**Ошибка \_ \_ недоступности \_ расширения критерий DS \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



Сервер не поддерживает запрошенное критическое расширение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**\_ \_ требуется конфиденциальность DS \_**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Для этого запроса требуется безопасное соединение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**Ошибка \_ \_ \_ несоответствия DS**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Неуместное сопоставление.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**Ошибка \_ \_ нарушения ограничения \_ DS**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Произошло нарушение ограничения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**Ошибка \_ DS \_ . \_ такой \_ объект отсутствует**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



На сервере отсутствует такой объект.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**Ошибка \_ \_ псевдонима \_ DS**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Существует проблема с псевдонимом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**Ошибка \_ DS с \_ недопустимым \_ \_ синтаксисом DN**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Указан недопустимый синтаксис DN.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**\_ \_ \_ Конечная ошибка DS**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



Объект является конечным объектом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**Ошибка \_ \_ псевдонима DS, \_ \_ связанная с ошибкой Deref**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Существует проблема разыменования псевдонима.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**\_ \_ не будет \_ выполнена ошибка DS \_**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Сервер не будет обрабатывать запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**Ошибка \_ \_ обнаружения циклов DS \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Обнаружен цикл.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**Ошибка \_ \_ именования \_ DS**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Существует нарушение именования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**\_результаты объекта "ошибка DS" \_ \_ \_ слишком \_ велики**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Результирующий набор слишком велик.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**Служба "ошибки \_ DS" \_ влияет на \_ несколько \_ DSA**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



Операция влияет на несколько DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**Ошибка \_ \_ сервера DS \_**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



Сервер не работает.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**Ошибка \_ \_ локальной \_ ошибки DS**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Произошла локальная ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**Ошибка \_ \_ кодирования DS \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Произошла ошибка кодирования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**Ошибка \_ \_ декодирования DS \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Произошла ошибка декодирования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**Ошибка \_ \_ \_ неизвестного фильтра DS**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Не удается распознать фильтр поиска.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**Ошибка \_ параметра службы DS \_ \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Один или несколько параметров недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**Ошибка \_ DS \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Указанный метод не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**Ошибка \_ DS \_ . \_ результаты не \_ возвращены**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Результаты не возвращены.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**Ошибка \_ \_ управления DS \_ не \_ найдена**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Указанный элемент управления не поддерживается сервером.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**Ошибка \_ \_ клиентский \_ цикл DS**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Клиент обнаружил цикл ссылок.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_ \_ \_ превышен предел ссылок DS \_**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



Предустановленный предел ссылок был превышен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**Ошибка \_ \_ управления сортировкой DS \_ \_**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



Для поиска требуется элемент управления SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**Ошибка \_ \_ диапазона смещения для DS \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Результаты поиска превышают указанный диапазон смещений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**Ошибка \_ DS \_ ридмгр \_ Disabled**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Служба каталогов обнаружила, что подсистема, которая выделяет относительные идентификаторы, отключена. Это может произойти в качестве защитного механизма, когда система определяет значительную часть относительных идентификаторов (RID). <https://go.microsoft.com/fwlink/p/?linkid=228610>Рекомендуемые шаги диагностики и процедура повторного включения создания учетной записи см. в разделе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**\_корень DS \_ ошибок \_ должен \_ быть \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



Корневой объект должен быть заголовком контекста именования. Корневой объект не может иметь экземпляр родителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**Ошибка \_ при \_ добавлении \_ реплики DS \_**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Не удается выполнить операцию добавления реплики. Для создания реплики контекст именования должен быть записываемым.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**Ошибка \_ DS \_ Атри \_ Not \_ DEF \_ в \_ схеме**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Ссылка на атрибут, который не определен в схеме.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_ \_ \_ превышен максимальный размер obj \_ \_ -службы DS**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



Превышен максимальный размер объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**Ошибка \_ доменного \_ \_ \_ имени obj \_ DS**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Предпринята попытка добавить в каталог объект с именем, которое уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**Ошибка \_ DS \_ . \_ не \_ определено RDN \_ в \_ схеме**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Предпринята попытка добавить объект класса, не имеющий RDN, определенного в схеме.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**Ошибка \_ \_ RDN DS \_ не \_ соответствует \_ схеме соответствия**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Предпринята попытка добавить объект с помощью RDN, который не является RDN, определенным в схеме.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**Ошибка \_ DS \_ . \_ запрошенные \_ АТТС не \_ найдены**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Ни один из запрошенных атрибутов не был найден для объектов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**Ошибка \_ \_ \_ \_ небольшого буфера пользователя \_ DS**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



Буфер пользователя слишком мал.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**Ошибка \_ DS \_ Атри \_ \_ не включена \_ в \_ obj**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



Атрибут, указанный в операции, отсутствует в объекте.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**Ошибка \_ DS \_ недопустимой \_ \_ операции mod**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Недопустимая операция изменения. Некоторые аспекты изменения не разрешены.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**Ошибка в OBJ-файле \_ DS \_ \_ слишком \_ большой**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



Указанный объект слишком велик.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**\_ \_ Недопустимый \_ тип экземпляра ошибки DS \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Указан недопустимый тип экземпляра.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**\_требуется ошибка \_ мастердса \_ DS**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



Эта операция должна выполняться на главном DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_ \_ \_ требуется класс объекта DS службы "ошибка" \_**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



Необходимо указать атрибут класса объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**в \_ DS \_ отсутствует \_ обязательный \_ Атри**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Отсутствует обязательный атрибут.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**Ошибка \_ DS \_ Атри, \_ не \_ DEF \_ для \_ класса**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Предпринята попытка изменить объект, включив в него атрибут, который не является допустимым для его класса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**Ошибка \_ DS \_ Атри \_ уже \_ существует**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



Указанный атрибут уже существует в объекте.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**Ошибка \_ DS \_ не \_ удается \_ Добавить \_ значения Атри**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



Указанный атрибут не существует или не имеет значений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**Ошибка \_ с \_ единственным \_ значением \_ в DS**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Для атрибута было указано несколько значений, которые могут иметь только одно значение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**Ошибка \_ \_ ограничения диапазона \_ DS**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Значение атрибута не находится в допустимом диапазоне значений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**Ошибка \_ DS \_ Атри \_ Val \_ уже \_ существует**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



Указанное значение уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**Ошибка \_ DS не \_ удается \_ REM \_ отсутствует \_ Атри**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Невозможно удалить атрибут, так как он отсутствует в объекте.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**Ошибка \_ DS не \_ удается \_ REM \_ отсутствует \_ Атри \_ Val**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



Значение атрибута не может быть удалено, поскольку оно отсутствует в объекте.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**Ошибка \_ \_ корня DS \_ \_ не может быть \_ субреф**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



Указанный корневой объект не может быть субреф.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**Ошибка \_ DS \_ без \_ цепочек**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Цепочки не разрешены.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**Ошибка \_ DS \_ без \_ цепочек \_ оценки**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



Вычисление цепочек не разрешено.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**Ошибка \_ DS \_ без \_ родительского \_ объекта**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



Эта операция не может быть выполнена, т.к. родитель объекта либо не подтвержден, либо удален.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**\_ \_ родительский объект ошибки DS \_ является \_ \_ псевдонимом**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



Наличие родителя, который является псевдонимом, не допускается. Псевдонимы являются конечными объектами.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**Ошибка \_ DS не \_ удается \_ смешать \_ главный \_ и \_ представители**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



Объект и родитель должны иметь один и тот же тип: как шаблоны, так и обе реплики.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**\_ \_ присутствуют дочерние элементы DS \_**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



Невозможно выполнить операцию, так как существуют дочерние объекты. Эта операция может быть выполнена только для конечного объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**Ошибка \_ \_ obj \_ не \_ найдена**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Объект каталога не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**Ошибка \_ в \_ псевдониме \_ obj \_ DS**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Отсутствует псевдоним объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**Ошибка \_ в \_ синтаксисе неверного \_ имени DS \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



Недопустимый синтаксис имени объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**Ошибка \_ \_ псевдонима \_ DS \_ , указывающая на \_ псевдоним**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Псевдоним не может ссылаться на другой псевдоним.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**Ошибка \_ DS не удается выявление \_ \_ \_ псевдонима**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Невозможно разыменование псевдонима.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**Ошибка \_ DS \_ вне \_ \_ области**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



Операция вне области действия.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**Ошибка \_ \_ удаления объекта \_ DS \_**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



Невозможно продолжить операцию, так как объект находится в процессе удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**Ошибка \_ DS не \_ удается \_ удалить \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Не удается удалить объект DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**Ошибка \_ DS \_ Generic \_ Error**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Произошла ошибка службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**Ошибка \_ DSA DS, \_ \_ должна \_ быть \_ \_ хозяином int**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



Эта операция может быть выполнена только для внутреннего основного объекта DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**Ошибка \_ класса DS, \_ \_ не являющийся \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



Объект должен иметь класс DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**Ошибка \_ \_ доступа инсуфф \_ DS \_**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Недостаточно прав доступа для выполнения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**Ошибка \_ DS — \_ Недопустимый \_ старший**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Не удается добавить объект, поскольку родительский элемент не находится в списке возможных старших элементов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**Ошибка \_ \_ атрибута DS \_ , принадлежащего \_ \_ SAM**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



Доступ к атрибуту не разрешен, так как атрибут принадлежит диспетчеру учетных записей безопасности (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**Ошибка \_ \_ имя DS \_ слишком \_ много \_ частей**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



Имя содержит слишком много частей.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**Ошибка \_ \_ \_ слишком \_ длинное имя DS**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



Слишком длинное имя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**Ошибка \_ \_ \_ \_ слишком \_ длинное значение имени DS**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



Значение имени слишком длинное.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**Ошибка \_ при \_ \_ разборе имени DS**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



Произошла ошибка службы каталогов при анализе имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**Ошибка \_ \_ \_ \_ неизвестного типа имени DS**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



Служба каталогов не может получить тип атрибута для имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**Ошибка \_ DS \_ \_ , не \_ объект**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



Имя не определяет объект; имя идентифицирует фантом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ОШИБКИ \_ в \_ секунду \_ , \_ слишком \_ короткий**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



Слишком короткий дескриптор безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимых DESC в секунду**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



Недопустимый дескриптор безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**Ошибка \_ DS \_ без \_ удаленного \_ имени**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Не удалось создать имя для удаленного объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**Ошибка \_ DS \_ субреф \_ должна \_ иметь \_ родителя**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Должен существовать родительский элемент нового субреф.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**Ошибка \_ доменных служб Active Directory ( \_ NCNAME) \_ должна \_ быть \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



Объект должен быть контекстом именования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**Ошибка \_ DS \_ не \_ удается \_ Добавить \_ только систему**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



Не разрешается добавлять атрибут, принадлежащий системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**класс DS с ОШИБКАми \_ \_ \_ должен \_ быть \_ конкретным**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



Класс объекта должен быть структурным; нельзя создать экземпляр абстрактного класса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**Ошибка \_ DS \_ Недопустимая \_ ДМД**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



Не удалось найти объект схемы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**Ошибка \_ - \_ \_ идентификатор GUID DS obj \_ существует**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Локальный объект с этим идентификатором GUID (Мертвое или неактивное) уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**Ошибка \_ DS \_ , \_ не \_ посмотрите**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



Операция не может быть выполнена на обратной ссылке.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**Ошибка \_ DS \_ без \_ CROSSREF \_ для \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



Перекрестная ссылка для указанного контекста именования не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**Ошибка \_ при \_ завершении работы DS \_**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



Не удалось выполнить операцию, так как служба каталогов завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**Ошибка \_ \_ неизвестной \_ операции DS**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



Недопустимый запрос службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**Ошибка \_ DS, \_ Недопустимая \_ \_ владелец роли**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Не удалось прочитать атрибут владельца роли.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**Ошибка \_ DS \_ не удалось \_ Contact \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



Ошибка требуемой операции FSMO. Нет связи с текущим владельцем FSMO.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**Ошибка \_ \_ \_ \_ переименования DN перекрестного сетевого контроллера в DS \_**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



Изменение DN в контексте именования не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**Ошибка \_ DS \_ не \_ удается \_ только система Mod \_**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



Невозможно изменить атрибут, так как он принадлежит системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**Ошибка \_ \_ репликатора \_ DS**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Эту функцию могут выполнять только репликатор.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**Ошибка \_ в \_ классе obj DS \_ \_ не \_ определена**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



Указанный класс не определен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**Ошибка \_ - \_ \_ подкласс для класса obj \_ DS \_**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



Указанный класс не является подклассом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**Ошибка \_ \_ \_ Недопустимая ссылка на имя DS \_**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



Недопустимая ссылка на имя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**\_существует ошибка \_ перекрестной \_ ссылки DS \_**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Перекрестная ссылка уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ОШИБКА DS не удается присвоить \_ \_ \_ \_ главному узлу Del \_**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



Удаление главной перекрестной ссылки не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**сообщение об ошибке поддерево "ошибка" \_ \_ \_ \_ не \_ \_ head NC**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Уведомления поддерева поддерживаются только в заголовках NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**\_ \_ \_ \_ слишком сложный фильтр уведомлений DS \_ с ошибками**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



Слишком сложный фильтр уведомлений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**Ошибка \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Ошибка обновления схемы: повторяющееся RDN.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**Ошибка \_ DS \_ DUP \_ OID**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Сбой обновления схемы: дублирующийся OID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**Ошибка \_ DS \_ DUP \_ MAPI \_ ID**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Сбой обновления схемы: дублирующийся идентификатор MAPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**Ошибка \_ DS \_ DUP \_ Schema \_ ID \_ GUID**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Сбой обновления схемы: идентификатор GUID схемы дублируется.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**Ошибка \_ DS \_ DUP \_ , \_ отображаемое \_ имя LDAP**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Ошибка обновления схемы: повторяющееся отображаемое имя LDAP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**Ошибка \_ \_ проверки семантического \_ Атри DS \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Сбой обновления схемы: диапазон-меньше, чем диапазон верхнего уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**Ошибка \_ при \_ несоответствии синтаксиса DS \_**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Не удалось обновить схему: несовпадение синтаксиса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**Ошибка \_ DS \_ Exists \_ в \_ должен \_ иметь**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Сбой удаления схемы: атрибут используется в, который должен содержать.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_ \_ \_ в \_ возможно \_ , существует ошибка DS в**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Сбой удаления схемы: в возможно, используется атрибут, который содержит.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_ \_ несуществующая ошибка \_ DS \_**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Ошибка обновления схемы: атрибут в, возможно, не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_НЕсуществующая ошибка DS \_ \_ должна \_ иметь**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Не удалось обновить схему: атрибут в "" должно быть не существует ".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**Ошибка \_ при \_ \_ проверке AUX \_ CLS \_ в DS**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Сбой обновления схемы: класс в списке AUX-Class не существует или не является вспомогательным классом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**Ошибка \_ DS, \_ несуществующая \_ ПОСС \_ SUP**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Сбой обновления схемы: класс в ПОСС-старших не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ОШИБКА подсистемы проверки подсистемы \_ CLS в DS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Сбой обновления схемы: класс в списке списках subClassOf не существует или не удовлетворяет правилам иерархии.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**Ошибка \_ DS \_ неверного \_ \_ \_ синтаксиса идентификатора RDN Атри \_**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Сбой обновления схемы: RDN-Атри-ID имеет неправильный синтаксис.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_ \_ \_ в \_ AUX \_ CLS существует ошибка DS**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Сбой удаления схемы: класс используется в качестве вспомогательного класса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**\_ \_ \_ в \_ подсистеме \_ CLS существует ошибка DS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Сбой удаления схемы: класс используется как подкласс.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_ \_ \_ в \_ ПОСС \_ SUP существует ошибка DS**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Сбой удаления схемы: класс используется как ПОСС старший.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**Ошибка \_ DS \_ рекалксчема \_**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Сбой обновления схемы при повторном вычислении кэша проверки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**Ошибка \_ при \_ \_ удалении дерева \_ DS \_**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



Удаление дерева не завершено. Чтобы продолжить удаление дерева, необходимо снова выполнить запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**Ошибка \_ при \_ \_ удалении DS**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Не удалось выполнить запрошенную операцию удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**Ошибка \_ \_ \_ \_ ИД требования схемы DS \_ Атри**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Не удается прочитать идентификатор класса управляемых классов для записи схемы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**Ошибка \_ DS \_ Bad \_ Атри \_ \_ синтаксис схемы**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



Схема атрибута имеет неверный синтаксис.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**Ошибка \_ DS не \_ удается \_ кэшировать \_ Атри**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



Не удалось кэшировать атрибут.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**Ошибка \_ DS не \_ удается \_ кэшировать \_ класс**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



Не удалось кэшировать класс.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**Ошибка \_ DS \_ не \_ удается \_ удалить \_ кэш Атри**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



Не удалось удалить атрибут из кэша.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**Ошибка \_ DS \_ не \_ удается \_ удалить \_ кэш класса**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



Не удалось удалить класс из кэша.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**Ошибка \_ DS не \_ удается \_ получить \_ различающееся имя**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



Не удалось прочитать атрибут различающегося имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**Ошибка \_ DS \_ Missing \_ супреф**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



No superior reference has been configured for the directory service (Для службы каталогов не была настроена ссылка верхнего уровня). Поэтому служба каталогов не может выдавать ссылки на объекты, находящиеся за пределами этого леса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**Ошибка \_ DS не \_ удается \_ получить \_ экземпляр**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



Не удалось получить атрибут типа экземпляра.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**Ошибка \_ \_ \_ несогласованности кода DS**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Произошла внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**Ошибка \_ \_ базы данных \_ DS**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Произошла ошибка базы данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**\_ \_ отсутствует GOVERNSID DS \_**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Отсутствует атрибут GOVERNSID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**в \_ DS обнаружено \_ \_ непредвиденных \_ Атри**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Отсутствует ожидаемый атрибут.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**Ошибка \_ в \_ DS \_ NCNAME \_ отсутствует \_ ссылка CR**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



В указанном контексте именования отсутствует перекрестная ссылка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**Ошибка \_ \_ проверки безопасности \_ DS \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Произошла ошибка проверки безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_схема DS \_ ошибки \_ не \_ загружена**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



Схема не загружена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**Ошибка \_ при выделении \_ схемы DS \_ \_**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Не удалось выделить схему. Убедитесь, что на компьютере недостаточно памяти.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**Ошибка \_ \_ \_ \_ синтаксиса требования схемы DS Атри \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Не удалось получить необходимый синтаксис для схемы атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**Ошибка \_ DS \_ гкверифи \_**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Сбой проверки глобального каталога. Глобальный каталог недоступен или не поддерживает эту операцию. В настоящее время часть каталога недоступна.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**Ошибка \_ \_ \_ несоответствия схемы DS DRA \_**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



Сбой операции репликации из-за несоответствия схем между вовлеченными серверами.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**Ошибка \_ DS не \_ удается \_ найти \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Не удалось найти объект DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**Ошибка \_ DS не \_ удается \_ найти \_ Ожидаемый \_ NC**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Не удалось найти контекст именования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**Ошибка \_ DS не \_ удается \_ найти \_ NC \_ в \_ кэше**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Не удалось найти контекст именования в кэше.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**Ошибка \_ DS не \_ удается \_ получить \_ дочерний элемент**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Не удалось получить дочерний объект.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**Ошибка \_ при \_ \_ недопустимом \_ изменении безопасности DS**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



Это изменение не было разрешено в целях безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**Ошибка \_ DS не \_ удается \_ заменить \_ скрытый \_ REC**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



Операция не может заменить скрытую запись.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**Ошибка \_ DS — \_ файл неправильной \_ иерархии \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



Недопустимый файл иерархии.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**Ошибка \_ \_ \_ \_ при выполнении таблицы иерархии сборки DS \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Не удалось выполнить сборку таблицы иерархии.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**Ошибка \_ в \_ \_ параметре конфигурации DS \_**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



В реестре отсутствует параметр конфигурации каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**Ошибка \_ \_ при подсчете \_ \_ индексов адресной книги \_ DS**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Попытка подсчитать индексы адресной книги не удалась.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**Ошибка \_ \_ \_ \_ malloc \_ при выполнении таблицы иерархии DS**
</dt> <dd> <dl> <dt>

8429 (со 0x20)
</dt> <dt>



Не удалось выделить таблицу иерархии.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**Ошибка \_ \_ внутреннего \_ сбоя DS**
</dt> <dd> <dl> <dt>

8430 (0x20)
</dt> <dt>



Произошла внутренняя ошибка службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**Ошибка \_ DS \_ Unknown \_ Error**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



Произошла неизвестная ошибка службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**\_корень DS \_ ошибки \_ требует указания \_ класса \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Для корневого объекта требуется класс "Top".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**\_службы DS, которые \_ отказывается от \_ \_ ролей FSMO**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Сервер каталогов завершает работу и не может стать владельцем новых ролей операций с плавающей операцией с одним хозяином.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**в \_ DS \_ отсутствуют \_ \_ Параметры FSMO**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



В службе каталогов отсутствуют обязательные сведения о конфигурации, и ей не удается определить принадлежность ролей операций с плавающей операцией с одним хозяином.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**Ошибка \_ DS \_ при \_ \_ суррендерии \_ ролей**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



Службе каталогов не удалось переместить владение одной или несколькими ролями операций с плавающей точкой на другие серверы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**Ошибка \_ \_ Generic DS DRA \_**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



Сбой операции репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**Ошибка \_ \_ \_ недопустимого параметра DS DRA \_**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Для этой операции репликации указан недопустимый параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**Ошибка \_ " \_ занят DS DRA" \_**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



Служба каталогов слишком занята для завершения операции репликации в данный момент.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**Ошибка \_ DS \_ DRA с \_ неправильным \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



Указано недопустимое различающееся имя для этой операции репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**Ошибка \_ \_ \_ неверного \_ NC DRA DS**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



Для этой операции репликации указан недопустимый контекст именования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**Ошибка \_ доменных служб DS \_ DRA \_ с именем \_**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



Различающееся имя, указанное для этой операции репликации, уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**Ошибка \_ \_ \_ внутренней ошибки DS DRA \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



В системе репликации произошла внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**Ошибка \_ DS \_ DRA не \_ согласуется с \_ деревом каталогов**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



При выполнении операции репликации возникла несогласованность базы данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**Ошибка \_ \_ \_ при подключении DS DRA \_**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



Не удалось связаться с сервером, указанным для этой операции репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**Ошибка \_ \_ \_ неправильного \_ типа экземпляра DRA DS \_**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



Операция репликации обнаружила объект с недопустимым типом экземпляра.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**Ошибка \_ \_ \_ вне \_ \_ памяти DS DRA**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



Операции репликации не удалось выделить память.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**Ошибка \_ \_ \_ электронной почты DS DRA \_**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



Операция репликации обнаружила ошибку в почтовой системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**Ошибка \_ " \_ ссылка DS DRA" \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Сведения о ссылке репликации для целевого сервера уже существуют.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**Ошибка \_ " \_ ссылка DS DRA \_ \_ не \_ найдена"**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Сведения о ссылке репликации для целевого сервера не существуют.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**Ошибка \_ DS \_ DRA \_ obj \_ — \_ \_ источник представителя**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Невозможно удалить контекст именования, так как он реплицируется на другой сервер.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**Ошибка \_ \_ \_ базы данных DS DRA \_**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



При выполнении операции репликации произошла ошибка базы данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**Ошибка \_ DS \_ DRA \_ без \_ реплики**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Контекст именования находится в процессе удаления или не реплицируется с указанного сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**Ошибка \_ \_ \_ отказа в доступе DS DRA \_**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Отказано в доступе к репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**Ошибка \_ DS \_ DRA \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



Запрошенная операция не поддерживается этой версией службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**Ошибка \_ при \_ \_ отмене RPC DRA DS \_**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



Удаленный вызов процедуры репликации был отменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**Ошибка \_ " \_ источник DRA DS \_ \_ отключен"**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Исходный сервер в настоящий момент отвергает запросы на репликацию.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**Ошибка \_ при \_ \_ отключении приемника DRA DS \_**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Целевой сервер в настоящий момент отвергает запросы на репликацию.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**Ошибка \_ при \_ \_ конфликте имен DS DRA \_**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



Сбой операции репликации из-за конфликта имен объектов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**Ошибка \_ при \_ \_ \_ повторной установке источника DRA DS**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



Источник репликации был переустановлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**Ошибка \_ DS \_ DRA с \_ отсутствующим \_ родителем**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



Сбой операции репликации из-за отсутствия обязательного родительского объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**Ошибка \_ DS \_ DRA с \_ вытеснением**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



Операция репликации была прервана.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**Ошибка \_ при \_ \_ \_ синхронизации несинхронизированных DS DRA**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



Попытка синхронизации репликации была прервана из-за отсутствия обновлений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**Ошибка \_ при \_ \_ завершении работы DS DRA**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



Операция репликации была прервана, так как система завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**Ошибка \_ при \_ \_ \_ частичном наборе несовместимости DS DRA \_**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Попытка синхронизации завершилась сбоем, так как целевой контроллер домена ожидает синхронизации новых частичных атрибутов из источника. Это состояние является нормальным, если Последнее изменение схемы изменило набор атрибутов partial. Целевой частичный набор атрибутов не является подмножеством частичного набора атрибутов источника.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**Ошибка \_ \_ \_ : источник DRA DS \_ является \_ частичной \_ репликой**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Попытка синхронизации репликации завершилась сбоем, так как Главная реплика попыталась выполнить синхронизацию из частичной реплики.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**Ошибка \_ \_ \_ \_ при подключении екстн DS \_ DRA**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Для сервера, указанного для этой операции репликации, установлен контакт, но серверу не удалось связаться с дополнительным сервером, необходимым для завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**Ошибка \_ при \_ установке \_ несоответствия схемы службы DS \_**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



Версия схемы службы каталогов исходного леса несовместима с версией службы каталогов на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**Ошибка \_ DS \_ DUP \_ Link \_ ID**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Сбой обновления схемы: атрибут с таким идентификатором связи уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**Ошибка \_ при \_ \_ \_ разрешении имени DS**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Преобразование имен: Общая ошибка обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**Ошибка \_ \_ имени DS \_ \_ не \_ найдена**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Преобразование имени: не удалось найти имя или недостаточно прав для просмотра имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**Ошибка \_ \_ имени DS \_ не \_ является \_ уникальной**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Преобразование имени: входное имя, сопоставленное более чем с одним выходным именем.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**Ошибка \_ имени DS, \_ \_ Ошибка \_ без \_ сопоставления**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Преобразование имени: обнаружено входное имя, но не соответствующий выходной формат.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**Ошибка \_ DS \_ имя \_ \_ только домен \_**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Преобразование имен: не удается полностью разрешить, найден только домен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**Ошибка \_ имени DS, \_ \_ Ошибка \_ без \_ синтаксического \_ сопоставления**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Преобразование имен: не удается выполнить чистое синтаксическое сопоставление на клиенте без перехода к сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**произошла ошибка \_ DS, \_ созданная \_ Атри \_ Mod**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



Изменение сконструированного атрибута не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**Ошибка \_ DS \_ - \_ неправильный \_ класс obj-объект \_**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



Указанный объект OM-Object-Class неверен для атрибута с указанным синтаксисом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**произошла ошибка \_ \_ \_ \_ в ожидании DS DRA REPL**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



Запрос на репликацию отправлен; Ожидание ответа.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**произошла ошибка доменных служб \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



Для запрошенной операции требуется служба каталогов, но она недоступна.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**Ошибка \_ DS \_ недопустимое \_ \_ отображаемое \_ имя LDAP**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



Отображаемое имя LDAP класса или атрибута содержит символы, отличные от ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**Ошибка \_ поиска в DS \_ без \_ базовой службы \_**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



Запрошенная операция поиска поддерживается только для базовых поисков.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**Ошибка \_ DS не \_ удается \_ получить \_ АТТС**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



Поиск не смог получить атрибуты из базы данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**Ошибка \_ DS \_ посмотрите \_ без \_ компоновки**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



Операция обновления схемы попыталась добавить атрибут обратной ссылки, который не имеет соответствующей ссылки вперед.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**Ошибка \_ при \_ несоответствии эпохи DS \_**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



Источник и назначение междоменного перемещения не согласуются с номером эпохи объекта. Источник или назначение не имеют последней версии объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии имени src в DS \_**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



Источник и назначение междоменного перемещения не согласуются с текущим именем объекта. Источник или назначение не имеют последней версии объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**Ошибка \_ при \_ \_ идентичности DS src и \_ DST \_ NC \_**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



Источник и назначение для операции междоменного перемещения идентичны. Вызывающий объект должен использовать операцию локального перемещения вместо операции перемещения между доменами.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**Ошибка \_ при \_ \_ \_ несоответствии NC в DS**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



Источник и назначение для междоменного перемещения не согласованы с контекстами именования в лесу. Источник или назначение не имеют последней версии контейнера секций.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**Ошибка \_ DS \_ , \_ не \_ аусоритиве \_ для \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



Назначение для перемещения между доменами не является полномочным для контекста именования назначения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**\_несоответствие \_ \_ идентификатора GUID \_ src в DS**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



Источник и назначение междоменного перемещения не согласуются с удостоверением исходного объекта. Источник или назначение не имеют последней версии исходного объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**Ошибка \_ DS не \_ удается \_ Переместить \_ Удаленный \_ объект**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



Объект, перемещаемый между доменами, уже удален целевым сервером. На исходном сервере не установлена последняя версия исходного объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**произошла ошибка \_ \_ при выполнении операции PDC DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Уже выполняется другая операция, которая требует монопольного доступа к FSMO PDC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**Ошибка \_ при \_ \_ очистке междоменной службы DS \_ \_ рекд**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Операция междоменного перемещения завершилась сбоем, так как существует две версии перемещенного объекта — по одному в исходном и конечном доменах. Целевой объект необходимо удалить для восстановления системы в целостное состояние.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**Ошибка \_ DS \_ недопустимой \_ \_ операции перемещения ксдом \_**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Этот объект не может быть перемещен между границами домена, так как перемещение между доменами для этого класса запрещено, или у объекта есть некоторые особые характеристики, например: учетная запись доверия или ограниченный RID, предотвращающий его перемещение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**Ошибка \_ DS \_ не \_ удается \_ с \_ мембершпс группы acct \_**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Невозможно переместить объекты с членством в границах домена, так как после перемещения это приведет к нарушению условий членства в группе учетных записей. Удалите объект из любого членства в группах учетных записей и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**Ошибка \_ NC DS Active Directory \_ \_ должна \_ иметь \_ \_ родителя NC**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Заголовок контекста именования должен быть прямым дочерним элементом другого заголовка контекста именования, а не внутреннего узла.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности CR в DS**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



Каталог не может проверить предложенное имя контекста именования, так как он не содержит реплики контекста именования выше предложенного контекста именования. Убедитесь, что роль хозяина именования доменов удерживается сервером, настроенным в качестве сервера глобального каталога, и что сервер обновлен с партнерами по репликации. (относится только к хозяинам именования доменов Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**\_домен ошибок DS \_ DST не является \_ \_ \_ собственным**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Конечный домен должен находиться в собственном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**Ошибка в \_ DS с \_ отсутствующим \_ \_ контейнером инфраструктуры**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Невозможно выполнить операцию, так как сервер не имеет контейнера инфраструктуры в предметной области.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**Ошибка \_ DS не \_ удается \_ Переместить \_ группу учетных записей \_**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Перемещение между доменами непустых групп учетных записей не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ группу ресурсов**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Перемещение между доменами непустых групп ресурсов не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**Ошибка \_ DS \_ Недопустимый \_ \_ флаг поиска**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Недопустимые флаги поиска для атрибута. Бит ANR допустим только для атрибутов строк Юникода или Teletex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**Ошибка \_ DS \_ без \_ дерева \_ Удаление \_ выше \_ сетевого контроллера**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Удаление дерева, начиная с объекта, имеющего заголовок NC в качестве потомка, запрещено.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**Ошибка \_ DS \_ не удалось \_ блокировать \_ дерево блокировки \_ для \_ удаления**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Службе каталогов не удалось заблокировать дерево при подготовке к удалению дерева, так как это дерево используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**Ошибка \_ DS \_ не удалось \_ определяет \_ объекты \_ для \_ \_ удаления дерева**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Службе каталогов не удалось опознать список объектов для удаления при попытке удаления дерева.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**Ошибка \_ \_ \_ при инициализации SAM \_ DS**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1. Состояние ошибки: 0x %2. Завершите работу системы и перезагрузите ее в режим восстановления служб каталогов. подробные сведения см. в журнале событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**Ошибка \_ при \_ \_ нарушении чувствительности группы DS \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Только администратор может изменить список членов административной группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**Ошибка \_ DS \_ не \_ удается \_ примариграупид mod**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Невозможно изменить идентификатор основной группы учетной записи контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**Ошибка \_ DS \_ недопустимой \_ базовой \_ схемы \_ Mod**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Предпринята попытка изменить базовую схему.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**Ошибка \_ \_ ненадежного \_ изменения схемы DS \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



Добавление нового обязательного атрибута к существующему классу, удаление обязательного атрибута из существующего класса или Добавление дополнительного атрибута к Специальному классу Top, который не является атрибутом посмотрите (например, добавление или удаление вспомогательного класса), не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**Ошибка \_ \_ \_ запрещенного обновления схемы DS \_**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



Обновление схемы не разрешено на этом контроллере домена, так как контроллер домена не является владельцем роли FSMO схемы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**Ошибка "не \_ \_ удается создать службу DS \_ \_ в \_ схеме"**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Объект этого класса не может быть создан в контейнере схемы. В контейнере схемы можно создавать только объекты Attribute-Schema и class-schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**Ошибка \_ DS \_ Install \_ . \_ \_ версия исходного SCH \_**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



Установка реплики или дочернего элемента не смогла получить атрибут Обжектверсион в контейнере схемы на исходном контроллере домена. Либо атрибут отсутствует в контейнере схемы, либо предоставленные учетные данные не имеют разрешения на его чтение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**Ошибка \_ DS \_ Install \_ не \_ установлена \_ версия SCH \_ в \_ инифиле**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



При установке реплики или дочерней части не удалось прочитать атрибут Обжектверсион в разделе схемы файла schema.ini в каталоге System32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**Ошибка \_ DS — \_ Недопустимый \_ \_ Тип группы**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Указан недопустимый тип группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ вложенных \_ глобалграуп \_ в \_ микседдомаин**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Нельзя вложить глобальные группы в смешанный домен, если включена безопасность группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ вложения \_ локальной группы \_ в \_ микседдомаин**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Невозможно вложить локальные группы в смешанный домен, если включена безопасность группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**\_глобальный домен \_ ошибок \_ \_ не могу иметь \_ локального \_ участника**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Глобальная группа не может иметь локальную группу в качестве члена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**в \_ глобальном DS "ошибка" \_ \_ \_ не удается использовать \_ универсальный \_ член**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Глобальная группа не может иметь универсальную группу в качестве члена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**Ошибка \_ \_ универсальной службы DS \_ \_ не удается иметь \_ локального \_ участника**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Универсальная группа не может иметь локальную группу в качестве члена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**в \_ Глобальной службе ошибок DS \_ \_ \_ нет \_ \_ члена CROSSDOMAIN**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Глобальная группа не может иметь междоменного члена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**" \_ Ошибка \_ локальной службы DS \_ \_ не удается иметь \_ \_ локальный \_ член CROSSDOMAIN"**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Локальная группа в локальной группе не может быть членом другой локальной группы домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**Служба "ошибки \_ DS" \_ имеет \_ основные \_ Участники**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Группу с основными участниками нельзя изменить на группу с отключенной безопасностью.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**Ошибка \_ \_ \_ \_ при преобразовании SD строки DS \_**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



При загрузке кэша схемы не удалось преобразовать строку SD по умолчанию для объекта class-schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**Ошибка \_ при \_ именовании \_ хозяина имен DS \_**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Только DSA, настроенные на серверы глобального каталога, должны иметь роль хозяина именования доменов. (относится только к серверам Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**Ошибка \_ \_ \_ уточняющего запроса DNS DS \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



Операция DSA не может быть продолжена из-за ошибки уточняющего запроса DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**Ошибка \_ DS \_ не удалось \_ Update \_ SPN**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



При обработке изменения имени узла DNS для объекта значения имени субъекта-службы не могут быть синхронизированы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**Ошибка \_ DS не \_ удается \_ получить \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Не удалось прочитать атрибут дескриптора безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ОШИБОЧный \_ \_ ключ DS \_ не является \_ уникальным**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



Запрошенный объект не найден, но найден объект с этим ключом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**Ошибка \_ DS \_ . \_ неправильный \_ синтаксис связанного Атри \_**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



Неправильный синтаксис добавляемого связанного атрибута. Прямые ссылки могут иметь только синтаксис 2.5.5.1, 2.5.5.7 и 2.5.5.14, а одноадресные ссылки могут иметь только синтаксис 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**Ошибка \_ DS \_ SAM \_ : \_ требуется \_ пароль буткэй**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Диспетчеру учетных записей безопасности необходимо получить пароль для загрузки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**Ошибка \_ DS \_ SAM: \_ требуется \_ буткэй флоппи- \_ дисковод**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Диспетчеру учетных записей безопасности необходимо получить загрузочный ключ с дискеты.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**Ошибка \_ \_ запуска DS \_**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Не удается запустить службу каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**Ошибка \_ \_ при инициализации \_ DS**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Не удалось запустить службы каталогов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**Ошибка \_ DS \_ без общедоступной \_ \_ политики конфиденциальности \_ при \_ подключении**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



Соединение между клиентом и сервером требует конфиденциальности пакетов или более высокого уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**Ошибка \_ \_ исходного \_ домена DS \_ в \_ лесу**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Исходный домен может не находиться в том же лесу, что и назначение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**Ошибка \_ \_ конечного домена DS, \_ \_ не \_ в \_ лесу**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Конечный домен должен находиться в лесу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_Аудит ошибок \_ назначения \_ DS \_ не \_ включен**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



Для операции требуется включить аудит конечного домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**Ошибка \_ DS не \_ удается \_ найти контроллер домена \_ \_ для \_ src \_**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



Операции не удалось нахождение контроллера домена для исходного домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**Ошибка \_ DS \_ src \_ \_ , не \_ Группа \_ или \_ пользователь**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



Исходный объект должен быть группой или пользователем.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**\_ \_ \_ \_ \_ в \_ лесу существует ошибка ИД безопасности src DS**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



Идентификатор безопасности исходного объекта уже существует в целевом лесу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**Ошибка \_ при \_ \_ \_ \_ \_ \_ несовпадении класса объектов src и DST в DS**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



Исходный и целевой объекты должны иметь один и тот же тип.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**Ошибка \_ \_ при инициализации ошибки SAM \_**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1. Состояние ошибки: 0x %2. нажмите кнопку ок, чтобы завершить работу системы и перезапустить ее в режиме Сейф. Подробные сведения см. в журнале событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**Ошибка \_ при \_ \_ \_ отправке сведений о схеме DS DRA \_**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Не удалось добавить сведения о схеме в запрос на репликацию.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**Ошибка \_ при \_ \_ конфликте схемы DS DRA \_**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



Не удалось завершить операцию репликации из-за несовместимости схемы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**произошла ошибка при \_ \_ \_ \_ конфликте схемы DS DRA более ранней версии \_**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



Не удалось завершить операцию репликации из-за несовместимости предыдущей схемы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**Ошибка \_ при \_ \_ \_ несовпадении NC obj DS DRA \_**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Не удалось применить обновление репликации, поскольку источник или назначение еще не получили сведения о последней операции перемещения между доменами.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**Ошибка \_ \_ NC DS \_ по-прежнему \_ имеет \_ DSA**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Не удалось удалить запрошенный домен, так как существуют контроллеры домена, на которых все еще размещен этот домен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**\_требуется ошибка \_ GC \_ DS**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



Запрошенную операцию можно выполнить только на сервере глобального каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**Ошибка \_ \_ локальный \_ член \_ локальной \_ \_ службы DS**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Локальная группа может быть членом только других локальных групп в том же домене.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**Ошибка \_ DS \_ No \_ FPO \_ в \_ универсальных \_ группах**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Участники внешней безопасности не могут быть членами универсальных групп.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**Ошибка \_ DS не \_ удается \_ Добавить \_ в \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



Атрибут не может быть реплицирован в GC по соображениям безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**Ошибка \_ DS \_ без \_ контрольной точки \_ с \_ основным контроллером домена**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Не удалось выполнить контрольную точку с основным контроллером домена, так как в настоящее время обрабатывается слишком много изменений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**Ошибка \_ \_ аудита исходного кода DS \_ \_ не \_ включена**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



Для операции требуется включить аудит исходного домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**Ошибка \_ \_ создания DS \_ \_ в \_ недомене \_ NC**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Объекты субъектов безопасности могут создаваться только внутри контекстов именования доменов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**Ошибка \_ DS \_ недопустимое \_ имя \_ \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Не удалось создать имя субъекта-службы (SPN), так как указанное имя узла имеет формат, отличный от требуемого.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**Ошибка \_ \_ фильтра DS \_ использует \_ создается \_ attr**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Передан фильтр, использующий сконструированные атрибуты.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**Ошибка \_ DS \_ UNICODEPWD \_ не \_ в \_ кавычках**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



Значение атрибута unicodePwd должно быть заключено в двойные кавычки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**\_ \_ \_ \_ превышена квота учетной записи виртуальной машины DS \_**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Не удалось присоединить компьютер к домену. Превышено максимальное число учетных записей компьютеров, которое вы можете создать в этом домене. Чтобы сбросить или увеличить этот предел, обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ \_ \_ \_ на \_ летнем \_ контроллере домена должна выполняться ошибка DS**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



По соображениям безопасности операция должна выполняться на целевом контроллере домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**Ошибка \_ \_ \_ , так как для DS src DC \_ требуется \_ \_ пакет обновления 4 \_ или \_ более поздней версии**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



По соображениям безопасности исходный контроллер домена должен быть NT4SP4 или выше.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**Ошибка \_ DS "не \_ удается \_ \_ удалить дерево удаление \_ критического \_ obj"**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Критические системные объекты службы каталогов невозможно удалить во время операций удаления дерева. Удаление дерева может быть выполнено частично.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**Ошибка \_ \_ при инициализации \_ \_ оснастки DS**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Не удалось запустить службы каталогов из-за следующей ошибки: %1. Состояние ошибки: 0x %2. Нажмите кнопку "ОК", чтобы завершить работу системы. Для дальнейшей диагностики системы можно использовать консоль восстановления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**Ошибка \_ \_ \_ \_ при инициализации \_ консоли DS SAM**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1. Состояние ошибки: 0x %2. Нажмите кнопку "ОК", чтобы завершить работу системы. Для дальнейшей диагностики системы можно использовать консоль восстановления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**\_ \_ \_ \_ слишком высокая версия леса DS \_**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



Версия операционной системы несовместима с текущим режимом работы AD DSного леса или AD LDS режимом работы набора конфигурации. Необходимо выполнить обновление до новой версии операционной системы, чтобы этот сервер мог стать AD DS контроллером домена или добавить экземпляр AD LDS в этом AD DS лесу или в наборе конфигурации AD LDS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**\_ \_ \_ \_ слишком высокая версия домена DS \_ с ошибками**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



Установленная версия операционной системы несовместима с текущим режимом работы домена. Необходимо выполнить обновление до новой версии операционной системы, чтобы этот сервер мог стать контроллером домена в этом домене.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**\_нехватка \_ \_ версии леса \_ DS \_ с ошибкой**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



Версия операционной системы, установленной на этом сервере, больше не поддерживает текущий функциональный уровень AD DS леса или AD LDS режим работы набора конфигурации. Чтобы этот сервер мог стать AD DS контроллером домена или экземпляром AD LDS в этом лесу или наборе конфигураций, необходимо повысить режим работы AD DSного леса или AD LDSного набора конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**\_ \_ \_ \_ слишком низкая версия домена DS \_ с ошибками**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



Версия операционной системы, установленной на этом сервере, больше не поддерживает текущий режим работы домена. Чтобы этот сервер мог стать контроллером домена в этом домене, необходимо повысить режим работы домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**Ошибка \_ \_ несовместимая \_ версия DS**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



Версия операционной системы, установленной на этом сервере, несовместима с функциональным уровнем домена или леса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**\_нехватка \_ \_ версии DSA \_ DS**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Режим работы домена (или леса) не может быть повышен до запрошенного значения, так как в домене (или лесу) существует один или несколько контроллеров домена, которые имеют более низкий несовместимый функциональный уровень.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ \_ версии поведения \_ в \_ микседдомаин**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Режим работы леса не может быть повышен до запрошенного значения, так как один или несколько доменов по-прежнему находятся в режиме смешанного домена. Для повышения функционального уровня леса все домены леса должны находиться в собственном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**\_ \_ \_ неподдерживаемый \_ порядок сортировки \_ в DS.**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



Запрошенный порядок сортировки не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**\_имя DS \_ ошибки \_ не является \_ уникальным**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



Запрошенное имя уже существует в качестве уникального идентификатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**Ошибка \_ \_ учетной записи виртуальной машины DS, \_ \_ созданной \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



Учетная запись компьютера была создана до NT4. Учетная запись должна быть создана повторно.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**Ошибка \_ DS \_ из \_ \_ хранилища версий \_**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



База данных находится вне хранилища версий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**\_используется ошибка \_ несовместимых \_ элементов управления \_ в DS**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Не удалось продолжить операцию, так как использовались несколько конфликтующих элементов управления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**Ошибка \_ DS \_ без \_ \_ домена ссылок**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Не удалось найти допустимый домен ссылки на дескриптор безопасности для этой секции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**Ошибка \_ \_ зарезервированного \_ ИД ссылки DS \_**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Сбой обновления схемы: идентификатор ссылки зарезервирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**\_идентификатор ссылки DS "ошибка \_ \_ \_ \_ недоступен"**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Не удалось обновить схему: нет доступных идентификаторов ссылок.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**Ошибка \_ \_ группы доступности \_ DS \_ не удается использовать \_ универсальный \_ член**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Группа учетных записей не может иметь универсальную группу в качестве члена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**Ошибка \_ DS \_ МОДИФИДН \_ , запрещенная \_ \_ типом экземпляра \_**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Операции переименования или перемещения при именовании заголовков контекста или объектов, доступных только для чтения, запрещены.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**Ошибка \_ DS \_ без \_ \_ перемещения объектов \_ в \_ \_ NC схемы**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Операции перемещения с объектами в контексте именования схемы не допускаются.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**Ошибка \_ DS \_ МОДИФИДН \_ , запрещенная \_ \_ флагом**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Для объекта был установлен системный флаг, который не допускает перемещение или переименование объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**Ошибка \_ DS \_ модифидн \_ неправильной \_**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Этому объекту запрещено изменять свой контейнер "бабушке". Перемещения для этого объекта запрещены, но ограничены одноуровневыми контейнерами.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**Ошибка \_ \_ имя DS \_ Ошибка \_ в \_ ссылке доверия**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Не удалось полностью разрешить, создается ссылка на другой лес.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**Ошибка \_ не \_ поддерживается \_ на \_ стандартном \_ сервере**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



Запрошенное действие не поддерживается на стандартном сервере.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**Ошибка \_ DS не \_ удается \_ получить доступ к \_ удаленной \_ части \_ \_ AD**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Не удалось получить доступ к разделу службы каталогов, расположенной на удаленном сервере. Убедитесь, что по крайней мере один сервер работает для рассматриваемого раздела.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**Ошибка \_ DS \_ CR \_ при \_ \_ проверке \_ v2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



Каталог не может проверить предложенное имя контекста именования (или раздела), так как он не содержит реплики и не может связаться с репликой контекста именования выше предложенного контекста именования. Убедитесь, что родительский контекст именования правильно зарегистрирован в DNS, и хотя бы одна реплика этого контекста именования достижима хозяином именования доменов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_ \_ превышен предел для потоков DS \_ \_**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



Превышено ограничение потока для этого запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**Ошибка \_ DS, \_ не \_ Ближайшая к**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



Сервер глобального каталога не находится на ближайшем сайте.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**Ошибка \_ DS \_ \_ не удается наследовать \_ SPN \_ без \_ ссылки на сервер \_**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



DS не может наследовать имя участника-службы (SPN) для взаимной проверки подлинности целевого сервера, так как соответствующий объект сервера в локальной базе данных DS не имеет атрибута Серверреференце.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**\_ \_ \_ сбой однопользовательского \_ режима \_ DS**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



Службе каталогов не удалось войти в однопользовательский режим.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**Ошибка \_ при \_ \_ синтаксической \_ ошибке нтдскрипт DS**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



Службе каталогов не удается проанализировать скрипт из-за синтаксической ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**Ошибка \_ \_ процесса нтдскрипт \_ DS \_**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Службе каталогов не удается обработать скрипт из-за ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ОШИБКИ \_ DS \_ в \_ разных \_ эпохах REPL**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Службе каталогов не удается выполнить запрошенную операцию, так как вовлеченные серверы относятся к различным эпохам репликации (которые обычно связаны с выполняемым переименованием домена).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**Ошибка \_ при \_ \_ изменении расширений DS DRS \_**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



Привязка службы каталогов должна быть повторно согласована из-за изменений в сведениях о серверных расширениях.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**\_ \_ \_ \_ \_ \_ \_ при \_ отключенном \_ CR не разрешено изменение набора реплик DS**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Операция запрещена для отключенной перекрестной ссылки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**Ошибка \_ DS \_ нет \_ msDS \_ интид**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Ошибка обновления схемы: нет доступных значений для msDS-Интид.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**Ошибка \_ DS \_ DUP \_ msDS \_ интид**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Ошибка обновления схемы: повторяющаяся msDS-Интид. Повторите операцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_ \_ \_ в \_ рднаттид существует ошибка DS**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Сбой удаления схемы: атрибут используется в Рднаттид.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**Ошибка \_ \_ авторизации DS \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Службе каталогов не удалось авторизовать запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**Ошибка \_ \_ недопустимого \_ скрипта DS**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Службе каталогов не удается обработать скрипт, так как он недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**Ошибка \_ \_ при удаленной \_ операции переcrossref DS \_ \_**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Операция удаленного создания перекрестной ссылки завершилась сбоем в роли хозяина именования доменов. Ошибка операции в расширенных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**Ошибка \_ " \_ Перекрестная ссылка DS" \_ \_ занята**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Перекрестная ссылка используется локально с тем же именем.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**Ошибка \_ DS не \_ удается \_ наследовать \_ SPN \_ для \_ удаленного \_ домена**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



ДОМЕНная служба не может наследовать имя участника-службы (SPN), с помощью которого осуществляется взаимная проверка подлинности целевого сервера, так как домен сервера был удален из леса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**Ошибка \_ DS не \_ удается \_ понизить \_ с помощью NC с \_ возможностью записи \_**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



Доступные для записи NC предотвращают понижение роли контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_ \_ обнаружена ошибка при дублировании \_ ИД DS \_**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



Запрошенный объект имеет неуникальный идентификатор и не может быть извлечен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**Ошибка \_ DS \_ , недостаточная \_ \_ для \_ создания \_ объекта**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Предоставлено недостаточно атрибутов для создания объекта. Возможно, этот объект не существует, так как он был удален и уже собран сборщиком мусора.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**Ошибка \_ \_ преобразования группы \_ DS \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



Невозможно преобразовать группу из-за ограничений атрибута для запрошенного типа группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ базовую \_ группу приложений**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



Перемещение между доменами непустых основных групп приложений запрещено.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ группу запросов приложения \_**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Перемещение между доменами непустых групп приложений на основе запросов не допускается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**роль DS с ОШИБКАми \_ \_ \_ не \_ проверена**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



Не удалось проверить владение ролью FSMO, так как ее раздел каталога не был успешно реплицирован по крайней мере с одним партнером репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**\_ \_ контейнер ВКО DS \_ Error \_ не может \_ быть \_ Специальным**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



Целевой контейнер для перенаправления хорошо известного контейнера объектов еще не может быть специальным контейнером.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**Ошибка \_ \_ \_ при переименовании домена DS \_ \_**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



Службе каталогов не удается выполнить запрошенную операцию, поскольку выполняется операция переименования домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**Ошибка \_ DS \_ существующий \_ \_ Дочерний \_ NC AD**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



Служба каталогов обнаружила дочерний раздел под запрошенным именем секции. Иерархия секций должна быть создана в нисходящем методе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_ \_ \_ Превышено время существования DS REPL \_**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



Служба каталогов не может выполнить репликацию с этим сервером, так как время, прошедшее с момента последней репликации с этим сервером, превысило время существования захоронения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**\_ \_ \_ в \_ контейнере System запрещена \_ ошибка DS.**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



Запрошенная операция запрещена для объекта в контейнере системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**Ошибка \_ \_ \_ \_ переполнения очереди отправки LDAP DS \_**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



Сетевая очередь отправки LDAP-серверов заполнена, так как клиент не обрабатывает результаты запросов достаточно быстро. Запросы больше не будут обрабатываться до тех пор, пока клиент не будет перехватываться. Если клиент не перехватится, он будет отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**Ошибка \_ в \_ \_ \_ \_ окне расписания DRA DS**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



Запланированная репликация не выполнялась, так как система слишком занята для выполнения запроса в окне расписания. Очередь репликации перегружена. Рекомендуется сократить число партнеров или уменьшить частоту запланированной репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**\_ \_ неизвестная политика DS \_ \_**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



В настоящее время невозможно определить, доступна ли политика репликации ветвей на контроллере домена концентратора. Повторите попытку позже, чтобы учесть задержки репликации.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**Ошибка \_ без \_ \_ объекта параметров \_ сайта**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



Объект параметров сайта для указанного сайта не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**Ошибка \_ без \_ секретов**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



Локальное хранилище учетных записей не содержит секретных материалов для указанной учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**Ошибка \_ не \_ \_ найден контроллер домена, доступный для записи \_**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Не удалось найти доступный для записи контроллер домена в домене.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**Ошибка \_ DS \_ без \_ \_ объекта сервера**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



Объект сервера для контроллера домена не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**Ошибка \_ DS \_ без \_ объекта Ntdsa \_**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



объект NTDS Параметры для контроллера домена не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**Ошибка \_ \_ поиска не \_ АСК \_ DS**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



Запрошенная операция поиска не поддерживается для поиска АСК.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**Ошибка \_ \_ аудита DS \_**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Не удалось создать обязательное событие аудита для операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**Ошибка \_ DS \_ недопустимое \_ \_ поддерево флага поиска \_**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Недопустимые флаги поиска для атрибута. Бит индекса поддерева допустим только для атрибутов с одним значением.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**Ошибка \_ DS \_ Недопустимый \_ \_ кортеж флага поиска \_**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Недопустимые флаги поиска для атрибута. Бит индекса кортежа допустим только для атрибутов строк Юникода.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**\_ \_ \_ \_ слишком глубокая таблица иерархии \_ DS**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Слишком глубокая вложенность адресных книг. Не удалось построить таблицу иерархии.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**Ошибка \_ DS \_ DRA \_ поврежденный \_ \_ вектор УТД**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



Указанный вектор rvalue характеристики для обновления поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**Ошибка \_ \_ секреты DS \_ DRA \_**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



Запрос на репликацию секретов запрещен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**Ошибка \_ \_ зарезервированного \_ идентификатора MAPI DS \_**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Сбой обновления схемы: Идентификатор MAPI зарезервирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**\_ \_ Идентификатор MAPI DS \_ Error \_ \_ недоступен**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Ошибка обновления схемы: нет доступных идентификаторов MAPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**Ошибка \_ при \_ \_ отсутствии \_ \_ секрета KRBTGT DS DRA**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



Сбой операции репликации из-за отсутствия необходимых атрибутов локального объекта KRBTGT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**\_имя домена службы "ошибка" \_ \_ \_ существует \_ в \_ лесу**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



Доменное имя доверенного домена уже существует в лесу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**\_ \_ \_ \_ \_ в \_ лесу существует ошибка "неструктурированное имя DS"**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



Неструктурированное имя доверенного домена уже существует в лесу.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**Ошибка \_ недопустимое \_ \_ имя участника-пользователя \_**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



Недопустимое имя участника-пользователя (UPN).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**Ошибка \_ \_ \_ сопоставленной \_ группы OID DS \_ \_ не удается иметь \_ членов**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



Сопоставленные группы OID не могут иметь членов.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**Ошибка \_ \_ OID DS \_ не \_ найдена**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



Не удается найти указанный OID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**Ошибка \_ \_ \_ перезапуска \_ целевого объекта DRA DS**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



Операция репликации завершилась сбоем, так как целевой объект, на который ссылается значение ссылки, перезапущен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**Ошибка \_ \_ неразрешенного \_ \_ перенаправления NC DS**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



Сбой операции перенаправления, так как целевой объект находится в NC, отличном от контекста именования домена текущего контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**Ошибка \_ DS \_ High \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



Функциональный уровень набора конфигурации AD LDS не может быть понижен до запрошенного значения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**Ошибка \_ с \_ высокой \_ версией DSA DS \_**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



Режим работы домена (или леса) не может быть понижен до запрошенного значения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**Ошибка \_ DS \_ Low \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



Функциональный уровень AD LDS набора конфигурации не может быть получен к запрошенному значению, так как существует один или несколько экземпляров ADLDS, которые имеют более низкий несовместимый функциональный уровень.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**Ошибка \_ \_ SID домена \_ , совпадающее \_ с именем \_ локальной \_ рабочей станции**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



Не удается выполнить присоединение к домену, так как идентификатор безопасности домена, который вы пытались присоединить, идентичен идентификатору безопасности этого компьютера. Это симптом неправильной клонированной установки операционной системы. Для создания нового идентификатора безопасности компьютера необходимо запустить Sysprep на этом компьютере. Дополнительные сведения см. по адресу <https://go.microsoft.com/fwlink/p/?linkid=168895>.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**Ошибка \_ \_ \_ при удалении проверки SAM \_ \_ в DS**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



Операция отмены удаления завершилась сбоем, так как имя учетной записи SAM или дополнительное имя учетной записи SAM объекта, для которого выполняется восстановление, конфликтует с существующим динамическим объектом.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**Ошибка при \_ неправильном \_ типе учетной записи \_**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



Система не является полномочным для указанной учетной записи и поэтому не может завершить операцию. Повторите операцию, используя поставщик, связанный с этой учетной записью. Если это поставщик в Интернете, используйте сайт поставщика в Интернете.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




