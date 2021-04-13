---
title: Метод Дисконнектпротокол класса Win32_TSGatewayConnection
description: Отключает все подключения указанного протокола с сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисконнектпротокол
- Службы удаленных рабочих столов метода Дисконнектпротокол, класс Win32_TSGatewayConnection
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов, метод Дисконнектпротокол
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340825"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Метод Дисконнектпротокол \_ класса Win32 тсгатевайконнектион

Отключает все подключения указанного протокола с сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ProtocolName* \[ окне\]
</dt> <dd>

Имя протокола для конкретного соединения. Это можно получить из свойства **ProtocolName** класса **Win32 \_ тсгатевайконнектион** .

<dt>

ЛИЦЕНЗИИ
</dt> <dd>

Протокол для сервера шлюза удаленных рабочих столов.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

