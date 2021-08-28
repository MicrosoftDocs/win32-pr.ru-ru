---
title: Метод Истранспортенаблед класса Win32_TSGatewayServerSettings
description: Определяет, включен ли указанный транспорт.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Истранспортенаблед
- Службы удаленных рабочих столов метода Истранспортенаблед, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Истранспортенаблед
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7960748228e11f3749cd86daa2a323ca32ab9b05e1c17f98261ad4ae62b0fc9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515084"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Истранспортенаблед \_ класса Win32 тсгатевайсерверсеттингс

Определяет, включен ли указанный транспорт.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
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

*Включено* \[ заполняет\]
</dt> <dd>

**Логическое** значение, указывающее, включен ли транспорт.

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

 

 





