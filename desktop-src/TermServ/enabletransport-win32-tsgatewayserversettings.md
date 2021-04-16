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
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672920"
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

 

 





