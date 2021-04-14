---
title: IMsRdpClientTransportSettings2 Гатевайпреауссервераддр, свойство
description: Указывает или получает веб-адрес сервера предварительной проверки подлинности, который используется для функции одноразового пароля шлюза удаленный рабочий стол (OTP).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпреауссервераддр
- Службы удаленных рабочих столов свойства Гатевайпреауссервераддр, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайпреауссервераддр
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415040"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>Свойство IMsRdpClientTransportSettings2:: Гатевайпреауссервераддр

Указывает или получает веб-адрес сервера предварительной проверки подлинности, который используется для функции одноразового пароля шлюза удаленный рабочий стол (OTP).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Значение свойства

Веб-адрес сервера предварительной проверки подлинности; Например, веб-адрес сервера Microsoft Internet Security and Acceleration (ISA) Server. Укажите веб-адрес, используя формат "https://*имя узла*. *Имя_домена*. com/*имя_веб-сайта* или *имя узла* HTTPS://. *Имя_домена*. com/*имя_веб-сайта*.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





