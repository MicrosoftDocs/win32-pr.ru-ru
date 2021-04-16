---
title: Метод Жетипандпорт класса Win32_TSGatewayServerSettings
description: Получает IP-адрес прослушивания и номер порта для указанного транспорта.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетипандпорт
- Службы удаленных рабочих столов метода Жетипандпорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетипандпорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340460"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Жетипандпорт \_ класса Win32 тсгатевайсерверсеттингс

Получает IP-адрес прослушивания и номер порта для указанного транспорта.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
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

*IP-адрес* \[ заполняет\]
</dt> <dd>

Строка, которая получает IP-адрес прослушивания в виде октета (например, "192.168.1.1").

</dd> <dt>

*Порт* \[ заполняет\]
</dt> <dd>

Указывает номер прослушивающего порта.

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

 

 





