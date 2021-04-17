---
title: Метод вниз класса Win32_TSGatewayRADIUSServer
description: Перемещает этот протокол RADIUS сервер (RADIUS) на одну точку вниз в порядке приоритета.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода вниз
- Службы удаленных рабочих столов метода вниз, класс Win32_TSGatewayRADIUSServer
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов, метод вниз
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534085"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>Метод вниз \_ класса Win32 тсгатевайрадиуссервер

Перемещает этот протокол RADIUS сервер (RADIUS) на одну точку вниз в порядке приоритета. Этот метод увеличивает свойство **Priority** текущего сервера RADIUS и уменьшает свойство **Priority** сервера RADIUS, которое следует за текущим сервером RADIUS.

## <a name="syntax"></a>Синтаксис


```mof
uint32 MoveDown();
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

 

