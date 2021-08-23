---
title: Метод Енаблетранспорт класса Win32_TSGatewayServerSettings
description: Включает или отключает указанный транспорт.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблетранспорт
- Службы удаленных рабочих столов метода Енаблетранспорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблетранспорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08087c4a28b0867f7457bed597a71c5156ea968fb50f3f2509c8da5ef3057fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059602"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Енаблетранспорт \_ класса Win32 тсгатевайсерверсеттингс

Включает или отключает указанный транспорт.

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*TransportType* \[ окне\]
</dt> <dd>

Указывает тип транспорта. Это должно быть одно из следующих значений.

<dt>

0
</dt> <dd>

Транспорт RPC через HTTP.

</dd> <dt>

1
</dt> <dd>

Транспорт HTTP.

</dd> <dt>

2
</dt> <dd>

Транспорт UDP.

</dd> </dl> </dd> <dt>

*Включить* \[ окне\]
</dt> <dd>

Указывает, включен или отключен транспорт.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





