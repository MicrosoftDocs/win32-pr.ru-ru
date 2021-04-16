---
description: Описывает локальную установку WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Класс __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702511"
---
# <a name="__cimomidentification-class"></a>\_\_Класс Цимомидентификатион

Системный класс **\_ \_ Цимомидентификатион** описывает локальную установку WMI. Это одноэлементный класс; Существует только один экземпляр. Класс **\_ \_ Цимомидентификатион** доступен только в **корневых** и корневых пространствах имен **\\ по умолчанию** . Пользователи запрашивают экземпляр для получения сведений об установке WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ Цимомидентификатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ Цимомидентификатион** имеет следующие свойства.

<dl> <dt>

**сетупдатетиме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время установки. Это свойство пусто после установки операционной системы в первый раз.

Если репозиторий WMI был удален, а затем создан снова, это свойство содержит дату и время повторного создания репозитория.

</dd> <dt>

**версионкуррентлируннинг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает версию фактического образа, содержащего службу WMI, которая создала репозиторий модель CIM (CIM). Так как формат репозитория может измениться между версиями WMI, это свойство позволяет будущим обновлениям WMI определить, нужно ли обновить базу данных. Формат будет следующим:

"1.00.183.0000"

Если первая цифра является основной версией, следующие две цифры являются дополнительными версиями, а следующие три цифры — номером сборки. Остальные цифры не используются.

</dd> <dt>

**версионуседтокреатедб**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает версию фактического образа, содержащего службу WMI, которая создала репозиторий CIM. Так как формат репозитория может измениться между версиями WMI, это свойство позволяет будущим обновлениям WMI определить, нужно ли обновить базу данных. Формат будет следующим:

"1.00.183.0000"

Если первая цифра является основной версией, следующие две цифры являются дополнительными версиями, а следующие три цифры — номером сборки. Остальные цифры не используются.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Каталог установки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ Цимомидентификатион** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.

## <a name="examples"></a>Примеры

В следующем образце кода VBScript описывается, как отобразить сведения об идентификации объектной модели CIM и они были взяты из каталога примеров в папке \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ сисмгмт \\ WMI \\ scripting.


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



В следующем образце кода Perl описывается, как отобразить сведения об идентификации объектной модели CIM и они были взяты из каталога примеров в папке \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ сисмгмт \\ WMI \\ scripting.


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Root<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_системкласс**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

