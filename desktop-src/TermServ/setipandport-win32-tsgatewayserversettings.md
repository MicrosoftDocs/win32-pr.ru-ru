---
title: Метод Сетипандпорт класса Win32_TSGatewayServerSettings
description: Задает IP-адрес прослушивания и номер порта для указанного транспорта.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетипандпорт
- Службы удаленных рабочих столов метода Сетипандпорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетипандпорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534073"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Сетипандпорт \_ класса Win32 тсгатевайсерверсеттингс

Задает IP-адрес прослушивания и номер порта для указанного транспорта.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*IP-адрес* \[ окне\]
</dt> <dd>

Указывает IP-адрес прослушивания в виде октета (например, "192.168.1.1").

</dd> <dt>

*Порт* \[ окне\]
</dt> <dd>

Указывает номер прослушивающего порта.

</dd> <dt>

*Оверридиксистинг* \[ окне\]
</dt> <dd>

Указывает, переопределять ли существующую привязку IP/Port для HTTP. Этот параметр используется только в том случае, если параметр *TransportType* содержит значение 0 (RPC по HTTP) или 1 (http).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





