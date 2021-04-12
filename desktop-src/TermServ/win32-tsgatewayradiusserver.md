---
title: Класс Win32_TSGatewayRADIUSServer
description: Описывает сервер протокол RADIUS (RADIUS) с набором политик авторизации подключений службы удаленных рабочих столов (RD \ 160; CAP).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayRADIUSServer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490278"
---
# <a name="win32_tsgatewayradiusserver-class"></a>\_Класс Win32 тсгатевайрадиуссервер

Описывает сервер протокол RADIUS (RADIUS) с набором политик авторизации подключений (RD CAP) службы удаленных рабочих столов.

RADIUS — это стандартный промышленный протокол, используемый для передачи данных проверки подлинности, авторизации и конфигурации между компьютером сервера и сервером проверки подлинности, который называется сервером RADIUS, с базой данных, в которой хранятся сведения о пользователях. Дополнительные сведения см. в разделе [протокол RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайрадиуссервер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайрадиуссервер** содержит следующие методы.



| Метод                                                                 | Описание                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Включить**](win32-tsgatewayradiusserver-add.md)                         | Добавляет новый сервер RADIUS.<br/>                                         |
| [**Вниз**](movedown-win32-tsgatewayradiusserver.md)               | Перемещает этот сервер RADIUS на одну точку вниз в порядке приоритета.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Перемещает этот сервер RADIUS на одну точку вверх в порядке приоритета.<br/>   |
| [**Отменит**](win32-tsgatewayradiusserver-remove.md)                   | Удаляет текущий сервер RADIUS.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Задает свойство **Name** для этого сервера RADIUS.<br/>                |
| [**сетшаредсекрет**](setsharedsecret-win32-tsgatewayradiusserver.md) | Задает свойство **SharedSecret** для этого сервера RADIUS.<br/>        |
| [**Обновляют**](update-win32-tsgatewayradiusserver.md)                   | Обновляет текущий сервер RADIUS.<br/>                                |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайрадиуссервер** имеет следующие свойства.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя сервера RADIUS. Это свойство можно изменить с помощью метода [**SetName**](setname-win32-tsgatewayradiusserver.md) .

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приоритет сервера RADIUS. Сервер шлюза удаленных рабочих столов выполняет поиск политик авторизации подключений удаленных рабочих столов на серверах RADIUS в зависимости от приоритета. Это свойство можно изменить с помощью методов [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**вниз**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)и [**Remove**](win32-tsgatewayradiusserver-remove.md) .

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий секрет для сервера RADIUS. Это свойство можно изменить с помощью метода [**сетшаредсекрет**](setsharedsecret-win32-tsgatewayradiusserver.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для использования этого класса необходимо быть членом группы администраторов.

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
</dt> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

