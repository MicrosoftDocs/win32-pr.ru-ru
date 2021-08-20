---
title: Класс Win32_SessionDirectoryServer
description: Предоставляет свойства для просмотра свойств сервера подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryServer, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702b56a9cf8aee2ab38ad9d6b3a0f2d270b2128ea46934cc1beb720c77400d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127074"
---
# <a name="win32_sessiondirectoryserver-class"></a>\_Класс Win32 сессиондиректорисервер

Предоставляет свойства для просмотра свойств сервера подключение к удаленному рабочему столу Broker (RDCB).

> [!Note]  
> в Windows Server 2008 R2 имя посредника сеансов служб терминалов изменено на RDCB. Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.

 

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессиондиректорисервер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ сессиондиректорисервер** имеет следующие свойства.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя фермы, содержащей сервер.

</dd> <dt>

**лоадиндикатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный номер, представляющий нагрузку на сервер узла сеансов удаленных рабочих столов при использовании алгоритма балансировки нагрузки по умолчанию. Значение свойства *лоадиндикатор* основано на количестве сеансов, количестве ожидающих запросов на перенаправление и значении веса сервера.

</dd> <dt>

**нумберофсессионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число сеансов на сервере RDCB.

</dd> <dt>

**нумпендредир**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число ожидающих запросов на перенаправление.

</dd> <dt>

**серверипаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

IP-адрес сервера RDCB. Если сервер настроен для адресов IPv4 и IPv6, он будет содержать IPv4-адрес.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя сервера RDCB.

</dd> <dt>

**сервервеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение веса сервера, используемое при балансировке нагрузки.

</dd> <dt>

**синглесессионмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметр режима одиночного сеанса RDCB сервера.

<dt>

0
</dt> <dd>

Ферма не находится в режиме одиночного сеанса.

</dd> <dt>

1
</dt> <dd>

Ферма в находится в режиме одиночного сеанса.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Сессиондиректориклустер Win32**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_Сессиондиректорисессион Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

