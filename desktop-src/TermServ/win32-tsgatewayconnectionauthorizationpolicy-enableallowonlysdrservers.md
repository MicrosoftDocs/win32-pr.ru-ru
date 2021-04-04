---
title: Метод Енаблеалловонлисдрсерверс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Используется для переключения свойства Алловонлисдрсерверс.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеалловонлисдрсерверс
- Службы удаленных рабочих столов метода Енаблеалловонлисдрсерверс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Енаблеалловонлисдрсерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802092"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Енаблеалловонлисдрсерверс \_ класса Win32 тсгатевайконнектионаусоризатионполици

Используется для переключения свойства **алловонлисдрсерверс** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Алловонлисдрсерверс* \[ окне\]
</dt> <dd>

Если задано значение **true**, подключения будут разрешены только для защиты RDS-серверов перенаправления устройств (SDR). Если задано значение **false**, то подключения будут разрешены более старым СЕРВЕРАм RDS.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | КОРНЕВой \\ CIMV2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TsGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





