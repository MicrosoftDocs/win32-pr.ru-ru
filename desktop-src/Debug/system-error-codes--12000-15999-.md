---
description: Описание кодов ошибок 12000-1599, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Коды системных ошибок (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aa250eb26db3a2dfefda4c8b31bb2bbfd5e5d6415ea50d7279121fb09302c7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058994"
---
# <a name="system-error-codes-12000-15999"></a>Коды системных ошибок (12000-15999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 12000 – 15999). Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**Ошибка в \_ Интернете\_\***
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0)
</dt> <dt>



См. [коды ошибок Интернета](../wininet/wininet-errors.md) и WinInet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>**Ошибка \_ \_ Политика QM \_ IPSec \_**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



Указанная политика быстрого режима уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена политика QM IPSec.**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



Указанная политика быстрого режима не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании политики QM \_ IPSec**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Указанная политика быстрого режима используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**Ошибка \_ Политика протокола IPsec \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



Указанная политика основного режима уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена политика mm для IPSec**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



Указанная политика основного режима не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**Ошибка \_ \_ \_ \_ при \_ использовании политики протокола IPsec mm**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Указанная политика основного режима используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**Ошибка \_ фильтр протокола IPsec \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



Указанный фильтр основного режима уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не найден фильтр IPSec \_ mm**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



Указанный фильтр основного режима не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**Ошибка \_ \_ Фильтр транспорта \_ IPSec \_**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



Указанный фильтр транспортного режима уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена фильтр транспорта IPSec**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



Указанный фильтр транспортного режима не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**Ошибка \_ \_ \_ проверки подлинности IPsec mm \_**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



Указанный список проверки подлинности в основном режиме существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**Ошибка \_ \_ \_ \_ не найдена проверка подлинности IPsec mm \_**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



Указанный список проверки подлинности в основном режиме не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании проверки подлинности IPsec mm \_**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Используется указанный список проверки подлинности в основном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**Ошибка \_ IPSec \_ по умолчанию \_ \_ \_ не \_ найдена политика mm**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



Указанная политика основного режима по умолчанию не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**Ошибка \_ IPSec \_ по умолчанию \_ \_ \_ не найдена проверка подлинности mm \_**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



Указанный список проверки подлинности основного режима по умолчанию не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**Ошибка \_ IPSec \_ Default \_ QM \_ политика \_ не \_ найдена**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



Указанная политика быстрого режима по умолчанию не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**Ошибка \_ \_ Фильтр туннеля \_ IPSec \_**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Указанный фильтр режима туннелирования существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена фильтр туннеля IPSec**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



Указанный фильтр туннельного режима не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра IPSec mm \_**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



Фильтр основного режима ожидает удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра транспорта \_ IPSec**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



Фильтр транспорта ожидает удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра туннеля \_ IPSec**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



Фильтр туннеля ожидает удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления политики IPSec mm \_**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



Политика основного режима ожидает удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**Ошибка \_ \_ \_ проверки подлинности при \_ ожидании \_ удаления с IPSec mm**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



Идет удаление пакета проверки подлинности основного режима.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления политики IPSec QM \_**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



Политика быстрого режима ожидает удаления.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**предупреждение \_ об \_ \_ очистке политики IPSec mm \_**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



Политика основного режима успешно добавлена, но некоторые из запрошенных предложений не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**предупреждение \_ об \_ \_ очистке политики IPSec QM \_**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



Политика быстрого режима успешно добавлена, но некоторые из запрошенных предложений не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**Ошибка \_ при \_ \_ \_ \_ начале состояния "сбой IPSec IKE"**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



Ошибка \_ при \_ \_ \_ \_ начале состояния "сбой IPSec IKE"


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**Ошибка \_ \_ \_ проверки подлинности IPsec IKE \_**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Учетные данные проверки подлинности IKE недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**Ошибка при сбое в IPSec для ошибки \_ \_ IKE \_ \_**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Атрибуты безопасности IKE недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**Ошибка \_ \_ \_ ожидания согласования IKE IPSec \_**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Выполняется согласование IKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**Ошибка \_ при \_ \_ общей \_ обработке \_ IPSec IKE**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Общая ошибка обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**Ошибка при истечении \_ \_ \_ времени \_ ожидания IKE IPSec**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Истекло время ожидания согласования.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ сертификата**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE не удалось найти допустимый сертификат компьютера. Обратитесь к администратору безопасности сети, чтобы установить действительный сертификат в соответствующем хранилище сертификатов.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**Ошибка \_ при \_ \_ удалении SA IPsec IKE \_**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



SA IKE удалено одноранговым узлом перед завершением установки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**Ошибка при установке \_ IPSec \_ IKE \_ SA \_**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



SA IKE удалено до завершения установки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**Ошибка при \_ получении из протокола IPsec \_ IKE \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



Слишком длинный запрос на согласование в очереди.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ получения запроса \_**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



Слишком длинный запрос на согласование в очереди.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**Ошибка \_ при \_ \_ \_ отброшении очереди IKE IPSec \_**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



Слишком длинный запрос на согласование в очереди.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**Ошибка \_ при \_ \_ отбрасывания очереди IKE IPSec \_ \_ No \_ mm**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



Слишком длинный запрос на согласование в очереди.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**Ошибка \_ при \_ \_ отбрасывания IPSec IKE \_ без \_ ответа**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Нет ответа от однорангового узла.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**Ошибка \_ \_ \_ \_ отложенной \_ отбрасывания IKE с ошибкой IPSec mm**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



Согласование заняло слишком много времени.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ delaying \_**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



Согласование заняло слишком много времени.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**Ошибка \_ \_ IKE IPSec \_ об ошибке**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Произошла неизвестная ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**Ошибка \_ IPSec \_ IKE \_ CRL \_**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Проверка отзыва сертификата не пройдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимое \_ \_ Использование ключа**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Недопустимое использование ключа сертификата.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ \_ тип сертификата**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Недопустимый тип сертификата.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ закрытого \_ ключа**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



Сбой согласования IKE, так как используемый сертификат компьютера не имеет закрытого ключа. Для сертификатов IPsec требуется закрытый ключ. Обратитесь к администратору безопасности сети, чтобы заменить сертификат с закрытым ключом.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**Ошибка \_ \_ \_ одновременного \_ смены ключей IPsec IKE**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Обнаружены одновременные Переключи.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**Ошибка \_ IPSec \_ \_ Сбой IKE DH \_**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Сбой в Diffie-Hellmanных вычислениях.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**Ошибка \_ \_ \_ \_ \_ не распознана критическая \_ нагрузка IPSec IKE**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Не знает, как обрабатывать критически важные полезные данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**Ошибка \_ \_ \_ неправильного \_ заголовка IPSec IKE**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Недопустимый заголовок.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ политики**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Политика не настроена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**Ошибка \_ \_ \_ недопустимой подписи IPSec IKE \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Не удалось проверить подпись.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**Ошибка \_ IPSec \_ IKE \_ Kerberos \_**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Не удалось выполнить проверку подлинности с помощью Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ открытого \_ ключа**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



У сертификата узла нет открытого ключа.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**Ошибка \_ протокола IPsec \_ IKE для \_ процесса \_**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Ошибка при обработке полезных данных ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**Ошибка \_ IPSec \_ процесса IKE об ошибке \_ \_ \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Ошибка обработки полезных данных SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**Ошибка сообщения об ошибке \_ \_ процесса IKE при IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Ошибка обработки полезных данных предложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ Process \_ Err \_**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Ошибка обработки полезных данных преобразования.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**Ошибка \_ ошибки \_ IKE при \_ обработке протокола \_ IPSec \_**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Ошибка обработки полезных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**Ошибка \_ с \_ \_ \_ идентификатором Err процесса IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Ошибка при обработке полезных данных идентификатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**Ошибка \_ при \_ \_ работе с \_ \_ сертификатом сообщения Err IKE**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Ошибка обработки полезных данных сертификата.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**Ошибка \_ IPSec \_ процесс IKE, запрос \_ \_ \_ сертификата Err \_**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Ошибка обработки полезных данных запроса на сертификат.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**Ошибка при проверке погрешности \_ протокола IPsec \_ IKE \_ \_ \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Ошибка при обработке полезных данных хэша.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ \_ \_**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Ошибка при обработке полезных данных сигнатуры.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**Ошибка сообщения об ошибке для \_ \_ процесса IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Ошибка обработки полезных данных nonce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**Ошибка \_ при \_ \_ \_ \_ уведомлении об ошибке процесса IKE IPSec**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Ошибка обработки полезных данных уведомления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**Ошибка \_ при \_ \_ удалении IKE \_ процесса \_ IPSec**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Ошибка при обработке полезных данных удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**Ошибка \_ \_ \_ поставщика Err для процесса IKE \_ IPSec \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Ошибка обработки полезных данных VendorId.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ полезная нагрузка**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Получены недопустимые полезные данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**Ошибка \_ IPSec \_ IKE \_ Load \_ \_ Software SA**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Мягкое SA загружено.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**Ошибка \_ при \_ \_ \_ \_ отключении мягкого SA IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Мягкое SA разорвано.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**Ошибка \_ \_ \_ неправильного \_ файла cookie IPSec IKE**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Получен недопустимый файл cookie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ однорангового \_ сертификата**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



Узлу не удалось отправить действительный сертификат компьютера.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**Ошибка \_ \_ \_ при сбое однорангового \_ списка отзыва сертификатов IPsec IKE \_**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Сбой проверки отзыва сертификата узла.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**Ошибка \_ при \_ \_ изменении политики \_ IKE IPSec**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Новая политика не прошла проверку SAs, сформированной с помощью старой политики.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**Ошибка \_ IPSec \_ IKE \_ No \_ mm, \_ Политика**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Нет доступной политики IKE основного режима.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**Ошибка \_ IPSec \_ IKE \_ ноткбприв**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Не удалось включить привилегии TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**Ошибка \_ IPSec \_ IKE \_ секлоадфаил**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Не удалось загрузить SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**Ошибка \_ IPSec \_ IKE \_ фаилсспинит**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Не удалось получить адрес диспетчеризации таблицы функции безопасности от SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**Ошибка \_ IPSec \_ IKE \_ фаилкуериссп**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Не удалось запросить пакет Kerberos для получения максимального размера токена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**Ошибка \_ IPSec \_ IKE \_ срваккфаил**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Не удалось получить учетные данные сервера Kerberos для \_ службы IKE/Error IPSec \_ . Проверка подлинности Kerberos не будет работать. Наиболее вероятной причиной этого является отсутствие членства в домене. Это нормально, если компьютер входит в рабочую группу.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**Ошибка \_ IPSec \_ IKE \_ срвкуерикред**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Не удалось определить имя участника SSPI для \_ службы IKE/Error IPSec \_ ([**куерикредентиалсаттрибутес**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**Ошибка \_ IPSec \_ IKE \_ жетспифаил**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Не удалось получить новый SPI для входящего SA из драйвера IPsec. Наиболее распространенной причиной этого является то, что драйвер не имеет нужного фильтра. Проверьте политику, чтобы проверить фильтры.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**Ошибка \_ \_ \_ неверного \_ фильтра IPSec IKE**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Данный фильтр недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**Ошибка \_ \_ \_ нехватки \_ памяти IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Ошибка выделения памяти.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**Ошибка \_ IPSec \_ IKE \_ \_ \_ не удалось добавить ключ обновления \_**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Не удалось добавить сопоставление безопасности в драйвер IPsec. Наиболее распространенной причиной этого является то, что согласование IKE заняло слишком много времени. Если проблема будет повторяться, уменьшите нагрузку на неисправный компьютер.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Политика**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Недопустимая политика.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**Ошибка \_ IPSec \_ IKE \_ Unknown \_ ДОИ**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



Недопустимый ДОИ.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**Ошибка \_ \_ \_ неправильной \_ ситуации IPSec IKE**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Недопустимая ситуация.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**Ошибка \_ IPSec \_ IKE \_ DH- \_ сбой**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Сбой Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Группа**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Недопустимая группа Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**Ошибка \_ \_ шифрования IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Ошибка при шифровании полезных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**Ошибка \_ \_ \_ расшифровки IPSec IKE**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Ошибка при расшифровке полезных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**Ошибка \_ \_ \_ соответствия политике IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Ошибка соответствия политики.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**Ошибка \_ \_ \_ неподдерживаемого идентификатора IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



Неподдерживаемый идентификатор.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**Ошибка \_ \_ \_ неверного \_ хэша IPSec IKE**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Проверка хэша не пройдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**Ошибка \_ \_ IKE IPSec \_ -Недопустимый \_ алгоритм хэширования \_**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Недопустимый хэш-алгоритм.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**Ошибка \_ IPSec \_ IKE \_ -Недопустимый \_ \_ Размер хэша**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Недопустимый размер хэша.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ \_ алгоритм шифрования**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Недопустимый алгоритм шифрования.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ алгоритм проверки подлинности \_**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Недопустимый алгоритм проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**Ошибка \_ \_ \_ неправильной \_ подписи IPSec IKE**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Недопустимая подпись сертификата.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**Ошибка \_ \_ \_ при загрузке IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Сбой загрузки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**Ошибка \_ IPSec \_ IKE \_ RPC \_ Delete**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Удалено через вызов RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**Ошибка \_ при \_ \_ \_ переинициализации IKE IPSec**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Временное состояние, созданное для выполнения повторной инициализации. Это не реальный сбой.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимое \_ \_ уведомление о времени существования респондента \_**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



значение времени существования, полученное в поле уведомления о времени жизни респондента, ниже Windows 2000, настроенного минимального значения. Исправьте политику на одноранговом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Основная \_ версия**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Получателю не удается управлять версией IKE, указанной в заголовке.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ сертификат \_ кэйлен**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



Длина ключа в сертификате слишком мала для настроенных требований безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**\_ \_ \_ предел IKE mm \_ , ошибка IPSec**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Превышено максимальное число установленных одноранговых сопоставлений MM SAs.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**Ошибка \_ при \_ \_ отключенном согласовании IKE IPSec \_**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE получила политику, которая отключает согласование.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ Limit**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Достигнуто максимальное ограничение быстрого режима для основного режима. Будет запущен новый основной режим.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**Ошибка \_ \_ IKE \_ mm с \_ истекшим сроком действия**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



Срок жизни SA основного режима истек, или узел отправил удаление в основном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**Ошибка \_ \_ \_ предполагается, что одноранговый mm IKE не является \_ \_ \_ допустимым**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Предполагается, что SA основного режима недопустимо, так как одноранговый узел перестал отвечать.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**Ошибка \_ при \_ \_ \_ \_ несоответствии политики цепочки сертификатов IKE IPSec \_**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



Сертификат не цепочка доверенного корня в политике IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**Ошибка \_ \_ \_ непредусмотренного \_ идентификатора сообщения IPSec IKE \_**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Получен непредвиденный идентификатор сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимые \_ полезные данные проверки подлинности \_**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Получены недопустимые предложения проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**Ошибка \_ при \_ \_ \_ отправке куки-файла cookie IKE DOS \_**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Отправлен файл cookie DoS на уведомление инициатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**Ошибка \_ при \_ \_ завершении работы IPsec IKE \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Служба IKE завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**Ошибка \_ \_ \_ \_ при проверке подлинности IPsec IKE КГА \_**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Не удалось проверить привязку между адресом КГА и сертификатом.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ \_ \_ натоа**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Ошибка при обработке полезных данных Натоа.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ mm \_ для \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Параметры основного режима недопустимы для этого быстрого режима.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ срок действия истек**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



Срок действия SA быстрого режима истек для драйвера IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**Ошибка \_ \_ IKE " \_ слишком \_ много \_ фильтров IPsec"**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Обнаружено слишком много динамически добавляемых фильтров IKEEXT.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**Ошибка \_ при \_ \_ \_ \_ истечении состояния "сбой IPSec IKE"**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



Ошибка \_ при \_ \_ \_ \_ истечении состояния "сбой IPSec IKE"


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**Ошибка \_ IPSec \_ IKE \_ Kill \_ фиктивный \_ \_ туннель NAP**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



Повторная проверка подлинности NAP прошла удачно, и необходимо удалить фиктивный туннель IKEv2 для NAP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**Ошибка \_ \_ \_ \_ \_ при назначении внутреннего IP-адреса IPSec IKE \_**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Ошибка при назначении внутреннего IP-адреса инициатору в туннельном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**Ошибка \_ IPSec \_ IKE \_ не \_ требуется \_ полезных данных CP \_**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Требуется отсутствие полезных данных конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**Ошибка \_ при \_ \_ \_ согласовании олицетворения модуля \_ ключей \_ IPSec**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Выполняется согласование в качестве участника безопасности, который выдал подключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**Ошибка \_ при \_ \_ ПОДАВЛЕНии сосуществования IKE IPSec \_**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA удалено из-за отключения проверки сосуществования в IKEv1/AuthIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**Ошибка \_ IPSec \_ IKE \_ рателимит \_ DROP**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



Входящий запрос SA был удален из-за ограничения скорости однорангового IP-адреса.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**Ошибка \_ IPSec \_ IKE \_ \_ \_ не поддерживает \_ мобике**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



Одноранговый узел не поддерживает МОБИКЕ.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**Ошибка \_ \_ \_ при проверке IPSec IKE \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Установка SA не разрешена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности \_ при сбое авторизации в IPSec IKE**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



Установка SA не разрешена, так как не существует достаточно строгих учетных данных на основе PKINIT.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**Ошибка \_ \_ авторизации IKE IPSec при \_ \_ \_ \_ необязательной \_ повторной попытке**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Установка SA не разрешена. Может потребоваться ввести обновленные или другие учетные данные, например смарт-карту.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности \_ при проверке \_ \_ согласованности IPSec IKE и цертмап**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



Установка SA не разрешена, так как не существует достаточно строгих учетных данных на основе PKINIT. Это может быть связано со сбоем сопоставления сертификатов и учетных записей для сопоставления безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**Ошибка \_ при \_ \_ \_ \_ расширенном завершении сообщения IKE о состоянии \_ IPSec**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



Ошибка \_ при \_ \_ \_ \_ расширенном завершении сообщения IKE о состоянии \_ IPSec


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**Ошибка \_ IPSec \_ Bad \_ SPI**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



Индекс SPI в пакете не соответствует действительному сопоставлению безопасности IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**Ошибка \_ \_ \_ времени существования SA IPsec \_ истекло**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Пакет был получен на сопоставление безопасности IPsec, срок действия которого истек.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**Ошибка \_ IPSec с \_ неверным \_ SA**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Пакет был получен на сопоставление безопасности IPsec, которое не соответствует характеристикам пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**Ошибка \_ \_ \_ при проверке воспроизведения IPSec \_**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Сбой при проверке воспроизведения порядкового номера пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**Ошибка \_ \_ недопустимого \_ пакета IPSec**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



Недопустимый заголовок или трейлер IPsec в пакете.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**Ошибка \_ \_ \_ при проверке целостности \_ IPSec**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Проверка целостности IPsec не пройдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**Ошибка \_ при \_ \_ отбрасывания открытого текста IPSec \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec отбросил пакет с открытым текстом.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**Ошибка \_ при \_ \_ отбрасывания брандмауэра проверки подлинности IPsec \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec отбросил входящий пакет ESP в режиме прошедшего проверку подлинности брандмауэра. Это немягкое удаление.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**Ошибка \_ \_ сброса регулирования IPSec \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec отбросил пакет из-за регулирования DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**Ошибка \_ в \_ \_ блоке досп IPSec**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



Защита с помощью IPsec DoS соответствует явному правилу блокировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**Ошибка \_ IPSec \_ досп \_ получения \_ многоадресной рассылки**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



Протокол IPsec DoS Protection получил пакет многоадресной рассылки, зависящий от IPsec, что запрещено.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**Ошибка \_ IPSec \_ досп \_ Недопустимый \_ пакет**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



IPsec DoS Protection получил неправильно отформатированный пакет.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**Ошибка \_ \_ \_ \_ при поиске состояния досп \_ IPSec**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



Защите от вирусов IPsec не удалось найти состояние.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**Ошибка \_ при \_ \_ вводе максимального числа записей IPSec досп \_**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



Защите от вирусов IPsec не удалось создать состояние, так как достигнуто максимально допустимое число записей в политике.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**Ошибка \_ IPSec \_ досп \_ кэймод \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



Защита от вирусов IPsec получила пакет согласования IPsec для модуля создания ключей, который не разрешен политикой.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**Ошибка \_ IPSec \_ досп \_ не \_ установлена**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



Защита от вирусов в ОС DoS не включена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**Ошибка \_ IPSec \_ досп \_ Max \_ для \_ \_ \_ очередей IP рателимит**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



Защите от вирусов IPsec не удалось создать очередь за внутренний предел скорости IP-адресов, так как достигнуто максимальное число очередей, разрешенных политикой.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена раздел SxS**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



Запрошенный раздел отсутствует в контексте активации.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**Ошибка \_ SxS не \_ удается \_ Gen \_ акткткс**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



Не удалось запустить приложение, так как его Параллельная конфигурация неверна. Дополнительные сведения см. в журнале событий приложений или с помощью средства командной строки sxstrace.exe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**Ошибка \_ SxS, \_ Недопустимый \_ \_ Формат актктксдата**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



Недопустимый формат данных привязки приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена сборка SxS**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



Сборка, на которую указывает ссылка, не установлена в системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**Ошибка \_ \_ формата манифеста SxS \_ \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



Файл манифеста не начинается с требуемого тега и сведений о форматировании.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**Ошибка \_ \_ \_ при синтаксическом анализе манифеста SxS \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



Файл манифеста содержит одну или несколько синтаксических ошибок.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**Ошибка \_ \_ \_ отключения контекста активации \_ SxS**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



Приложение попыталось активировать отключенный контекст активации.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена ключ SxS**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



Запрошенный ключ поиска не найден ни в одном из активных контекстов активации.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**Ошибка \_ при \_ \_ конфликте версий SxS**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Версия компонента, необходимая для приложения, конфликтует с другой версией компонента, которая уже активна.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**Ошибка \_ SxS \_ . \_ неправильный \_ тип раздела**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



Раздел контекста активации запрошенного типа не соответствует используемому API запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**Ошибка \_ при \_ \_ отключении запросов потока SxS \_**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



Нехватка системных ресурсов требует отключения изолированной активации для текущего потока выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**Ошибка \_ \_ \_ по умолчанию для процесса SxS \_ уже \_ задана**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Не удалось задать контекст активации по умолчанию для процесса, так как уже задан контекст активации по умолчанию процесса.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**Ошибка \_ \_ неизвестной \_ группы кодирования SxS \_**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



Указанный идентификатор группы кодировок не распознан.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**Ошибка \_ \_ неизвестной \_ кодировки SxS**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



Запрошенная кодировка не распознана.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**Ошибка \_ SxS. \_ Недопустимый \_ \_ URI пространства имен XML \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



Манифест содержит ссылку на недопустимый URI.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**Ошибка \_ \_ \_ \_ \_ не установлена зависимость корневого манифеста SxS \_**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



Манифест приложения содержит ссылку на зависимую сборку, которая не установлена.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**Ошибка \_ при \_ \_ \_ \_ \_ установке зависимости конечного манифеста SxS**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



Манифест для сборки, используемой приложением, имеет ссылку на зависимую сборку, которая не установлена.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**Ошибка \_ SxS. \_ Недопустимый \_ \_ атрибут удостоверения сборки \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



Манифест содержит недопустимый атрибут для удостоверения сборки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**Ошибка \_ \_ манифеста \_ SxS \_ отсутствует \_ необходимое \_ пространство имен по умолчанию**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



В манифесте отсутствует требуемая спецификация пространства имен по умолчанию для элемента Assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**Ошибка \_ \_ манифеста SxS. \_ недопустимое \_ требуемое \_ пространство имен по умолчанию \_**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



Манифест имеет пространство имен по умолчанию, указанное в элементе Assembly, но его значение не равно "urn: schemas-microsoft-com: ASM. v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**Ошибка \_ при \_ \_ \_ перекрестном пути частного манифеста SxS \_ \_ с \_ точкой повторного анализа \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



Проверенный частный манифест превысил путь с неподдерживаемой точкой повторного анализа.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ имя библиотеки DLL \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют файлы с одинаковым именем.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ \_ имя виндовкласс**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют классы окон с одинаковыми именами.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**Ошибка \_ при \_ дублировании CLSID для SxS \_**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют одинаковые идентификаторы CLSID COM-сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**Ошибка \_ при \_ дублировании \_ идентификатора SxS**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Два или более компонентов, на которые напрямую или косвенно ссылается манифест приложения, имеют прокси-серверы для одного и того же интерфейса COM идентификаторов IID.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**Ошибка \_ SxS \_ дублирует \_ тлбид**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют одинаковые Тлбидс библиотеки типов COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**Ошибка \_ при \_ дублировании \_ идентификатора SxS**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Два или более компонента, непосредственно или косвенно упоминаемые в манифесте приложения, имеют одинаковые идентификаторы ProgID COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ \_ имя сборки**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Два или более компонента, непосредственно или косвенно упоминаемые в манифесте приложения, являются разными версиями одного и того же компонента, что не разрешено.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии хэша файла SxS \_**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



Файл компонента не соответствует сведениям проверки, присутствующим в манифесте компонента.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**Ошибка \_ при \_ анализе политики SxS \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



Манифест политики содержит одну или несколько синтаксических ошибок.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингкуоте**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Ошибка анализа манифеста: ожидался строковый литерал, но не найдена открывающая кавычка.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**Ошибка \_ SxS \_ XML \_ E \_ комментсинтакс**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Ошибка анализа манифеста: в комментарии использован неверный синтаксис.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадстартнамечар**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Ошибка анализа манифеста: имя было запущено с недопустимым символом.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**Ошибка \_ SxS \_ XML \_ E \_ баднамечар**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Ошибка анализа манифеста: имя содержит недопустимый символ.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадчаринстринг**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Ошибка анализа манифеста: строковый литерал содержал недопустимый символ.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**Ошибка \_ SxS \_ XML \_ E \_ ксмлдеклсинтакс**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Ошибка анализа манифеста: недопустимый синтаксис объявления XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадчардата**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Ошибка анализа манифеста: в текстовом содержимом обнаружен недопустимый символ.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингвхитеспаце**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Ошибка анализа манифеста: отсутствует обязательный пробел.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**Ошибка \_ SxS \_ XML \_ E \_ експектингтаженд**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Ошибка анализа манифеста: ожидался символ ">".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингсемиколон**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Ошибка анализа манифеста: ожидался символ точки с запятой.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**Ошибка \_ SxS \_ XML \_ E \_ унбаланцедпарен**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Ошибка анализа манифеста: непарные круглые скобки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**Ошибка \_ SxS \_ XML \_ E \_ интерналеррор**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Ошибка анализа манифеста: Внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ непредвиденный \_ пробел**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Ошибка анализа манифеста: пробелы в этом месте не разрешены.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**Ошибка \_ \_ \_ \_ неполной кодировки SxS XML E \_**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Ошибка анализа манифеста: достигнут конец файла в недопустимом состоянии для текущей кодировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**Ошибка \_ SxS \_ XML \_ E \_ отсутствует \_ скобка**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Ошибка анализа манифеста: отсутствует круглая скобка.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**Ошибка \_ SxS \_ XML \_ E \_ експектингклосекуоте**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Ошибка анализа манифеста: отсутствует одинарная или двойная закрывающая кавычка ( \\ "или \\ ").


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**Ошибка \_ SxS \_ XML \_ E \_ несколько \_ двоеточий**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Ошибка анализа манифеста: в имени не допускается несколько двоеточий.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**Ошибка \_ SxS \_ XML \_ E \_ недопустимое \_ десятичное число**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Ошибка анализа манифеста: недопустимый символ для десятичной цифры.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**Ошибка \_ SxS \_ XML \_ E \_ недопустимое \_ шестнадцатеричное представление**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Ошибка анализа манифеста: недопустимый символ для шестнадцатеричной цифры.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимая \_ кодировка Юникод**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Ошибка анализа манифеста: недопустимое значение символа Юникода для этой платформы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**Ошибка \_ SxS \_ XML \_ E \_ вхитеспацеоркуестионмарк**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Ошибка анализа манифеста: ожидается пробел или "?".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унекспектедендтаг**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Ошибка анализа манифеста: в этом месте не ожидался конечный тег.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседтаг**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Ошибка анализа манифеста: следующие теги не закрыты: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**Ошибка \_ SxS \_ XML \_ E \_ дупликатеаттрибуте**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Ошибка анализа манифеста: дублирующийся атрибут.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**Ошибка \_ SxS \_ XML \_ E \_ мултиплерутс**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Ошибка анализа манифеста: в XML-документе допускается только один элемент верхнего уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалидатрутлевел**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Ошибка анализа манифеста: недопустимо на верхнем уровне документа.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадксмлдекл**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Ошибка анализа манифеста: недопустимое объявление XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингрут**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Ошибка анализа манифеста: XML-документ должен иметь элемент верхнего уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**Ошибка \_ SxS \_ XML \_ E \_ унекспектедеоф**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Ошибка анализа манифеста: непредвиденный конец файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадперефинсубсет**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Ошибка анализа манифеста: нельзя использовать сущности параметров внутри объявлений разметки во внутреннем подмножестве.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседстарттаг**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Ошибка анализа манифеста: элемент не закрыт.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседендтаг**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Ошибка анализа манифеста: в элементе End отсутствовал символ ">".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседстринг**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Ошибка анализа манифеста: строковый литерал не закрыт.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседкоммент**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Ошибка анализа манифеста: комментарий не закрыт.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседдекл**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Ошибка анализа манифеста: объявление не закрыто.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседкдата**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Ошибка анализа манифеста: раздел CDATA не закрыт.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ ресерведнамеспаце**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Ошибка анализа манифеста: префикс пространства имен не может начинаться с зарезервированной строки "XML".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалиденкодинг**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Ошибка анализа манифеста: система не поддерживает указанную кодировку.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалидсвитч**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Ошибка анализа манифеста: переключение с текущей кодировки на указанную не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадксмлкасе**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Ошибка анализа манифеста: имя "XML" зарезервировано и должно быть указано в нижнем регистре.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимый \_ автономный**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Ошибка анализа манифеста: Изолированный атрибут должен иметь значение "Yes" или "No".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**Ошибка \_ SxS \_ XML \_ E \_ непредвиденная \_ Автономная**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Ошибка анализа манифеста: Автономный атрибут не может использоваться во внешних сущностях.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимая \_ версия**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Ошибка анализа манифеста: недопустимый номер версии.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссинжекуалс**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Ошибка анализа манифеста: отсутствует знак равенства между атрибутом и значением атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**Ошибка \_ \_ \_ при восстановлении защиты SxS \_**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Ошибка защиты сборки: не удалось восстановить указанную сборку.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**Ошибка \_ \_ открытого ключа защиты SxS, \_ \_ \_ слишком \_ короткий**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Ошибка защиты сборки: открытый ключ для сборки слишком короткий, чтобы быть разрешенным.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**Ошибка \_ \_ \_ \_ \_ Недопустимый каталог защиты SxS**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Ошибка защиты сборки: Каталог для сборки является недопустимым или не соответствует манифесту сборки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**Ошибка \_ \_ переводимого значения HRESULT при непреобразовании SxS \_**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Не удалось преобразовать значение HRESULT в соответствующий код ошибки Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**Ошибка \_ в \_ \_ файле каталога \_ защиты \_ SxS**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Ошибка защиты сборки: отсутствует каталог для сборки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**Ошибка \_ SxS \_ . \_ отсутствует \_ атрибут удостоверения сборки \_**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



В указанном удостоверении сборки отсутствует один или несколько атрибутов, которые должны присутствовать в этом контексте.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ \_ имя атрибута \_ удостоверения сборки**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



Предоставленное удостоверение сборки имеет одно или несколько имен атрибутов, содержащих символы, запрещенные в именах XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**Ошибка \_ \_ сборки SxS \_**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Не удалось найти сборку, на которую указывает ссылка.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**Ошибка \_ SxS, \_ поврежденный \_ \_ стек активации**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



Стек активации контекста активации для выполняющегося потока поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**Ошибка \_ при \_ повреждении SxS**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Метаданные изоляции приложения для этого процесса или потока были повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**Ошибка \_ при \_ ранних \_ деактивации SxS**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Деактивируемый контекст активации не является самой последней активацией.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**Ошибка \_ \_ неправильной \_ деактивации SxS**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Деактивируемый контекст активации неактивен для текущего потока выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**Ошибка \_ при \_ множественной \_ деактивации SxS**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Деактивируемый контекст активации уже деактивирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**Ошибка \_ при \_ \_ завершении завершения процесса SxS \_**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Компонент, используемый средством изоляции, запросил завершить процесс.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**Ошибка \_ \_ \_ контекста активации выпуска \_ SxS**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Компонент режима ядра освобождает ссылку на контекст активации.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**Ошибка \_ SxS \_ . \_ \_ контекст активации по умолчанию для системы \_ \_**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Не удалось создать контекст активации системной сборки по умолчанию.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ значение атрибута Identity \_**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



Значение атрибута в удостоверении находится за пределами допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ имя атрибута удостоверения \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



Имя атрибута в удостоверении находится за пределами допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**Ошибка \_ \_ \_ дублирования атрибута удостоверения SxS \_**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Удостоверение содержит два определения для одного и того же атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**Ошибка \_ \_ \_ синтаксического анализа удостоверения SxS \_**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



Строка удостоверения имеет неправильный формат. Это может быть вызвано завершающей запятой, более чем двумя неименованными атрибутами, отсутствием имени атрибута или отсутствующим значением атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**Ошибка при \_ оформлении \_ строки подстановки \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Строка, содержащая локализованное подставляемое содержимое, имеет неправильный формат. За символом доллара ($) следует не левая круглая скобка или другой знак доллара, либо правая скобки подстановки не найдены.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**Ошибка \_ SxS \_ . \_ неправильный \_ токен открытого ключа \_**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



Токен открытого ключа не соответствует указанному открытому ключу.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**Ошибка при \_ НЕсопоставленной \_ строке подстановки \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Строка подстановки не имеет сопоставления.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**Ошибка \_ " \_ Сборка SxS \_ не \_ заблокирована"**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



Перед выполнением запроса компонент должен быть заблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**Ошибка \_ при \_ \_ повреждении хранилища компонентов SxS \_**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



Хранилище компонентов повреждено.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**Ошибка \_ расширенного \_ установщика ошибок \_**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Сбой расширенного установщика во время установки или обслуживания.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**Ошибка \_ при \_ несоответствии кодировки XML \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



Кодировка символов в объявлении XML не соответствует кодировке, используемой в документе.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**Ошибка \_ \_ идентичности манифеста SxS, \_ \_ \_ но \_ содержимое \_ отличается**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Удостоверения манифестов идентичны, но их содержимое отличается.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ОШИБКИ \_ , \_ отличные от удостоверений SxS \_**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Идентификаторы компонентов различаются.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**Ошибка \_ \_ сборки SxS \_ \_ не является \_ \_ развертыванием**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



Сборка не является развертыванием.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**Ошибка \_ SxS. \_ файл \_ не является \_ частью \_ \_ сборки**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Файл не является частью сборки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**Ошибка \_ \_ \_ слишком большой манифест \_ SxS**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



Размер манифеста превышает максимально допустимое значение.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**Ошибка \_ \_ \_ не \_ зарегистрирована параметр SxS**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



Параметр не зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**Ошибка \_ \_ \_ неполной закрытия транзакции SxS \_**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Отсутствует один или несколько обязательных элементов транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**Ошибка \_ \_ \_ при выполнении установщика примитива SMI \_**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Сбой установщика примитива SMI во время установки или обслуживания.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**Ошибка \_ \_ \_ при выполнении универсальной команды**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Исполняемый файл универсальной команды вернул результат, который указывает на сбой.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**Ошибка \_ при \_ \_ отсутствии хэша \_ файла SxS**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



В манифесте компонента отсутствуют сведения о проверке файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Ошибка \_ evt \_ недопустимого \_ \_ пути канала**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



Указан недопустимый путь к каналу.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Ошибка \_ \_ недопустимого \_ запроса evt**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



Указан недопустимый запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Ошибка \_ \_ \_ \_ не найдены метаданные издателя \_ evt**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Не удается найти метаданные издателя в ресурсе.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ шаблон событий Error \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



Не удается найти шаблон для определения события в ресурсе (ошибка = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**Ошибка \_ evt \_ недопустимое \_ \_ имя издателя**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



Указано недопустимое имя издателя.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Ошибка \_ evt " \_ недопустимые \_ \_ данные события"**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Данные события, создаваемые издателем, несовместимы с определением шаблона события в манифесте издателя.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_канал ошибки \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



Не удалось найти указанный канал. Проверьте конфигурацию канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**Ошибка \_ evt \_ неправильно сформированный \_ XML- \_ текст**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



Указанный XML-текст имеет неправильный формат. Дополнительные сведения см. в разделе Расширенная ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Ошибка \_ при \_ подписке evt \_ на \_ прямой \_ канал**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



Вызывающая сторона пытается подписываться на прямой канал, что недопустимо. События прямого канала переходят непосредственно в файл журнала и не могут быть подписаны на.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Ошибка \_ \_ конфигурации evt \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Ошибка конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**\_ \_ \_ неактуальный результат \_ запроса "ошибка evt"**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



Результат запроса устарел или недопустим. Это может быть вызвано очисткой или перебором журнала после создания результата запроса. Пользователи должны решить этот код, отпустив объект результата запроса и повторно выполнив запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ошибочное \_ \_ \_ значение результата \_ запроса \_ "ошибка evt"**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



Результат запроса в настоящее время находится в недопустимой позиции.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Ошибка \_ EVT, \_ не \_ проверяя \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



зарегистрированные MSXML не поддерживают проверку.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Ошибка \_ evt \_ Filter \_ алреадископед**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



За выражением может следовать только изменение операции Scope только в том случае, если оно является набором узлов и еще не является частью другого изменения области действия.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Ошибка \_ evt \_ Filter \_ нотелтсет**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Невозможно выполнить шаг с термином, который не представляет набор элементов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Ошибка \_ evt \_ Filter \_ инварг**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Аргументы левой стороны к бинарным операторам должны быть либо атрибутами, либо узлами, либо переменными и аргументами правой части должны быть константы.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Ошибка \_ evt \_ Filter \_ инвтест**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Операция шага должна затрагивать либо проверку узла, либо, в случае предиката, алгебраические выражение, по которому будет проверяться каждый узел в наборе узлов, идентифицируемом предшествующим набором узлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**Ошибка \_ evt \_ Filter \_ инвтипе**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Этот тип данных в настоящее время не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Ошибка \_ evt \_ Filter \_ парсирр**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Синтаксическая ошибка в позиции %1! d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Ошибка \_ evt \_ Filter \_ унсуппортедоп**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Этот оператор не поддерживается этой реализацией фильтра.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Ошибка \_ evt \_ Filter \_ унекспектедтокен**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



Обнаружена непредвиденная лексема.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Ошибка \_ evt \_ недопустимой \_ операции \_ через \_ включенный \_ прямой \_ канал**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



Запрошенная операция не может быть выполнена через включенный прямой канал. Прежде чем выполнять запрошенную операцию, необходимо отключить канал.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства канала \_**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Свойство канала %1! s! содержит недопустимое значение. Значение имеет недопустимый тип, находится вне допустимого диапазона, не может быть обновлено или не поддерживается этим типом канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства издателя \_**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Publisher свойство %1! s! содержит недопустимое значение. Значение имеет недопустимый тип, находится вне допустимого диапазона, не может быть обновлено или не поддерживается издателем этого типа.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**Ошибка \_ при \_ \_ активации канала \_ evt**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



Не удается активировать канал.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**\_ \_ \_ слишком \_ сложный фильтр evt ошибки**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



Выражение XPath превысило поддерживаемую сложность. Симплифи его или разделите его на два или более простых выражения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**сообщение с ошибкой \_ evt \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



ресурс сообщения существует, но сообщение не найдено в строке или таблице сообщений.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ идентификатор сообщения ошибки \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



Не удалось найти идентификатор сообщения для требуемого сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Ошибка \_ EVT, \_ неразрешенное \_ значение \_ INSERT**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



Не удалось найти строку подстановки для индекса вставки (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Ошибка \_ EVT, \_ неразрешенная \_ \_ Вставка параметра**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



Не удалось найти строку описания для ссылки на параметр (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_ \_ \_ достигнуто максимальное число вставок \_ ошибок evt**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



Достигнуто максимальное число замен.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_Определение события "ошибка evt" \_ \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



Не удалось найти определение события для идентификатора события (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ не удалось найти языковой стандарт сообщений \_ с ошибкой evt**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



Не указан ресурс, зависящий от языкового стандарта для требуемого сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**\_ \_ \_ слишком \_ старая версия evt**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



Ресурс слишком старый, чтобы быть совместимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**\_ \_ \_ слишком \_ Новая версия ошибки evt**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



Ресурс слишком новый для совместимости.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Ошибка \_ evt \_ не \_ удается \_ открыть \_ канал \_ запроса**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



Канал по индексу %1! d! не удается открыть запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Ошибка \_ " \_ Издатель evt \_ отключен"**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



Издатель отключен, и его ресурс недоступен. Обычно это происходит, когда издатель находится в процессе удаления или обновления.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ОШИБОЧный \_ \_ Фильтр evt \_ за пределами \_ \_ диапазона**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Попытка создать числовой тип, который находится за пределами допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**Ошибка \_ \_ \_ не удается активировать подписку EC \_**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



Не удается активировать подписку.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**Ошибка \_ EC — \_ Журнал \_ отключен**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



Журнал подписки находится в отключенном состоянии и не может использоваться для перенаправления событий в. Прежде чем активировать подписку, необходимо включить журнал.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**Ошибка \_ EC \_ цикличное \_ перенаправление**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



При пересылке событий с локального компьютера на себя, запрос подписки не может содержать целевой журнал подписки.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**Ошибка \_ EC \_ кредсторе \_ Full**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



Хранилище учетных данных, используемое для сохранения учетных данных, заполнено.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**Ошибка \_ EC \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



Учетные данные, используемые этой подпиской, невозможно найти в хранилище учетных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**Ошибка \_ EC \_ нет \_ активного \_ канала**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Для запроса не найден активный канал.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**файл MUI с ОШИБКАми \_ \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Загрузчику ресурсов не удалось найти файл MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**Ошибка \_ \_ недопустимого \_ файла MUI**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Загрузчику ресурсов не удалось загрузить MUI-файл, так как файл не прошел проверку.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**Ошибка \_ MUI \_ Недопустимая \_ \_ Конфигурация RC**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



Манифест RC поврежден с данными мусора или неподдерживаемой версией, или отсутствует обязательный элемент.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**Ошибка \_ MUI \_ недопустимое \_ имя локали \_**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



Манифест версии-КАНДИДАТа имеет недопустимое имя языка и региональных параметров.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**Ошибка \_ MUI \_ недопустимое \_ \_ имя ултиматефаллбакк**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



Манифест версии-КАНДИДАТа имеет недопустимое имя ултиматефаллбакк.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**файл MUI с ОШИБКАми \_ \_ \_ не \_ загружен**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



Кэш загрузчика ресурсов не загрузил запись MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_ \_ Перечисление \_ пользовательских ресурсов ошибок \_**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



Пользователь остановил перечисление ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**Ошибка \_ многоязыкового интерфейса пользователя \_ интлсеттингс \_ уиланг \_ не \_ установлена**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Не удалось установить язык пользовательского интерфейса.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**Ошибка \_ многоязыкового интерфейса пользователя \_ интлсеттингс \_ недопустимое \_ имя локали \_**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Не удалось установить языковой стандарт.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**Ошибка \_ управления записями сообщений \_ среды выполнения \_ без \_ по умолчанию \_ или \_ нейтрального \_ ресурса**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Ресурс не имеет значения по умолчанию или нейтрального.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**Ошибка \_ управления записями сообщений \_ Недопустимая \_ файлу priconfig**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Недопустимый файл конфигурации PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ \_ Тип файла**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Недопустимый тип файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**Ошибка \_ управления записями сообщений \_ неизвестный \_ квалификатор**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Неизвестный квалификатор.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**Ошибка \_ управления записями сообщений \_ недопустимое \_ значение квалификатора \_**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Недопустимое значение квалификатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**Ошибка \_ управления записями сообщений \_ нет \_ кандидатов**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Кандидатов не найдены.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**Ошибка \_ управления записями сообщений \_ нет \_ совпадения \_ или \_ кандидата по умолчанию \_**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



Ресаурцемап или Намедресаурце имеет элемент, который не имеет по умолчанию или нейтрального ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии типа ресурса управления записями сообщений \_**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Недопустимый тип Ресаурцекандидате.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**Ошибка \_ управления записями сообщений \_ дублирование \_ \_ имени схемы**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Повторяющаяся схема ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**Ошибка \_ управления записями сообщений \_ повторяющаяся \_ запись**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Повторяющаяся запись.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ \_ идентификатор ресурса**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Недопустимый идентификатор ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**Ошибка \_ управления записями сообщений \_ путь к файлу \_ слишком \_ длинный**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



Слишком длинный путь к файлу.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**Ошибка \_ управления записями сообщений \_ неподдерживаемый \_ \_ тип каталога**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Неподдерживаемый тип каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ PRI \_ файл**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Недопустимый PRI файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**Ошибка \_ управления записями сообщений. \_ именованный \_ ресурс \_ не \_ найден**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



Намедресаурце не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**Ошибка \_ управления записями сообщений \_ . \_ не \_ удалось найти карту**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



Ресаурцемап не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**Ошибка \_ управления записями сообщений \_ неподдерживаемый \_ \_ Тип профиля**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Неподдерживаемый тип профиля MRT.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ оператор квалификатора \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Недопустимый оператор квалификатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**Ошибка \_ управления записями сообщений \_ \_ значение квалификатора неопределенности \_**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Не удалось определить значение квалификатора, или значение квалификатора не задано.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**Ошибка \_ управления записями сообщений. \_ Автослияние \_ включено**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



Автослияние включено в PRI-файле.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**Ошибка \_ управления записями сообщений \_ слишком \_ много \_ ресурсов**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Для пакета определено слишком много ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**Ошибка \_ MCA. \_ Недопустимая \_ \_ строка возможностей**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



Монитор вернул строку возможностей DDC/CI, которая не соответствует спецификации доступа. Bus 3,0, DDC/CI 1,1 или MCCS 2 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**Ошибка \_ MCA, \_ Недопустимая \_ \_ версия**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



Код версии-0xDF (версия-перечислитель монитора) вернул недопустимое значение версии.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**\_монитор ошибок \_ MCA \_ нарушает \_ \_ спецификацию MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



Монитор не соответствует спецификации MCCS, которую он требует для поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии версии MCA MCCS \_**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



Версия MCCS в \_ функции MCCS ver монитора не соответствует версии MCCS, которую монитор сообщает при использовании кода версии-0xDF.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**Ошибка \_ MCA \_ неподдерживаемая \_ \_ версия MCCS**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



API конфигурации монитора работает только с мониторами, которые поддерживают спецификацию MCCS 1,0, спецификация MCCS 2,0 или MCCS 2,0 редакции 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**\_ \_ Внутренняя ошибка MCA \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Произошла внутренняя ошибка API настройки монитора.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**Ошибка \_ MCA \_ возвратила недопустимый \_ \_ тип технологии \_**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



Монитор вернул недопустимый тип технологии мониторинга. Примеры типов технологий мониторинга: CRT, плазменный и ЖК-монитор (TFT). Эта ошибка означает, что монитор нарушил спецификацию MCCS 2,0 или MCCS 2,0 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**Ошибка \_ при \_ неподдерживаемой \_ цветовой \_ температуре MCA**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



Вызывающий объект [**сетмониторколортемпературе**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) указал цветовую температуру, которую текущий монитор не поддерживал. Эта ошибка означает, что монитор нарушил спецификацию MCCS 2,0 или MCCS 2,0 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**Ошибка \_ неоднозначных \_ системных \_ устройств**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



Не удается определить запрошенное системное устройство из-за нескольких неразличимых устройств, которые могут соответствовать критериям идентификации.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_системное устройство с ошибками \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Не удается найти запрошенное системное устройство.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_хэш ошибок \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



Создание хэша для указанной версии хэша и типа хэша не включено на сервере.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_хэш ошибки \_ отсутствует \_**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



Хэш, запрошенный с сервера, недоступен или больше не действителен.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**Ошибка \_ \_ \_ \_ не зарегистрирована вторичный поставщик IC \_ .**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



Экземпляр дополнительного контроллера прерываний, управляющий указанным прерыванием, не зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**Ошибка \_ \_ \_ недопустимых сведений о клиенте GPIO \_**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



Недопустимые сведения, предоставленные драйвером GPIO Client.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**Ошибка \_ " \_ версия GPIO \_ не \_ поддерживается"**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



Версия, указанная драйвером GPIO Client, не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**Ошибка \_ GPIO — \_ Недопустимый \_ \_ Пакет регистрации**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



Недопустимый регистрационный пакет, предоставленный драйвером GPIO Client.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**Ошибка \_ GPIO. \_ операция \_ запрещена**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



Запрошенная операция не поддерживается для указанного маркера.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**Ошибка \_ GPIO \_ несовместимого \_ \_ режима подключения**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



Запрошенный режим подключения конфликтует с существующим режимом на одном или нескольких указанных ПИН-кодах.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**Ошибка \_ " \_ прерывание GPIO уже снято с \_ \_ маски"**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



Прерывание, запрошенное для снятия маски, не замаскировано.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**Ошибка \_ не может \_ Переключить \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



Не удается успешно завершить запрошенный параметр уровня выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**Ошибка \_ недопустимого \_ \_ параметра RUNLEVEL**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



Служба имеет недопустимый параметр уровня выполнения. Уровень выполнения для службы не должен быть выше уровня выполнения зависимых служб.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**Ошибка \_ RUNLEVEL \_ \_ время ожидания переключения**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



Не удается успешно выполнить запрошенный параметр уровня выполнения, так как одна или несколько служб не будут перезапущены или перезагружены в течение указанного времени ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**Ошибка \_ RUNLEVEL \_ \_ время ожидания агента коммутатора \_**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Агент переключения уровня выполнения не ответил в течение указанного времени ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**Ошибка \_ \_ \_ при выполнении переключения \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



В настоящее время выполняется переключение уровня выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_ \_ сбой при \_ автозапуске служб ошибок**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Не удалось запустить одну или несколько служб на этапе запуска службы коммутатора уровня выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**Ошибка \_ при \_ \_ ожидании завершения задачи com \_**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



Запрос на остановку задачи не может быть выполнен немедленно, так как для выполнения задачи требуется больше времени для завершения работы.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**Ошибка \_ \_ при установке открытого \_ пакета \_**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Не удалось открыть пакет.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**Ошибка при \_ установке \_ пакета \_ не \_ найдена**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



Пакет не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**Ошибка при \_ установке \_ недопустимого \_ пакета**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Недопустимые данные пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**Ошибка \_ \_ при установке разрешения \_ зависимости \_**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Сбой пакета обновлений, зависимости или проверки конфликтов.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**Ошибка при \_ установке \_ нехватки места на \_ \_ диске \_**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



На компьютере недостаточно дискового пространства. Освободите место и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**Ошибка \_ \_ при установке сетевого \_ сбоя**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



При скачивании продукта возникла проблема.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**Ошибка \_ \_ при регистрации \_ установки**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Не удалось зарегистрировать пакет.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**Ошибка \_ при отмене \_ регистрации установки \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



Не удалось отменить регистрацию пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**Ошибка при \_ установке \_ "Отмена"**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



Пользователь отменил запрос на установку.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**Ошибка \_ \_ при установке**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Сбой установки. Обратитесь к поставщику программного обеспечения.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**Ошибка \_ \_ при удалении**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Сбой удаления. Обратитесь к поставщику программного обеспечения.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**\_пакет ошибок \_ уже \_ существует**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



Указанный пакет уже установлен, и переустановка пакета была заблокирована. Дополнительные сведения см. в журнале событий AppXDeployment-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**Ошибка \_ требует \_ исправления**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



Не удается запустить приложение. Попробуйте переустановить приложение, чтобы устранить проблему.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**Ошибка \_ \_ при установке необходимого компонента \_**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Не удалось удовлетворить необходимым требованиям для установки.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**\_ \_ репозиторий пакета ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



Репозиторий пакетов поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**Ошибка \_ \_ при установке \_ сбоя политики**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



для установки этого приложения требуется либо лицензия разработчика Windows, либо система с поддержкой загрузки неопубликованных приложений.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**Ошибка \_ при \_ обновлении пакета**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



Невозможно запустить приложение, так как оно сейчас обновляется.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_развертывание ошибок \_ заблокировано \_ \_ политикой**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



Операция развертывания пакета заблокирована политикой. Обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_используемые пакеты \_ ошибок \_**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



Не удалось установить пакет, так как ресурсы, которые он изменяет, сейчас используются.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**\_файл восстановления \_ ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



Не удалось восстановить пакет, так как необходимые данные для восстановления повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**Ошибка \_ недопустимой \_ промежуточной \_ подписи**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



Сигнатура недопустима. Для регистрации в режиме разработчика AppxSignature. p7x и AppxBlockMap.xml должны быть допустимыми или отсутствовать.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**Ошибка \_ \_ при удалении \_ существующего \_ хранилища \_ APPLICATIONDATA**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Произошла ошибка при удалении ранее существующих данных приложения пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**Ошибка \_ при \_ установке \_ понижения уровня пакета**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Не удалось установить пакет, поскольку уже установлена более поздняя версия этого пакета.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**\_система ошибок \_ требует \_ исправления**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Обнаружена ошибка в системном двоичном файле. Попробуйте обновить компьютер, чтобы устранить проблему.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**Ошибка \_ \_ проверки целостности APPX в \_ \_ CLR \_ Ngen**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



В системе обнаружен поврежденный двоичный файл среды CLR NGEN.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_ \_ поврежден файл устойчивости к ошибке \_**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



Не удалось возобновить операцию, так как необходимые данные для восстановления повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**Ошибка \_ при \_ установке \_ службы брандмауэра \_ не \_ запущена**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



не удалось установить пакет, так как служба брандмауэра Windows не запущена. включите службу брандмауэра Windows и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_Ошибка APPMODEL \_ без \_ пакета**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



Процесс не имеет удостоверения пакета.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Среда выполнения пакета с ошибками APPMODEL \_ \_ \_ повреждена**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



Сведения о среде выполнения пакета повреждены.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_ \_ удостоверение пакета ошибок APPMODEL \_ \_ повреждено**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



Удостоверение пакета повреждено.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**\_Ошибка APPMODEL \_ нет \_ приложения**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



Процесс не имеет удостоверения приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**Ошибка \_ \_ \_ хранилища при загрузке \_ состояния**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Не удалось загрузить хранилище состояний.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ \_ сбой при получении версии \_ состояния ошибки**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Не удалось получить версию состояния для приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**Ошибка \_ \_ при установке \_ версии состояния ошибки \_**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Не удалось задать версию состояния для приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**Ошибка \_ \_ структурированного \_ сброса состояния ошибки \_**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Не удалось сбросить структурированное состояние приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**Ошибка \_ \_ при открытии \_ контейнера состояния ошибки \_**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Диспетчеру состояний не удалось открыть контейнер.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**Ошибка \_ \_ при создании \_ контейнера состояния ошибки \_**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Диспетчеру состояний не удалось создать контейнер.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**Ошибка \_ \_ при удалении \_ контейнера состояния ошибки \_**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Диспетчеру состояний не удалось удалить контейнер.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_ \_ \_ Сбой настройки чтения состояния \_ ошибки**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Диспетчеру состояний не удалось прочитать параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ \_ Сбой настройки записи состояния \_ ошибки**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Диспетчеру состояний не удалось записать параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**Ошибка \_ \_ при удалении \_ параметра состояния ошибки \_**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Диспетчеру состояний не удалось удалить параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_ \_ \_ сбой параметра запроса состояния \_ ошибки**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Диспетчеру состояний не удалось запросить параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**Ошибка \_ \_ при чтении \_ параметра "составное состояние \_ " \_**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Диспетчеру состояний не удалось считать составной параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**Ошибка \_ \_ при создании \_ составного \_ параметра записи состояния \_ ошибки**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Диспетчеру состояний не удалось записать составной параметр.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**\_ \_ не удалось перечислить \_ контейнер состояния ошибки \_**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Диспетчеру состояний не удалось перечислить контейнеры.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ не удалось перечислить \_ Параметры состояния ошибки \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



Диспетчеру состояний не удалось перечислить параметры.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ Превышено ограничение на размер \_ значения \_ составного параметра состояния ошибки**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



Размер значения составного параметра диспетчера состояний превысил установленное ограничение.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ превышен предел размера значения параметра \_ состояния ошибки**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



Размер значения параметра диспетчера состояний превысил установленное ограничение.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ превышен предельный размер имени параметра состояния ошибки \_**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



Длина имени параметра диспетчера состояний превысила предел.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_ \_ \_ \_ Превышено ограничение на размер имени \_ контейнера \_ состояний ошибок**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



Длина имени контейнера диспетчера состояний превысила предел.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**\_API ошибок \_ недоступен**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Этот API нельзя использовать в контексте типа приложения вызывающего объекта.


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

 

 
