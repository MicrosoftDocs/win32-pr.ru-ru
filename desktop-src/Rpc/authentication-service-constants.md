---
title: Константы Authentication-Service (Рпкдце. h)
description: Константы службы проверки подлинности представляют службы проверки подлинности, передаваемые различным функциям времени выполнения.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535111"
---
# <a name="authentication-service-constants"></a>Константы Authentication-Service

Константы службы проверки подлинности представляют службы проверки подлинности, передаваемые различным функциям времени выполнения.

Следующие константы являются допустимыми значениями для параметра *ауснсвк* .



| Константа/значение                                                                                                                                                                                                                                               | Описание                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ нет**</dt> <dt>0</dt> </dl>                              | Без проверки подлинности.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ частный**</dt> <dt>1</dt> </dl>        | Используйте проверку подлинности с закрытым ключом среды распределенных вычислений (DCE).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ Public**</dt> <dt>2</dt> </dl>           | Проверка подлинности с открытым ключом DCE (зарезервировано для будущего использования).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ Dec \_**</dt> <dt>4</dt> </dl>           | Аутентификация с открытым ключом DEC (зарезервировано для будущего использования).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS — \_ согласование**</dt> <dt>9</dt> </dl>  | Используйте [поставщик общих служб Майкрософт для согласования](/windows/desktop/SecAuthN/microsoft-negotiate). Этот поставщик общих служб согласовывает использование протоколов NTLM и протокола безопасности Kerberos (SSP).<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WinNT**</dt> <dt>10</dt> </dl>                          | Используйте [SSP Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SChannel**</dt> <dt>14</dt> </dl>    | Используйте для этого [поставщик общих служб SChannel](/windows/desktop/SecAuthN/secure-channel). Этот поставщик общих служб поддерживает протокол SSL, технологию частной связи (PCT) и безопасность на транспортном уровне (TLS).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Используйте [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | Используйте распределенную проверку пароля (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | SSP протокола проверки подлинности, используемый для сети Microsoft (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ Digest**</dt> <dt>21</dt> </dl>                       | Windows XP или более поздней версии: используйте [дайджест-поставщик Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ \_ Расширитель C AUTHN него**</dt> <dt>30</dt> </dl> | Windows 7 или более поздней версии: зарезервировано. Не использовать<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | Этот поставщик общих служб предоставляет совместимую с SSPI оболочку для протокола транспортного уровня очереди сообщений Майкрософт (MSMQ).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt> </dl>            | Используйте службу проверки подлинности по умолчанию.<br/>                                                                                                                                   |



## <a name="remarks"></a>Комментарии

Укажите RPC \_ C \_ AUTHN \_ None, чтобы отключить проверку подлинности для вызовов удаленных процедур, выполненных на основе маркера привязки. При указании RPC \_ c \_ AUTHN \_ по умолчанию библиотека времени выполнения RPC использует \_ \_ \_ службу проверки подлинности RPC c AUTHN WinNT для удаленных вызовов процедур, выполненных с помощью маркера привязки.

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
</dt> </dl>

 

