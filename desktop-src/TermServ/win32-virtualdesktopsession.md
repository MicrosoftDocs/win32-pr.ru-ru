---
title: Класс Win32_VirtualDesktopSession
description: Управляет сеансом виртуального рабочего стола.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Класс Win32_VirtualDesktopSession службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_VirtualDesktopSession, описание
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489342"
---
# <a name="win32_virtualdesktopsession-class"></a>\_Класс Win32 виртуалдесктопсессион

Управляет сеансом виртуального рабочего стола.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ виртуалдесктопсессион** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ виртуалдесктопсессион** содержит следующие методы.



| Метод                                                         | Описание                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Отключение**](disconnect-win32-virtualdesktopsession.md)   | Отключает сеанс виртуального рабочего стола.<br/>                        |
| [**Выполнен**](logoff-win32-virtualdesktopsession.md)           | Выполнит выход пользователя из сеанса виртуального рабочего стола.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Отправка сообщения пользователю через сеанс виртуального рабочего стола.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ виртуалдесктопсессион** имеет следующие свойства.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает имя клиентского компьютера, подключенного к сеансу.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает имя коллекции виртуальных рабочих столов, в которой размещена виртуальная машина.

</dd> <dt>

**коннектстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает состояние соединения с сеансом.

</dd> <dt>

**Имя_домена**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает доменное имя пользователя.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает идентификатор сеанса виртуального рабочего стола.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает имя учетной записи пользователя, назначенной сеансу.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает имя сервера узла виртуализации удаленный рабочий стол, на котором размещена виртуальная машина.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает имя виртуальной машины, назначенной сеансу.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик служб удаленный рабочий стол Management Services](rdms-api-reference.md)
</dt> </dl>

 

