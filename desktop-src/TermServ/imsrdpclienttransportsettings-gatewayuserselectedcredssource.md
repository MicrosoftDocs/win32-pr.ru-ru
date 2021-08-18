---
title: Имсрдпклиенттранспортсеттингс Гатевайусерселектедкредссаурце, свойство
description: Задает или получает указанный пользователем источник учетных данных шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусерселектедкредссаурце
- Службы удаленных рабочих столов свойства Гатевайусерселектедкредссаурце, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайусерселектедкредссаурце
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7632609f34d0133f37af4e8df16ebd574b3ef84e248c2bb3d2b1a84313957b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001014"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>Свойство Имсрдпклиенттранспортсеттингс:: Гатевайусерселектедкредссаурце

Задает или получает указанный пользователем источник учетных данных шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Значение свойства

Переменная **ulong** , указывающая метод проверки подлинности шлюза удаленных рабочих столов. Этот параметр может принимать одно из указанных ниже значений.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**Таймер TSC \_ \_ \_ \_ Усерпасс режима учетных в прокси-сервере** (0 (0x0))


</dt> <dd>

Используйте пароль (NTLM) в качестве метода проверки подлинности для шлюза удаленных рабочих столов.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**Таймер TSC \_ \_ \_ \_ Смарт-прокси режим учетных записи** (1 (0x1))


</dt> <dd>

Используйте смарт-карту в качестве метода проверки подлинности для шлюза удаленных рабочих столов.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**Таймер TSC \_ Режим учетных и прокси-серверов \_ \_ \_** (4 (0x4))


</dt> <dd>

Используйте любой метод проверки подлинности для шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





