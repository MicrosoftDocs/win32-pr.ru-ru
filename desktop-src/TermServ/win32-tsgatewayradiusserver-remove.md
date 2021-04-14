---
title: Метод Remove класса Win32_TSGatewayRADIUSServer
description: Удаляет текущий сервер протокол RADIUS (RADIUS).
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Удалить метод службы удаленных рабочих столов
- Удаление метода службы удаленных рабочих столов, Win32_TSGatewayRADIUSServer Interface
- Службы удаленных рабочих столов интерфейса Win32_TSGatewayRADIUSServer, метод Remove
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341105"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a>Метод Remove класса Win32 \_ тсгатевайрадиуссервер

Удаляет текущий сервер протокол RADIUS (RADIUS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Remove();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

[**\_Тсгатевайрадиуссервер Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

