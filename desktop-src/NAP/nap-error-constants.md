---
title: Константы ошибок NAP (WinError. h)
description: Следующие константы ошибок NAP определены в файле WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620843"
---
# <a name="nap-error-constants"></a>Константы ошибок NAP

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Следующие константы ошибок NAP определены в файле WinError. h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_ \_ Недопустимый \_ пакет NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270001L)
</dt> <dt>



Недопустимый пакет [**состояния работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**\_ \_ отсутствует \_ состояние работоспособности NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270002L)
</dt> <dt>



В пакете NAP отсутствовало [**состояние работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ \_ конфликтующий идентификатор NAP \_ E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270003L)
</dt> <dt>



Идентификатор сущности конфликтует с уже зарегистрированным ИДЕНТИФИКАТОРом сущности.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**Защита доступа к сети \_ E \_ без \_ кэшированного \_ состояния работоспособности**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270004L)
</dt> <dt>



Отсутствует кэшированное [**состояние работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**\_ \_ по-прежнему \_ привязанный к NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270005L)
</dt> <dt>



Сущность все еще привязана к системе защиты доступа к сети.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**Защита доступа к сети \_ E \_ не \_ зарегистрирована**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270006L)
</dt> <dt>



Сущность не зарегистрирована в системе защиты доступа к сети.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**Защита доступа к сети \_ E \_ не \_ инициализирована**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270007L)
</dt> <dt>



Сущность не инициализирована системой защиты доступа к сети.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ \_ несовпадающий идентификатор NAP \_ E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270008L)
</dt> <dt>



Идентификаторы корреляции в запросе [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) и ответе **SoH** не совпадают.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**Защита доступа к сети \_ E \_ не \_ ожидается**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270009L)
</dt> <dt>



Завершение было указано для запроса, который в настоящий момент не находится в состоянии ожидания.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**Идентификатор защиты доступа к сети ( \_ E) \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000AL)
</dt> <dt>



Идентификатор компонента NAP не найден.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**\_ \_ \_ слишком \_ маленький размер защиты доступа к сети (NAP)**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000BL)
</dt> <dt>



Максимальный размер соединения слишком мал для пакета SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_Служба NAP \_ E \_ не \_ запущена**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000CL)
</dt> <dt>



Служба Напажент не запущена.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_сертификат NAP \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x0027000DL) 
</dt> <dt>



Сертификат уже существует в хранилище сертификатов.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_ \_ отключена сущность NAP E \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000EL)
</dt> <dt>



Сущность отключена в службе Напажент.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_ \_ \_ GROUPPOLICY \_ Ошибка Netsh для защиты доступа к сети**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000FL)
</dt> <dt>



Групповая политика не настроена.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**\_ \_ слишком \_ много вызовов NAP \_ E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270010L)
</dt> <dt>



Слишком много одновременных вызовов.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**Конфигурация средства защиты доступа к сети (NAP) \_ \_ \_ \_ существовала**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270011L)
</dt> <dt>



Конфигурация SHV уже существует.

> [!Note]  
> поддерживается в Windows 7 или более поздней версии.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ не \_ найдена Конфигурация NAP E SHV**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270012L)
</dt> <dt>



Конфигурация SHV не найдена.

> [!Note]  
> поддерживается в Windows 7 или более поздней версии.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_ \_ время ожидания SHV для защиты от NAP \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270013L)
</dt> <dt>



Время ожидания SHV истекло в запросе.

> [!Note]  
> поддерживается в Windows 7 или более поздней версии.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Константы NAP**](nap-constants.md)
</dt> </dl>

 

 





