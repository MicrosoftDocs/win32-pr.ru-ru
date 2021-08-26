---
title: Константы службы проверки подлинности (Рпкдце. h)
description: Определяет службы проверки подлинности, определяя пакет безопасности, предоставляющий службу, например NTLMSSP, Kerberos или SChannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14cf6f0ab42b03d028d52df8160cad286e8c37af3988d8ca3b9736dad538012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993784"
---
# <a name="authentication-service-constants"></a>Константы службы проверки подлинности

Определяет службы проверки подлинности, определяя пакет безопасности, предоставляющий службу, например NTLMSSP, Kerberos или SChannel.



| Константа/значение                                                                                                                                                                                                                                               | Описание                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ нет**</dt> <dt>0</dt> </dl>                              | Без проверки подлинности.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ частный**</dt> <dt>1</dt> </dl>        | Проверка подлинности с закрытым ключом DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ Public**</dt> <dt>2</dt> </dl>           | Проверка подлинности открытого ключа DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ Dec \_**</dt> <dt>4</dt> </dl>           | Аутентификация с открытым ключом DEC. Зарезервировано для последующего использования.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS — \_ согласование**</dt> <dt>9</dt> </dl>  | Поставщик поддержки безопасности снего.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WinNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SChannel**</dt> <dt>14</dt> </dl>    | Поставщик поддержки безопасности SChannel. Эта служба проверки подлинности поддерживает SSL 2,0, SSL 3,0, TLS и PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Поставщик поддержки безопасности Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | Поставщик поддержки безопасности DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | Поставщик поддержки безопасности MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ \_ \_ Ядро C AUTHN**</dt> <dt>20</dt> </dl>                       | Поставщик поддержки безопасности ядра.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ Digest**</dt> <dt>21</dt> </dl>                       | Дайджест-поставщик поддержки безопасности.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ \_ Расширитель C AUTHN него**</dt> <dt>30</dt> </dl> | Поставщик поддержки безопасности расширителя него.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Поставщик поддержки безопасности PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | MQ поставщик поддержки безопасности.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt> </dl>           | Системная служба проверки подлинности по умолчанию. Если это значение указано, COM использует стандартный алгоритм согласования безопасности (контракта) для выбора службы проверки подлинности. Дополнительные сведения см. в разделе [Безопасность — общий согласование](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Remarks

Эти константы используются в [**единственной \_ \_ службе проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) и в [**единственной структуре \_ \_ сведений о проверке подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) . **Единственная структура \_ \_ службы проверки подлинности** передается сервером функции [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и может быть получена функцией [**кокуеряусентикатионсервицес**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Указатель на **единственную структуру \_ \_ сведений о проверке подлинности** передается клиентом **CoInitializeSecurity**. Дополнительные сведения о пакетах безопасности, определенных этими значениями, например NTLMSSP и Kerberos, см. в разделе [com и пакеты безопасности](com-and-security-packages.md).

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

 

