---
title: Метод Дисконнектусер класса Win32_TSGatewayConnection (Тсгаусентикатионенгине. h)
description: Отключает все подключения указанного пользователя от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисконнектусер
- Службы удаленных рабочих столов метода Дисконнектусер, класс Win32_TSGatewayConnection
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов, метод Дисконнектусер
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130999"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Метод Дисконнектусер \_ класса Win32 тсгатевайконнектион

Отключает все подключения указанного пользователя от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Имя пользователя в формате * домен * **\\** _имя пользователя_ , подключения которого должны быть отключены.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                             |
| Header<br/>                   | <dl> <dt>Тсгаусентикатионенгине. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

