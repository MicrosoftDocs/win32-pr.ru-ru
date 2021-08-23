---
title: Константы авторизации (Рпкдце. h)
description: Определяет, что авторизует сервер.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048672"
---
# <a name="authorization-constants"></a>Константы авторизации

Определяет, что авторизует сервер.



| Константа/значение                                                                                                                                                                                                                                    | Описание                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | Сервер не выполняет авторизацию. В настоящее время RPC \_ c \_ AUTHN \_ WinNT, RPC \_ c \_ AUTHN \_ GSS \_ SChannel и RPC \_ c \_ AUTHN \_ GSS \_ Kerberos используют только RPC \_ c \_ AUTHZ \_ None.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ имя**</dt> <dt>1</dt> </dl>                   | Сервер выполняет авторизацию на основе имени участника клиента. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Сервер выполняет проверку авторизации, используя сведения о сертификате ключа доступа DCE, которые отправляются на сервер при каждом вызове удаленной процедуры, выполненной с помощью маркера привязки. Как правило, доступ проверяется по спискам управления доступом DCE (ACL). <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt> </dl> | DCOM может выбрать уровень авторизации с помощью обычного алгоритма согласования безопасности общего доступа. Дополнительные сведения см. в разделе [Безопасность — общий согласование](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Remarks

Эти константы используются методами интерфейса [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Они используются в структуре [**единственной \_ \_ службы проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , которая извлекается функцией [**кокуеряусентикатионсервицес**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Они также используются в структуре [**единственной \_ \_ информации для проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , которая, в свою очередь, является членом [**единственной структуры \_ \_ списка проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) . Эта структура представляет собой список служб проверки подлинности, выполняемых ими служб авторизации, а также сведения о проверке подлинности для каждой службы передаются функции [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и методу [**Иклиентсекурити:: сетбланкет**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**кокуеряусентикатионсервицес**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**\_сведения о единственной проверке подлинности \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**Единственная \_ Служба проверки подлинности \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

