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
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415024"
---
# <a name="win32_sessiondirectorysession-class"></a>\_Класс Win32 сессиондиректорисессион

Предоставляет свойства для просмотра свойств сеанса подключение к удаленному рабочему столу Broker (RDCB).

> [!Note]  
> В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB. Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.

 

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

### <a name="properties"></a>Свойства

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

**креатетиме**
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

**Имя_домена**
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

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

