---
title: Константы Authorization-Service (Рпкдце. h)
description: Константы службы авторизации представляют службы авторизации, передаваемые различным функциям времени выполнения.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535597"
---
# <a name="authorization-service-constants"></a>Константы Authorization-Service

Константы службы авторизации представляют службы авторизации, передаваемые различным функциям времени выполнения.

Следующие константы являются допустимыми значениями для параметра *аусзсвк* . Большинство приложений находят \_ \_ недостаточный вызов RPC C AUTHZ \_ .



| Константа/значение                                                                                                                                                                                                                                    | Описание                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | Сервер не выполняет авторизацию.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ имя**</dt> <dt>1</dt> </dl>                   | Сервер выполняет авторизацию на основе имени участника клиента.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Сервер выполняет проверку авторизации с помощью сведений о сертификате ключа доступа DCE, которые отправляются на сервер при каждом вызове удаленной процедуры с помощью маркера привязки. Как правило, доступ проверяется по спискам управления доступом DCE ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)).<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt> </dl> | Сервер использует службу авторизации по умолчанию для текущего поставщика общих служб.<br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**рпкбиндингинкаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**рпкбиндингсетаусинфоекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**рпкбиндингинкаусинфоекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[**рпкмгмтинкдефаултпротектлевел**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

