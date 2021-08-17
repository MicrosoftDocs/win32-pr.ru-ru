---
title: Класс Win32_SessionDirectorySession
description: Предоставляет свойства для просмотра свойств сеанса подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectorySession службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectorySession, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a7d883d3b356713f2f9c3d2b1f9de76676e845020b211ee8a600604a674c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848198"
---
# <a name="win32_sessiondirectorysession-class"></a>\_Класс Win32 сессиондиректорисессион

Предоставляет свойства для просмотра свойств сеанса подключение к удаленному рабочему столу Broker (RDCB).

> [!Note]  
> в Windows Server 2008 R2 имя посредника сеансов служб терминалов изменено на RDCB. Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.

 

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессиондиректорисессион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ сессиондиректорисессион** имеет следующие свойства.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приложение запущено в этом сеансе. Это то же самое, что и свойство **стартпрограм** объекта [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md).

</dd> <dt>

**Clientareawidth**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Глубина цвета сеанса, измеряемая в битах на пиксель.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания сеанса. Это значение не сбрасывается при отключении и повторном подключении сеанса.

</dd> <dt>

**дисконнекттиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время отключения сеанса (если применимо).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доменное имя пользователя, вошедшего в этот сеанс.

</dd> <dt>

**ресолутионхеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Высота сеанса (в пикселях) для данного сеанса.

</dd> <dt>

**ресолутионвидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ширина сеанса (в пикселях) для этого сеанса.

</dd> <dt>

**серверипаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

IP-адрес сервера RDCB для этого сеанса.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя сервера RDCB для этого сеанса.

</dd> <dt>

**SessionID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Идентификатор сеанса для этого сеанса.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние этого сеанса.

<dt>

0
</dt> <dd>

Сеанс активен.

</dd> <dt>

1
</dt> <dd>

Сеанс отключен.

</dd> </dl>

</dd> <dt>

**тспротокол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Протокол для этого сеанса.

<dt>

0
</dt> <dd>

Этот сеанс работает на физической консоли.

</dd> <dt>

1
</dt> <dd>

Для этого сеанса используется собственный протокол стороннего производителя.

</dd> <dt>

2
</dt> <dd>

Для этого сеанса используется протокол удаленного рабочего стола (RDP).

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя пользователя, выполнившего вход в этот сеанс.

</dd> </dl>

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сессиондиректориклустер Win32**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_Сессиондиректорисервер Win32**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

