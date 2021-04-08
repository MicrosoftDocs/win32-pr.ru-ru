---
title: Структуры RPC
description: В этом разделе объясняются структуры, определенные и используемые в Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Удаленный вызов процедур RPC, ссылки, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793201"
---
# <a name="rpc-structures"></a>Структуры RPC

В этом разделе объясняются структуры, определенные и используемые в Microsoft RPC.

-   [**NDR \_ сконтекст**](/previous-versions/aa374336(v=vs.80))
-   [**УСТРОЙСТВА**](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [**\_ \_ сведения о МАРШАЛИРОВАНИИ пользователя NDR \_**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [**\_ \_ Сведения о МАРШАЛИРОВАНИИ пользователя NDR \_ \_ level1**](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [**\_асинхронные \_ сведения об УВЕДОМЛЕНии RPC \_**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [**\_асинхронное \_ Состояние RPC**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [**\_ \_ Параметры обработчика привязки RPC \_ \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [**\_ \_ Безопасность маркера привязки RPC \_ \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [**\_ \_ Шаблон маркера привязки RPC \_ \_ v1**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [**\_вектор привязки \_ RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [**\_ \_ \_ \_ дескриптор проверки подлинности "RPC C opt" \_**](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [**\_Атрибуты вызова \_ RPC \_ v1**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [**\_Атрибуты вызова \_ RPC \_ v2**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [**\_Локальный адрес удаленного вызова процедур \_ \_ \_ v1**](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [**\_клиентский \_ интерфейс RPC**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [**\_Таблица ДИСПЕТЧЕРИЗАЦИИ \_ RPC**](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [**\_ \_ параметр сведений RPC \_ ee**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [**\_шаблон конечной точки RPC \_**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [**\_ \_ маркер ПЕРЕЧИСЛЕНИЯ ошибок \_ RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [**\_Расширенные \_ сведения об ОШИБКе RPC \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [**\_ \_ \_ учетные данные транспорта HTTP RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [**\_ \_ Учетные данные транспорта HTTP для RPC \_ \_ v2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [**\_ \_ \_ Учетные данные транспорта HTTP RPC \_ v3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [**Идентификатор RPC, \_ Если \_ ИД**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [**RPC, \_ Если \_ идентификатор \_ вектора**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [**\_шаблон интерфейса \_ RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [**\_Политика RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [**\_вектор ПРОТСЕК \_ RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [**Служба \_ безопасности RPC \_ QoS**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [**RPC \_ Security \_ QoS \_ v2**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [**RPC \_ Security \_ QoS \_ v3**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [**RPC \_ Security \_ QoS \_ v4**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [**RPC \_ Security \_ QoS \_ V5**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [**\_вектор статистики \_ RPC**](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [**с \_ WinNT \_ AUTH \_ Identity**](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [**UUID**](./rpcdce/ns-rpcdce-uuid.md)
-   [**\_вектор UUID**](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 