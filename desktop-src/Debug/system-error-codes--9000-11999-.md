---
description: Описание кодов ошибок 9000-11999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Коды системных ошибок (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aea735601b2c19bfc54a0841bb0150426b5c292e61dddb53473dfe41575e4337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984484"
---
# <a name="system-error-codes-9000-11999"></a>Коды системных ошибок (9000-11999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 9000 – 11999). Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**\_Ошибка DNS \_ Ошибка \_ формата \_ ркоде**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



DNS-серверу не удалось интерпретировать формат.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**\_Ошибка DNS \_ \_ при ркоде сервера \_**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Ошибка DNS-сервера.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**Ошибка DNS ошибка \_ \_ \_ имени \_ ркоде**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



DNS-имя не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_Ошибка DNS \_ ркоде \_ не \_ реализована**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



DNS-запрос не поддерживается сервером имен.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_Ошибка DNS \_ ркоде \_ отклонена**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Операция DNS отклонена.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_Ошибка DNS \_ ркоде \_ иксдомаин**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



Существует несуществующее DNS-имя.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_Ошибка DNS \_ ркоде \_ иксррсет**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



Существует набор DNS RR, который не должен существовать.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_Ошибка DNS \_ ркоде \_ нксррсет**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



Набор RR DNS, который должен существовать, не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_Ошибка DNS \_ ркоде \_ нотаус**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



DNS-сервер не является полномочным для зоны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_Ошибка DNS \_ ркоде \_ нотзоне**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



DNS-имя в обновлении или prereq не входит в зону.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_Ошибка DNS \_ ркоде \_ бадсиг**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



Не удалось проверить подпись DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_Ошибка DNS \_ ркоде \_ бадкэй**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Неверный ключ DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_Ошибка DNS \_ ркоде \_ бадтиме**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



Срок действия подписи DNS истек.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**\_ \_ требуется КЭЙМАСТЕР ошибка \_ DNS**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Эту операцию могут выполнять только DNS-сервер, выступающий в качестве основного для зоны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_ \_ \_ \_ в \_ подписанной \_ зоне не разрешена ошибка DNS**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Эта операция запрещена для зоны, которая подписана или имеет ключи подписывания.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Ошибка DNS \_ NSEC3 \_ несовместима \_ с \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



NSEC3 несовместим с алгоритмом RSA-SHA-1. Выберите другой алгоритм или используйте NSEC.

Это значение также называлось " **Ошибка DNS". \_ \_ недопустимые \_ \_ Параметры NSEC3**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_Ошибка DNS \_ - \_ недостаточно \_ \_ \_ дескрипторов ключей подписывания**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



В зоне недостаточно ключей подписывания. Должен существовать хотя бы один ключ подписывания ключа (KSK) и хотя бы один ключ подписывания зоны (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_ \_ неподдерживаемый алгоритм DNS-ошибки \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



Указанный алгоритм не поддерживается.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**Ошибка DNS- \_ \_ Недопустимый \_ \_ Размер ключа**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



Указанный размер ключа не поддерживается.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_ \_ ключ подписывания ошибки DNS \_ \_ \_ недоступен**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Один или несколько ключей подписывания для зоны недоступны для DNS-сервера. Подписывание зоны не будет работать до устранения этой ошибки.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_KSP об ошибках DNS не \_ \_ \_ \_ поддерживает \_ защиту**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



Указанный поставщик хранилища ключей не поддерживает DPAPI + + Data Protection. Подписывание зоны не будет работать до устранения этой ошибки.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**Ошибка DNS, \_ \_ непредвиденная ошибка \_ \_ защиты данных \_**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Обнаружена непредвиденная ошибка DPAPI + +. Подписывание зоны не будет работать до устранения этой ошибки.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**\_Ошибка DNS \_ непредвиденная \_ \_ Ошибка CNG**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Обнаружена непредвиденная ошибка шифрования. Подписывание зоны может не работать, пока эта ошибка не будет устранена.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**Ошибка DNS — \_ \_ неизвестная \_ \_ версия параметра подписи \_**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



DNS-сервер обнаружил ключ подписывания неизвестной версии. Подписывание зоны не будет работать до устранения этой ошибки.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP ошибок \_ DNS \_ \_ недоступен**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



Указанный поставщик службы ключей не может быть открыт DNS-сервером.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_Ошибка DNS \_ слишком \_ много \_ скдс**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



DNS-сервер не может принимать дополнительные ключи подписывания с указанным алгоритмом и значением флага KSK для этой зоны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**Ошибка DNS. \_ \_ Недопустимый \_ \_ период переключения**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



Указан недопустимый период переключения.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**\_Ошибка DNS \_ недопустимое \_ \_ смещение начального переключения \_**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



Указано недопустимое начальное смещение смены ключа.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ \_ идет смена \_ состояния ошибки DNS**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



Указанный ключ подписывания уже находится в процессе последовательного перебора ключей.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_ \_ \_ отсутствует ключ резервного режима ожидания \_ \_ DNS**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



Указанный ключ подписывания не имеет резервного ключа для отмены.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_Ошибка DNS \_ не \_ разрешена \_ для \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Эта операция запрещена для ключа подписывания зоны (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_Ошибка DNS \_ не \_ разрешена \_ для \_ активного \_ SKD**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Эта операция запрещена для активного ключа подписывания.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_Смена ошибок \_ DNS \_ уже \_ поставлена в очередь**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



Указанный ключ подписывания уже помещен в очередь для продолжения.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_Ошибка DNS \_ не \_ разрешена \_ в \_ неподписанной \_ зоне**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Эта операция запрещена для неподписанной зоны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_Ошибка DNS при \_ неправильном \_ кэймастер**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



Не удалось выполнить эту операцию, так как DNS-сервер, указанный в качестве текущего мастера ключей для этой зоны, отключен или неправильно настроен. Устраните проблему в текущем мастере ключей для этой зоны или используйте другой DNS-сервер для присвоения роли мастера ключей.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**\_Ошибка DNS \_ . \_ \_ срок действия \_ подписи недопустим**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



Указанный период действия подписи недопустим.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Ошибка DNS при \_ недопустимом \_ \_ числе итераций NSEC3 \_**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



Указанное число итераций NSEC3 выше, чем разрешено минимальной длиной ключа, используемой в зоне.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**\_Ошибка DNS \_ DNSSEC \_ \_ отключена**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



Не удалось выполнить эту операцию, так как DNS-сервер настроен с отключенными функциями DNSSEC. Включите DNSSEC на DNS-сервере.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ Недопустимый \_ XML-код ошибки DNS**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



Не удалось выполнить эту операцию, так как полученный XML-поток пуст или является синтаксически недопустимым.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**Ошибка DNS — \_ \_ нет \_ допустимых \_ \_ якорей доверия**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Эта операция завершена, но не были добавлены якоря доверия, так как все полученные якоря доверия были недопустимыми, не поддерживаются, истек срок действия или не станут действительными менее чем за 30 дней.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_не удается \_ прокрутить смену ошибок \_ DNS \_**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



Указанный ключ подписывания не ожидает обновления родительского DS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_Ошибка DNS \_ при \_ \_ конфликте имен NSEC3**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



При подписывании NSEC3 обнаружен конфликт хэша. Укажите другую пользовательскую соль или используйте соль, сгенерированную случайным образом, и повторите попытку подписи зоны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Ошибка DNS \_ NSEC \_ несовместима \_ с \_ NSEC3 \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC не совместима с алгоритмом NSEC3-RSA-SHA-1. Выберите другой алгоритм или используйте NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_сведения об DNS \_ нет \_ записей**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



Для данного запроса записей в DNS не найдено.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**Ошибка DNS — \_ \_ неправильный \_ пакет**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Неверный пакет DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**Ошибка DNS — \_ \_ нет \_ пакета**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



Нет пакета DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_Ошибка DNS \_ ркоде**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Ошибка DNS, проверьте ркоде.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**\_Ошибка DNS при \_ небезопасном \_ пакете**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Незащищенный пакет DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_ \_ Ожидание запроса DNS**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



Запрос DNS-запроса ожидает выполнения.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**Ошибка DNS — \_ \_ Недопустимый \_ тип**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Недопустимый тип DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_Ошибка DNS при \_ неправильном \_ IP- \_ адресе**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Недопустимый IP-адрес.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**Ошибка DNS — \_ \_ недопустимое \_ свойство**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Недопустимое свойство.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**Ошибка DNS повторите попытку \_ \_ \_ \_ позже**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Повторите операцию DNS позже.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_Ошибка DNS \_ не является \_ уникальной**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



Запись для заданного имени и типа не является уникальной.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**Ошибка DNS, \_ \_ не относящаяся к \_ \_ имени RFC**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



DNS-имя не соответствует спецификациям RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_ \_ полное доменное имя состояния DNS**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



DNS-имя — это полное DNS-имя.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**состояние DNS — \_ \_ точечное \_ имя**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



DNS-имя имеет несколько точек (с несколькими метками).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_ \_ \_ имя одной части \_ состояния DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



DNS-имя — это однокомпонентное имя.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_Ошибка DNS \_ недопустимое \_ имя \_ char**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



DNS-имя содержит недопустимый символ.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ числовое имя ошибки DNS \_**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



DNS-имя является полностью числовым.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_Ошибка DNS \_ не \_ разрешена \_ на \_ корневом \_ сервере**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



Запрошенная операция запрещена на корневом сервере DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_ \_ \_ \_ в делегировании не разрешена ошибка \_ DNS**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



Не удалось создать запись, так как эта часть пространства имен DNS делегирована другому серверу.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_Ошибка DNS \_ не удается \_ найти \_ корневые \_ ссылки**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



DNS-серверу не удалось найти набор корневых ссылок.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_Ошибка DNS при \_ несоответствии \_ корневых \_ ссылок**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



DNS-сервер обнаружил корневые ссылки, но они не были согласованы во всех адаптерах.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_Ошибка DNS \_ \_ \_ слишком \_ малое значение DWORD**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



Указанное значение слишком мало для этого параметра.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_Ошибка DNS \_ \_ \_ слишком большая величина DWORD \_**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



Указанное значение слишком велико для этого параметра.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ Фоновая загрузка ошибок DNS \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Эта операция запрещена, пока DNS-сервер загружает зоны в фоновом режиме. Повторите попытку позже.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_Ошибка DNS \_ не \_ разрешена \_ на \_ RODC**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



Запрошенная операция запрещена для DNS-сервера, работающего на контроллере домена только для чтения.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_ \_ \_ \_ в Dname не разрешена ошибка DNS \_**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



Под записью DNAME не может быть данных.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_ \_ требуется делегирование ошибок DNS \_**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Для этой операции требуется делегирование учетных данных.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_Ошибка DNS при \_ неверной \_ \_ таблице политики**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



Таблица политики разрешения имен повреждена. Разрешение DNS завершится сбоем, пока оно не будет устранено. Обратитесь к сетевому администратору.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_зона ошибок \_ DNS \_ \_ не \_ существует**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



Зона DNS не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**Ошибка DNS — \_ \_ нет \_ \_ сведений о зоне**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Сведения о зоне DNS недоступны.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_Ошибка DNS \_ при \_ \_ выполнении операции с зоной**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Недопустимая операция для зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_ \_ \_ Ошибка конфигурации зоны ошибок \_ DNS**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Недопустимая конфигурация зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**\_зона ошибок \_ DNS \_ \_ не имеет \_ \_ записи SOA**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



В зоне DNS отсутствует начальная запись зоны (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**в \_ \_ зоне ошибок \_ DNS \_ нет \_ \_ записей NS**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



В зоне DNS нет записи сервера имен (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_зона ошибок \_ DNS \_ заблокирована**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



Зона DNS заблокирована.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ не удалось создать зону ошибок DNS \_**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Не удалось создать зону DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**\_зона ошибок \_ DNS \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



Зона DNS уже существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**автозона "ошибка DNS" \_ \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



Автоматическая зона DNS уже существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**Ошибка DNS — \_ \_ Недопустимый \_ \_ тип зоны**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Недопустимый тип зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**во \_ вторичной ошибке DNS \_ \_ требуется \_ главный \_ IP-адрес**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



Для дополнительной зоны DNS требуется главный IP-адрес.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_зона ошибок \_ DNS \_ не является \_ вторичной**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Зона DNS не является вторичной.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**\_при ошибке DNS \_ требуются \_ Дополнительные \_ адреса**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



Требуется дополнительный IP-адрес.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_Ошибка DNS \_ \_ при инициализации \_ WINS**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Сбой инициализации WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**\_Ошибка DNS при \_ необходимости \_ WINS- \_ серверов**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Требуются WINS-серверы.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_Ошибка DNS \_ \_ при инициализации \_ NBSTAT**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Не удалось вызвать инициализацию NBTSTAT.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_Ошибка DNS \_ при \_ удалении \_ SOA**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Недопустимое удаление начальной записи зоны (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**\_ \_ сервер пересылки ошибок DNS \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Для этого имени уже существует условная зона перенаправления.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**для \_ зоны ошибок DNS \_ \_ требуется \_ главный \_ IP-адрес**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Для этой зоны необходимо настроить один или несколько IP-адресов главного DNS-сервера.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**\_зона ошибок \_ DNS \_ \_ завершена**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



Невозможно выполнить операцию, так как эта зона выключена.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_зона ошибок \_ DNS \_ заблокирована \_ для \_ подписывания**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Невозможно выполнить эту операцию, так как зона подписана в данный момент. Повторите попытку позже.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**для \_ основной ошибки DNS \_ \_ требуется \_ файл данных**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



Основной зоне DNS требуется файл данных.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_Ошибка DNS при \_ недопустимом \_ \_ имени файла**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Недопустимое имя файла в зоне DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_Ошибка \_ \_ при открытии файла ошибок \_ DNS**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



Не удалось открыть файл для зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_ \_ \_ сбой обратной записи в файл ошибок DNS \_**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



Не удалось записать файл в зону DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**\_ \_ \_ синтаксический анализ файла ошибок DNS**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Ошибка при чтении файла подзоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_запись об ошибке DNS \_ \_ \_ не \_ существует**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



Запись DNS не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_ \_ Формат записи ошибок \_ DNS**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Ошибка формата записи DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ не удалось создать узел ошибки DNS \_**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Сбой создания узла в DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**Ошибка DNS — \_ \_ неизвестный \_ \_ тип записи**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Неизвестный тип записи DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**\_ \_ \_ истекло время ожидания записи об ошибке DNS \_**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



Истекло время ожидания записи DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_имя ошибки \_ DNS \_ не \_ в \_ зоне**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



Имя не входит в зону DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_Ошибка DNS \_ \_ циклическая запись CNAME**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Обнаружен цикл CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**\_узел ошибки \_ DNS \_ — \_ запись CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



Узел является записью CNAME DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_Ошибка DNS \_ при \_ конфликте CNAME**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Запись CNAME уже существует для указанного имени.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_запись ошибок \_ DNS \_ только \_ в \_ \_ корне зоны**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Запись только в корне зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**\_запись об ошибке DNS \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



Запись DNS уже существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ Дополнительные данные об ОШИБКАх DNS \_**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Ошибка данных дополнительной зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**Ошибка DNS — \_ \_ нет \_ данных о создании \_ кэша \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



Не удалось создать данные кэша DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_имя ошибки \_ DNS \_ \_ не \_ существует**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



DNS-имя не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_предупреждение DNS \_ \_ при создании \_ ошибки PTR**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



Не удалось создать запись указателя (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS-предупреждение о том, что \_ \_ домен не \_ удален**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



Домен DNS был удален.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_ \_ недоступная Служба каталогов DS \_**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



Служба каталогов недоступна.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**\_зона DS с ошибками DNS \_ \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



Зона DNS уже существует в службе каталогов.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_Ошибка DNS \_ нет \_ бутфиле \_ , \_ Если \_ зона DS**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



DNS-сервер не создает или не считывает файл загрузки для зоны DNS, интегрированной со службой каталогов.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**\_узел ошибки \_ DNS \_ — \_ Dname**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



Узел — это запись DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_конфликт Dname с ошибками DNS \_ \_**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Запись DNAME уже существует для данного имени.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_ \_ цикл псевдонима ошибок DNS \_**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



Обнаружена петля псевдонимов с записями CNAME или DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_сведения DNS \_ AXFR \_ завершены**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



Завершение DNS AXFR (зонная отправка).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_Ошибка DNS \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Сбой при переносе зоны DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**\_сведения о DNS \_ добавлены \_ Локальная \_ Служба WINS**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Добавлен локальный WINS-сервер.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_ \_ требуется продолжить состояние \_ DNS**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



Вызов безопасного обновления должен продолжать запрос на обновление.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_Ошибка DNS \_ отсутствует \_ TCP/IP**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



Сетевой протокол TCP/IP не установлен.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**Ошибка DNS — \_ \_ нет \_ DNS- \_ серверов**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



Нет DNS-серверов, настроенных для локальной системы.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_ \_ точка распространения ошибок \_ DNS \_ не \_ существует**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



Указанный раздел каталога не существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**\_точка распространения с ошибкой DNS \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



Указанный раздел каталога уже существует.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_ \_ точка распространения ошибок DNS \_ не \_ прикреплена**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Этот DNS-сервер не прикреплен к указанному разделу каталога.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_ \_ точка распространения ошибок DNS \_ уже \_ прикреплена**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Этот DNS-сервер уже прикреплен к указанному разделу каталога.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_Ошибка " \_ точка распространения DNS \_ \_ недоступна"**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



Раздел каталога недоступен в данный момент. Подождите несколько минут и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**Ошибка DNS при возникновении ошибки \_ \_ DP \_ FSMO \_**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



Не удалось выполнить операцию, так как не удалось связаться с ролью FSMO хозяина именования доменов. контроллер домена, удерживающий роль FSMO доменного именования, не работает или не может обслуживать запрос или не работает Windows Server 2003 или более поздней версии.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**всаеинтр**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Операция блокировки была прервана вызовом Всаканцелблоккингкалл.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**всаебадф**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



Указан недопустимый файловый обработчик.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**всаеакцес**
</dt> <dd> <dl> <dt>

10013 (0x271D)
</dt> <dt>



Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**всаефаулт**
</dt> <dd> <dl> <dt>

10014 (0x271E)
</dt> <dt>



Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**всаеинвал**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Указан недопустимый аргумент.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**всаемфиле**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Слишком много открытых сокетов.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**всаеваулдблокк**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



Не удалось немедленно завершить операцию неблокирующего сокета.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**всаеинпрогресс**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



В данный момент выполняется блокирующая операция.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**всаеалреади**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Была предпринята попытка выполнить операцию на неблокируемом сокете, на котором уже выполнялась операция.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**всаенотсокк**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Предпринята попытка выполнить операцию для объекта, который не является сокетом.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**всаедестаддррек**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



В операции на сокете пропущен требуемый адрес.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**всаемсгсизе**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Сообщение, отправленное на сокет датаграммы, превысило размер внутреннего буфера сообщений или другое ограничение сети, или буфер, используемый для получения датаграммы, меньше, чем сама датаграмма.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**всаепрототипе**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



В вызове функции сокета указан протокол, не поддерживающий семантику запрошенного типа сокета.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**всаенопротупт**
</dt> <dd> <dl> <dt>

10042 (0x273A)
</dt> <dt>



В вызове жетсоккопт или сетсоккопт был указан неизвестный, недопустимый или неподдерживаемый параметр или уровень.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**всаепротоносуппорт**
</dt> <dd> <dl> <dt>

10043 (0x273B)
</dt> <dt>



Запрошенный протокол не был настроен в системе или для него не существует реализации.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**всаесокктносуппорт**
</dt> <dd> <dl> <dt>

10044 (0x273C)
</dt> <dt>



Указанный тип сокета не поддерживается в данном семействе адресов.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**всаеопнотсупп**
</dt> <dd> <dl> <dt>

10045 (0x273D)
</dt> <dt>



Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**всаепфносуппорт**
</dt> <dd> <dl> <dt>

10046 (0x273E)
</dt> <dt>



Семейство протоколов не было настроено в системе или не существует реализации для него.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**всаеафносуппорт**
</dt> <dd> <dl> <dt>

10047 (0x273F)
</dt> <dt>



Использован адрес, несовместимый с запрошенным протоколом.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**всаеаддринусе**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



обычно разрешено только одно использование каждого адреса сокета (протокол/сетевой адрес/порт).


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**всаеаддрнотаваил**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



Запрошенный адрес недопустим в своем контексте.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**всаенетдовн**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Операция на сокете обнаружила отключение сети.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**всаенетунреач**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Операция сокета была предпринята к недостижимой сети.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**всаенетресет**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



Соединение разорвано из-за того, что операция проверки активности обнаруживает сбой во время выполнения операции.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**всаеконнабортед**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



Установленное подключение прервано программой на вашем компьютере.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**всаеконнресет**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



существующее соединение было принудительно завершено удаленным узлом.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**всаенобуфс**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



Не удалось выполнить операцию с сокетом, так как в системе недостаточно места в буфере или из-за переполнения очереди.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**всаеисконн**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Запрос на подключение был сделан на уже подключенном сокете.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**всаенотконн**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



Запрос на отправку или получение данных отклонен, так как сокет не подключен и (при отправке по сокету датаграмм через вызов sendto) не указан адрес.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**всаешутдовн**
</dt> <dd> <dl> <dt>

10058 (0x274A)
</dt> <dt>



Запрос на отправку или получение данных запрещен, так как сокет уже завершил работу в этом направлении по предыдущему запросу на завершение работы.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**всаетуманирефс**
</dt> <dd> <dl> <dt>

10059 (0x274B)
</dt> <dt>



Слишком много ссылок на некоторый объект ядра.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**всаетимедаут**
</dt> <dd> <dl> <dt>

10060 (0x274C)
</dt> <dt>



Попытка подключения не удалась, так как подключенная сторона не ответила должным образом по истечении определенного периода времени или не удалось установить соединение, так как не удалось ответить подключенному узлу.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**всаеконнрефусед**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



Не удалось установить подключение, так как целевой компьютер отказался от него.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**всаелуп**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



Не удается преобразовать имя.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**всаенаметулонг**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



Имя компонента или имя слишком длинное.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**всаехостдовн**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Сбой операции сокета, так как целевой узел не работает.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**всаехостунреач**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Сделана попытка выполнить операцию на сокете для недоступного хоста.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**всаенотемпти**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



Невозможно удалить каталог, который не является пустым.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**всаепроклим**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



реализация Windowsных сокетов может иметь ограничение на количество приложений, которые могут использовать его одновременно.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**всаеусерс**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Квота исчерпана.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**всаедкуот**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Дисковая квота исчерпана.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**всаестале**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



Ссылка на файл больше недоступна.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**всаеремоте**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



Элемент не доступен локально.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**всасиснотреади**
</dt> <dd> <dl> <dt>

10091 (0x276B)
</dt> <dt>



В настоящее время сбой WSAStartup не может работать, так как базовая система, используемая для предоставления сетевых служб, в данный момент недоступна.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**всавернотсуппортед**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



запрошенная версия сокетов Windows не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**всанотинитиалисед**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



Либо приложение не вызвало сбой WSAStartup, либо сбой сбой WSAStartup.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**всаедискон**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Возвращается функцией Всарекв или Всареквфром, чтобы указать, что удаленная сторона инициировала корректное завершение работы.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**всаеноморе**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



Всалукупсервиценекст не может вернуть дополнительные результаты.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**всаеканцеллед**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



Вызов Всалукупсервицеенд был выполнен во время обработки этого вызова. Вызов отменен.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**всаеинвалидпроктабле**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



Недопустимая таблица вызовов процедур.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**всаеинвалидпровидер**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



Запрошенный поставщик услуг недопустим.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**всаепровидерфаилединит**
</dt> <dd> <dl> <dt>

10106 (0x277A)
</dt> <dt>



Не удалось загрузить или инициализировать запрошенного поставщика услуг.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**всасискаллфаилуре**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Сбой системного вызова.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**ВСАСЕРВИЦЕ \_ не \_ найден**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



Такая служба неизвестна. Не удается найти службу в указанном пространстве имен.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**ВСАТИПЕ \_ не \_ найден**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



Указанный класс не найден.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ больше \_**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



Всалукупсервиценекст не может вернуть дополнительные результаты.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ отменено**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



Вызов Всалукупсервицеенд был выполнен во время обработки этого вызова. Вызов отменен.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**всаерефусед**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Запрос к базе данных не выполнен из-за того, что он был активно отклонен.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**ВСАХОСТ \_ не \_ найден**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



Такой узел не существует.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**ВСАТРИ \_**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Обычно это временная ошибка при разрешении имени узла, и она означает, что локальный сервер не получил ответа от заслуживающего доверия сервера.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_Восстановление всано**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



При просмотре базы данных произошла неисправимая ошибка.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_данные всано**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



Запрошенное имя допустимо, но данные запрошенного типа не найдены.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_получатели качества обслуживания WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



Получен по меньшей мере один резерв.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_отправители качества обслуживания WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



Получен по крайней мере один путь.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ качество обслуживания \_ нет \_ отправителей**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



Отправители отсутствуют.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA \_ качество обслуживания \_ нет \_ получателей**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



Нет получателей.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_запрос на качество обслуживания WSA \_ \_ подтвержден**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



Резервирование подтверждено.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_ \_ Ошибка при допуске обслуживания WSA \_**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Ошибка из-за нехватки ресурсов.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_Ошибка политики качества обслуживания WSA \_ \_**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Отклонено по соображениям администрирования — неверные учетные данные.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ неверный стиль качества обслуживания WSA \_**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Неизвестный или конфликтующий стиль.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_Недопустимый объект качества обслуживания WSA \_ \_**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Проблема с некоторой частью буфера филтерспек или провидерспеЦифик в целом.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_ \_ \_ Ошибка Ctrl трафик качества обслуживания WSA \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Проблема с некоторой частью фловспек.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ Общая ошибка WSA \_ QoS**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Общая ошибка QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ качество обслуживания \_ есервицетипе**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



В фловспек найден недопустимый или Нераспознанный тип службы.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA \_ качество обслуживания \_ ефловспек**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



В структуре QOS обнаружена недопустимая или нераспознанная фловспек.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ качество обслуживания \_ епровспекбуф**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Недопустимый буфер, зависящий от поставщика QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ качество обслуживания \_ ефилтерстиле**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



Использован недопустимый стиль фильтра качества обслуживания.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA \_ качество обслуживания \_ ефилтертипе**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



Использован недопустимый тип фильтра качества обслуживания.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA \_ качество обслуживания \_ ефилтеркаунт**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



В ФЛОВДЕСКРИПТОР указано неверное число Филтерспекс качества обслуживания.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA \_ качество обслуживания \_ еобжленгс**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



В буфере, зависящем от поставщика QOS, был указан объект с недопустимым полем Обжектленгс.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA \_ качество обслуживания \_ ефловкаунт**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



В структуре QOS задано неверное число дескрипторов потока.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ качество обслуживания \_ еунковнпсобж**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



В буфере, зависящем от поставщика QOS, обнаружен нераспознанный объект.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ качество обслуживания \_ еполициобж**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



В буфере, зависящем от поставщика QOS, обнаружен недопустимый объект политики.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ качество обслуживания \_ ефловдеск**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



В списке дескрипторов потока обнаружен недопустимый дескриптор потока качества обслуживания.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ качество обслуживания \_ епсфловспек**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



В буфере, заданном для поставщика QOS, обнаружено недопустимое или непротиворечивое фловспек.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ качество обслуживания \_ епсфилтерспек**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



В буфере, зависящем от поставщика QOS, обнаружен недопустимый ФИЛТЕРСПЕК.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ качество обслуживания \_ есдмодеобж**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



В буфере, заданном поставщиком QOS, обнаружен недопустимый объект режима удаления фигуры.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ качество обслуживания \_ ешаператеобж**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



В буфере, зависящем от поставщика QOS, обнаружен недопустимый объект частоты формирования.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA \_ качество обслуживания \_ зарезервировано \_ петипе**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Зарезервированный элемент политики обнаружен в буфере, зависящем от поставщика QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ не найден безопасный узел \_ WSA**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



Такой узел не известен безопасно.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_ \_ \_ Ошибка политики имен IP WSA IPSec \_**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



Не удалось добавить политику IPSEC на основе имен.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




