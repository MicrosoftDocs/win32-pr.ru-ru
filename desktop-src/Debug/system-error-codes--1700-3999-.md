---
description: Описание кодов ошибок 1700-3999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Коды системных ошибок (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 707425f7714c84d92bf5bc001f57c1677183b9edbd9170236d1c629bc0aaf121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405605"
---
# <a name="system-error-codes-1700-3999"></a>Коды системных ошибок (1700-3999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1700 – 3999. Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ Недопустимая \_ Привязка строк RPC S \_**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



Недопустимая строка привязки.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_ \_ неправильный \_ тип \_ \_ привязки RPC**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



Недопустимый тип маркера привязки.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_ \_ Недопустимая привязка RPC S \_**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



Недопустимый маркер привязки.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_ПРОТСЕК RPC \_ S \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



Последовательность протокола RPC не поддерживается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ недопустимое \_ \_ протсек RPC**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



Последовательность протокола RPC недопустима.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC \_ S \_ Недопустимая \_ строка \_ UUID**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



Недопустимый универсальный уникальный идентификатор (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ Недопустимый \_ Формат конечной точки RPC S \_**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



Недопустимый формат конечной точки.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ Недопустимый \_ сетевой \_ адрес RPC S**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



Недопустимый сетевой адрес.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ не \_ найдена конечная точка \_**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



Конечная точка не найдена.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_ \_ недопустимое \_ время ожидания RPC S**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



Недопустимое значение времени ожидания.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_объект RPC \_ S \_ не \_ найден**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



Не найден универсальный уникальный идентификатор (UUID) объекта.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ уже \_ зарегистрирован**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



Универсальный уникальный идентификатор (UUID) объекта уже зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_тип RPC \_ S \_ уже \_ зарегистрирован**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



Универсальный уникальный идентификатор (UUID) типа уже зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ уже \_ прослушивает**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



Сервер RPC уже прослушивается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ \_ протсекс не \_ зарегистрирован**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



Последовательности протоколов не зарегистрированы.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ не \_ ожидает передачи данных**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



Сервер RPC не прослушивается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_неизвестный \_ \_ тип диспетчера \_ RPC S**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



Неизвестный тип диспетчера.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ Unknown, \_ Если**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



Неизвестный интерфейс.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ нет \_ привязок**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



Привязки отсутствуют.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ нет \_ протсекс**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



Нет последовательностей протоколов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S не \_ удается \_ создать \_ конечную точку**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



Не удается создать конечную точку.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ не \_ хватает \_ ресурсов**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



Недостаточно ресурсов для выполнения этой операции.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_сервер RPC \_ S \_ недоступен**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



Сервер RPC недоступен.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_сервер RPC \_ S \_ \_ занят**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



Сервер RPC слишком занят для выполнения этой операции.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ недопустимые \_ Параметры сети RPC S \_**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



Недопустимые параметры сети.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ нет \_ \_ активных вызовов**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



В этом потоке отсутствуют активные вызовы удаленных процедур.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_ \_ сбой вызова RPC \_ S**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



Сбой вызова удаленной процедуры.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_ \_ сбой вызова RPC \_ S \_ дне**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



Не удалось выполнить удаленный вызов процедуры, так как он не выполнен.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_ \_ Ошибка протокола RPC \_ S**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Произошла ошибка протокола удаленного вызова процедур (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ доступ прокси-сервера RPC S \_ \_ запрещен**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



Отказано в доступе к прокси-серверу HTTP.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ неподдерживаемый входящий \_ \_ флаг RPC S**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



Синтаксис перемещения не поддерживается сервером RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ неподдерживаемый тип RPC \_ S**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



Тип универсального уникального идентификатора (UUID) не поддерживается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_ \_ Недопустимый \_ тег RPC S**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



Недопустимый тег.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_ \_ Недопустимая привязка RPC S \_**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



Недопустимые границы массива.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ \_ имя записи \_ отсутствует**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



Привязка не содержит имени записи.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_ \_ Недопустимый \_ синтаксис имени RPC S \_**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



Недопустимый синтаксис имени.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_ \_ неподдерживаемый \_ синтаксис имени RPC \_ S**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



Синтаксис имени не поддерживается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_ \_ идентификатор UUID RPC S не является \_ \_ адресом**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



Нет доступного сетевого адреса для создания универсального уникального идентификатора (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ повторяющаяся \_ Конечная точка RPC S**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



Повторяющаяся конечная точка.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_неизвестный \_ \_ тип AUTHN \_ RPC S**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



Неизвестный тип проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ Максимальное число вызовов RPC S \_ \_ слишком \_ мало**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



Максимальное число вызовов слишком мало.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_ \_ \_ слишком \_ длинная строка RPC S**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



Строка слишком длинная.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**\_ПРОТСЕК RPC \_ S \_ не \_ найден**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



Последовательность протокола RPC не найдена.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**\_ПРОКНУМ RPC \_ S \_ за пределами \_ \_ диапазона**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



Номер процедуры выходит за пределы допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**\_Привязка RPC \_ S \_ \_ не имеет \_ проверки подлинности**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



Привязка не содержит сведений о проверке подлинности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_ \_ неизвестная \_ Служба AUTHN RPC S \_**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



Неизвестная служба проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_неизвестный \_ \_ уровень AUTHN \_ RPC S**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



Неизвестный уровень проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ недопустимое \_ удостоверение проверки подлинности RPC S \_**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



Недопустимый контекст безопасности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_ \_ неизвестная \_ Служба AUTHZ RPC S \_**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



Неизвестная служба авторизации.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ Недопустимая \_ запись**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



Недопустимая запись.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S не \_ удается \_ выполнить \_ Op**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



Конечной точке сервера не удается выполнить операцию.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ не \_ зарегистрирован**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



В модуле сопоставления конечных точек больше нет доступных конечных узлов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ нет ничего \_ для \_ экспорта в RPC**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



Нет экспортированных интерфейсов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_неполное \_ \_ имя RPC S**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



Имя записи является неполным.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ недопустимое \_ \_ значение параметра сторно**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



Недопустимый параметр версии.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ \_ больше нет \_ \_ членов**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



Больше нет членов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ не \_ все \_ OBJ-файлы \_ Экспорт**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



Нет ничего для экспорта.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_интерфейс RPC \_ S \_ не \_ найден**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



Интерфейс не найден.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**\_запись RPC \_ S \_ уже \_ существует**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



Запись уже существует.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_запись RPC \_ S \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



Запись не найдена.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_ \_ служба имен RPC \_ \_ недоступна**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



Служба имен недоступна.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ неправильный \_ \_ идентификатор "RPC S"**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



Недопустимое семейство сетевых адресов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ не \_ поддерживает**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



Запрошенная операция не поддерживается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**\_ \_ нет \_ доступных контекстов RPC. \_**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



Нет доступных контекстов безопасности для разрешения олицетворения.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ Внутренняя ошибка RPC \_ S**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Произошла внутренняя ошибка в удаленном вызове процедуры (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ с \_ нулевым \_ делением**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



Сервер RPC попытался выполнить целочисленное деление на ноль.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_ \_ Ошибка адреса RPC \_ S**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Произошла ошибка адресации на сервере RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_0 подключений \_ FP \_ div, \_ ноль**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Операция с плавающей точкой на сервере RPC привела к делению на нуль.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_потеря точности в RPC с \_ плавающей запятой \_**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



На сервере RPC произошла потеря точности с плавающей точкой.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_ \_ переполнение FP в RPC S \_**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Переполнение с плавающей запятой произошло на сервере RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ больше \_ нет \_ записей**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



Список серверов RPC, доступных для привязки автодескрипторов, исчерпан.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ , \_ \_ сбой передачи \_ char**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



Не удалось открыть файл таблицы преобразования символов.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**истечение \_ \_ \_ \_ \_ короткого файла для \_ транзакции RPC X SS**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



Файл, содержащий таблицу преобразования символов, имеет менее 512 байт.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ в \_ \_ контексте null**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



При вызове удаленной процедуры от клиента к узлу был передан нулевой маркер контекста.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_ \_ \_ повреждение контекста RPC X \_ SS**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



Обработчик контекста изменился во время удаленного вызова процедуры.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_ \_ \_ несовпадение дескрипторов RPC X SS \_**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Дескрипторы привязки, переданные удаленному вызову процедуры, не совпадают.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ не \_ может \_ получить \_ маркер вызова**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



Заглушке не удается получить маркер удаленного вызова процедуры.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_ \_ пустой \_ указатель ссылки RPC \_ X**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Заглушке передан пустой указатель ссылки.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ значение перечисления RPC \_ X \_ вне \_ \_ допустимого диапазона**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



Значение перечисления вне диапазона.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**\_ \_ число байт RPC \_ X \_ слишком \_ мало**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



Число байтов слишком мало.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_ \_ неверные \_ данные заглушки RPC X \_**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



Заглушка получила неправильные данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**Ошибка \_ недопустимого \_ \_ буфера пользователя**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



Указанный буфер пользователя недопустим для запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**Ошибка \_ НЕопознанного \_ носителя**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



Дисковый носитель не распознан. Возможно, он не отформатирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**Ошибка \_ без \_ доверия \_ \_ секрет LSA**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



Рабочая станция не имеет секрета доверия.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**Ошибка \_ \_ : нет \_ \_ учетной записи SAM доверия**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



База данных безопасности на сервере не имеет учетной записи компьютера для этого отношения доверия рабочей станции.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**Ошибка \_ доверенного \_ домена при ошибке \_**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



Не удалось установить доверительные отношения между основным доменом и доверенным доменом.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**Ошибка \_ \_ \_ при сбое доверительной связи**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



Сбой отношения доверия между данной рабочей станцией и основным доменом.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**Ошибка \_ доверия \_ при сбое**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Ошибка входа в сеть.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_ \_ выполняется вызов RPC \_ S \_**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



Удаленный вызов процедур уже выполняется для этого потока.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**Ошибка \_ Netlogon \_ не \_ запущена**
</dt> <dd> <dl> <dt>

1792 (0X700)
</dt> <dt>



Предпринята попытка входа в систему, но служба сетевого входа не запущена.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**\_срок действия учетной записи ошибки \_ истек**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



Срок действия учетной записи пользователя истек.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**Перенаправитель ошибок \_ \_ имеет \_ открытые \_ дескрипторы**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



Перенаправитель используется и не может быть выгружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_драйвер принтера \_ ошибок \_ уже \_ установлен**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



Указанный драйвер принтера уже установлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**Ошибка \_ неизвестного \_ порта**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



Указанный порт неизвестен.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**Ошибка \_ неизвестного \_ \_ драйвера принтера**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Неизвестный драйвер принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**Ошибка \_ неизвестного \_ принтпроцессор**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Неизвестный обработчик заданий печати.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**Ошибка \_ недопустимого \_ \_ файла разделителя**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



Указан недопустимый файл разделителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**Ошибка \_ недопустимого \_ приоритета**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



Указан недопустимый приоритет.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**Ошибка \_ недопустимое \_ \_ имя принтера**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



Недопустимое имя принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**\_принтер ошибок \_ уже \_ существует**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



Принтер уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**Ошибка \_ недопустимой \_ \_ команды принтера**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



Недопустимая команда принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**Ошибка \_ недопустимого \_ типа данных**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



Указан недопустимый тип данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**Ошибка \_ недопустимого \_ окружения**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



Указана недопустимая среда.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ больше \_ нет \_ привязок**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



Больше нет привязок.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**Ошибка \_ без входа в \_ \_ \_ УЧЕТную запись междоменного доверия**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



Используемая учетная запись является учетной записью междоменного доверия. Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**Ошибка при \_ \_ \_ \_ учетной записи доверия рабочей станции без входа**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



Используемая учетная запись — это учетная запись компьютера. Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**Ошибка при \_ подключении \_ \_ \_ учетной записи доверия сервера без имени**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



Используемая учетная запись является учетной записью доверия сервера. Для доступа к серверу используйте глобальную учетную запись пользователя или локальную учетную запись пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Ошибка \_ при \_ \_ несоответствии доверия домена**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



Имя или идентификатор безопасности (SID) указанного домена не согласуется со сведениями о доверии для этого домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**\_сервер ошибок \_ имеет \_ открытые \_ дескрипторы**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



Сервер используется и не может быть выгружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**\_ \_ \_ не \_ найдены данные ресурса об ошибке**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



Указанный файл изображения не содержит раздел ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_тип ресурса \_ ошибки \_ не \_ найден**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



Указанный тип ресурса не найден в файле образа.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ не \_ найдено имя ресурса ошибки**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



Указанное имя ресурса не найдено в файле образа.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ не \_ удалось найти язык ресурса ошибок**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



Указанный идентификатор языка ресурсов не найден в файле образа.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**Ошибка \_ \_ недостаточно \_ квоты**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Недостаточно квот для обработки команды.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ нет \_ интерфейсов**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Нет зарегистрированных интерфейсов.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_вызов RPC \_ S \_ отменен**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



Удаленный вызов процедур был отменен.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_Привязка RPC S не \_ \_ завершена**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



Этот маркер привязки не содержит все необходимые сведения.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**сбой связи RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Ошибка связи при удаленном вызове процедуры.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**\_ \_ неподдерживаемый \_ уровень AUTHN RPC \_ S**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



Запрошенный уровень проверки подлинности не поддерживается.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ без \_ \_ имени принк**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



Имя участника не зарегистрировано.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ не \_ \_ Ошибка RPC**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



указанная ошибка не является допустимым Windows кодом ошибки RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ только локальная UUID RPC S \_**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Выделен UUID, допустимый только на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_ \_ \_ \_ Ошибка pkg при вызове RPC S sec**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Произошла ошибка, относящаяся к пакету безопасности.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ не \_ отменен**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



Поток не отменен.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ недопустимое \_ действие ES RPC X \_**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Недопустимая операция с маркером кодирования или декодирования.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**\_ \_ неправильная \_ версия ES RPC X \_**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Несовместимая версия пакета сериализации.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_ \_ неправильная \_ версия заглушки RPC X \_**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Несовместимая версия заглушки RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ Недопустимый \_ \_ объект канала**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



Объект канала RPC недопустим или поврежден.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ \_ неправильный \_ порядок каналов RPC \_ X**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Попытка выполнить недопустимую операцию для объекта канала RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_ \_ неправильная \_ версия канала RPC X \_**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Неподдерживаемая версия канала RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_ \_ \_ Ошибка проверки подлинности cookie RPC S \_**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



Прокси-сервер HTTP отклонил подключение, так как произошел сбой при проверке подлинности файла cookie.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ член группы RPC \_ S \_ не \_ найден**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



Член группы не найден.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S не \_ удается \_ создать**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



Не удалось создать запись базы данных сопоставителя конечных точек.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_ \_ Недопустимый \_ объект RPC S**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



Универсальный уникальный идентификатор (UUID) объекта является пустым UUID.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**Ошибка \_ недопустимое \_ время**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



Указано недопустимое время.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**Ошибка \_ недопустимого \_ \_ имени формы**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



Указано недопустимое имя формы.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**Ошибка \_ недопустимого \_ \_ размера формы**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



Указан недопустимый размер формы.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**Ошибка \_ уже \_ ожидает выполнения**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



Указанный обработчик принтера уже находится в ожидании.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**\_принтер ошибок \_ удален**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



Указанный принтер удален.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**Ошибка \_ недопустимого \_ \_ состояния принтера**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



Недопустимое состояние принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**\_пароль ошибки \_ должен \_ измениться**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



Пароль пользователя необходимо изменить перед входом в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**Ошибка \_ при \_ \_ \_ обнаружении контроллера домена**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Не удалось найти контроллер домена для этого домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**\_учетная запись ошибки \_ заблокирована \_**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



Учетная запись, на которую дана ссылка, заблокирована и не может быть зарегистрирована в.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**ИЛИ \_ недопустимое \_ оксид**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



Указанный объект экспорта объектов не найден.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**ИЛИ \_ Недопустимый \_ OID**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



Указанный объект не найден.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**ИЛИ \_ Недопустимый \_ набор**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



Указанный набор сопоставителя объектов не найден.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**\_ \_ незавершенная отправка RPC S \_**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Некоторые данные будут отправлены в буфер запроса.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ Недопустимый \_ асинхронный обработчик RPC S \_**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Недопустимый асинхронный обработчик вызова удаленной процедуры.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_ \_ Недопустимый \_ асинхронный вызов RPC S \_**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Недопустимый обработчик асинхронных вызовов RPC для этой операции.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_канал RPC \_ X \_ закрыт**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



Объект канала RPC уже закрыт.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_ \_ \_ Ошибка дисциплины канала RPC X \_**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



Вызов RPC завершен до обработки всех каналов.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_канал RPC \_ X \_ пуст**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



Больше нет доступных данных из канала RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**Ошибка \_ No \_ SITENAME**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



Для этого компьютера нет доступных имен сайтов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ОШИБКА не \_ удается \_ получить доступ к \_ файлу**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



Системе не удается получить доступ к файлу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ОШИБКА не \_ удается \_ Разрешить \_ имя файла**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



Имя файла не может быть разрешено системой.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**\_несоответствие \_ типа записи RPC S \_ \_**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



Тип записи отличается от ожидаемого.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**\_ \_ не \_ все \_ OBJ-файлы \_ экспортированы в RPC S**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Не все UUID объекта можно экспортировать в указанную запись.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_интерфейс RPC \_ S \_ не \_ экспортирован**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



Не удалось экспортировать интерфейс в указанную запись.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_профиль RPC \_ S \_ не \_ добавлен**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Не удалось добавить указанную запись профиля.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**удаленное \_ ELT RPC S \_ \_ \_ не \_ Добавлено**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Не удалось добавить указанный элемент профиля.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**\_ \_ \_ \_ не \_ удалено ELT RPC с PRF**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Не удалось удалить указанный элемент профиля.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT \_ не \_ добавлен**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Не удалось добавить элемент Group.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**\_ \_ \_ \_ не \_ удалено ELT для RPC S GRP**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



Не удалось удалить элемент группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**Ошибка \_ \_ заблокирована драйвером на км \_**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



Драйвер принтера несовместим с политикой, включенной на компьютере, которая блокирует драйверы NT 4,0.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**\_ \_ срок действия контекста ошибки истек**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



Срок действия контекста истек, и его больше нельзя использовать.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**\_ \_ \_ \_ превышена квота доверия на пользователя (Error) \_**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



Превышена квота на создание делегированного доверия текущего пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**Ошибка \_ \_ \_ \_ превышения квоты доверия для всех пользователей \_**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



Общая квота на создание делегированного доверия была превышена.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**Ошибка \_ при \_ удалении \_ пользователем \_ превышения квоты доверия \_**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



Превышена квота на удаление делегированного доверия текущего пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**Ошибка \_ при проверке подлинности \_ брандмауэра \_**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



Компьютер, на который вы входите в систему, защищен брандмауэром проверки подлинности. Указанная учетная запись не может пройти проверку подлинности на компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**Ошибка \_ \_ \_ заблокированных подключений удаленной печати \_**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Удаленные подключения к диспетчеру очереди печати блокируются политикой, заданной на компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**Ошибка \_ NTLM \_ заблокирована**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Проверка подлинности не удалась, так как проверка подлинности NTLM отключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_ \_ требуется изменение пароля при ошибке \_**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Ошибка входа. Политика EAS требует, чтобы пользователь изменил свой пароль перед выполнением этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**Ошибка \_ недопустимого \_ \_ формата пикселей**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



Недопустимый формат пикселей.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**Ошибка \_ неправильный \_ драйвер**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



Указан недопустимый драйвер.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**Ошибка \_ недопустимого \_ \_ стиля окна**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



Недопустимый атрибут стиля окна или класса для этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_МЕТАФАЙЛ ошибок \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



Запрошенная операция с метафайлами не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_Преобразование ошибок \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



Запрошенная операция преобразования не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_Обрезка ошибки \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



Запрошенная операция обрезки не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**Ошибка \_ недопустимого модуля \_ CMM**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



Указан недопустимый модуль управления цветом.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**Ошибка при \_ недопустимом \_ профиле**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



Указан недопустимый цветовой профиль.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_тег ошибки \_ не \_ найден**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



Указанный тег не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_тег ошибки \_ отсутствует \_**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



Отсутствует обязательный тег.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**Ошибка \_ дублирования \_ тега**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



Указанный тег уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_профиль ошибок \_ не \_ связан \_ с \_ устройством**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



Указанный цветовой профиль не связан с указанным устройством.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_профиль ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



Указанный цветовой профиль не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**Ошибка \_ недопустимого \_ колорспаце**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



Указано недопустимое цветовое пространство.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**Ошибка \_ ICM \_ не \_ включена**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



Управление цветом изображений не включено.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**Ошибка при \_ удалении \_ ICM \_ XForm**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



При удалении преобразования цветов произошла ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**Ошибка \_ недопустимого \_ преобразования**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



Указано недопустимое преобразование цвета.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**Ошибка \_ колорспаце \_ несоответствие**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



Указанное преобразование не соответствует цветовому пространству точечного рисунка.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**Ошибка \_ недопустимого \_ колориндекс**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



Указанный именованный индекс цвета отсутствует в профиле.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**\_профиль ошибок \_ \_ не \_ соответствует \_ устройству**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



Указанный профиль предназначен для устройства другого типа, отличного от указанного устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**Ошибка \_ подключения к \_ другому \_ паролю**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



Сетевое подключение успешно установлено, но пользователю пришлось запрашивать пароль, отличный от указанного ранее.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**Ошибка \_ подключения к \_ другому \_ паролю \_ по умолчанию**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



Сетевое подключение успешно установлено с использованием учетных данных по умолчанию.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**Ошибка \_ неправильного \_ имени пользователя**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



Указано недопустимое имя пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**Ошибка \_ не \_ подключена**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Это сетевое подключение не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**Ошибка при \_ открытии \_ файлов**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Это сетевое подключение имеет открытые файлы или ожидающие запросы.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ОШИБКИ \_ активных \_ подключений**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Активные соединения по-прежнему существуют.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_ \_ используемое устройство с ошибками \_**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



Устройство используется активным процессом и не может быть отключено.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**Ошибка \_ неизвестного \_ \_ монитора печати**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Указанный монитор печати неизвестен.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_ \_ используется драйвер принтера \_ ошибок \_**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



Указанный драйвер принтера сейчас используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ не \_ найден файл очереди сообщений об ошибках**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



Файл очереди печати не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**Ошибка \_ СПЛ \_ No \_ стартдок**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



Вызов Стартдокпринтер не был выдан.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**Ошибка \_ СПЛ \_ No \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



Вызов AddJob не был выдан.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**\_обработчик печати \_ ошибок \_ уже \_ установлен**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



Указанный обработчик печати уже установлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**монитор печати "ошибка" \_ \_ \_ уже \_ установлен**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



Указанный монитор печати уже установлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**Ошибка при \_ неправильном \_ \_ мониторе печати**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



Указанный монитор печати не имеет необходимых функций.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**Ошибка \_ \_ использования монитора \_ печати \_**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



Указанный монитор печати сейчас используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**на \_ принтере ошибок \_ есть \_ задания \_ в очереди**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



Запрошенная операция не разрешена при наличии заданий в очереди принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**Ошибка \_ " \_ требуется перезагрузка при успешном выполнении" \_**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



Запрошенная операция выполнена успешно. Изменения вступят в силу только после перезагрузки системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**Ошибка при \_ успешном \_ перезапуске \_**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



Запрошенная операция выполнена успешно. Изменения вступят в силу только после перезапуска службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_принтер ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



Принтеры не найдены.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**предупреждение об ОШИБКе \_ \_ драйвера принтера \_**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



Известно, что драйвер принтера является ненадежным.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_драйвер принтера \_ ошибок \_ заблокирован**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



Известно, что драйвер принтера наносит вред системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**\_ \_ \_ используемый пакет драйверов \_ \_ принтера ошибок**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



Указанный пакет драйвера принтера в настоящее время используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_пакет основных \_ драйверов \_ ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



Не удалось найти основной пакет драйверов, необходимый для пакета драйверов принтера.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**Ошибка \_ при \_ перезагрузке не \_ требуется**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



Не удалось выполнить запрошенную операцию. Для отката внесенных изменений требуется перезагрузка системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**Ошибка \_ при \_ перезагрузке не удалось \_ запустить**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



Не удалось выполнить запрошенную операцию. Инициирована перезагрузка системы для отката внесенных изменений.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**\_ \_ \_ требуется загрузка драйвера принтера \_ с ошибками**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



Указанный драйвер принтера не найден в системе и должен быть загружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**Ошибка \_ при \_ \_ перезапуске задания печати \_**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



Не удалось напечатать запрошенное задание печати. Обновление системы печати требует повторной отправки задания.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**Ошибка при \_ неправильном \_ \_ \_ манифесте драйвера принтера**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



Драйвер принтера не содержит допустимого манифеста или содержит слишком много манифестов.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**\_принтер ошибок \_ не является \_ общим**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



Указанный принтер не может быть общим.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**запрос на ошибку \_ \_ приостановлен**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



Операция приостановлена.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**Ошибка \_ ввода-вывода при ошибке \_ \_ в \_ кэше**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Повторите данную операцию в виде кэшированной операции ввода-вывода.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




