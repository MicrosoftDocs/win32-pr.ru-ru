---
title: Класс Win32_SessionDirectoryCluster
description: Предоставляет свойства для просмотра свойств фермы в подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryCluster службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryCluster, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490095"
---
# <a name="win32_sessiondirectorycluster-class"></a>\_Класс Win32 сессиондиректориклустер

Предоставляет свойства для просмотра свойств фермы в подключение к удаленному рабочему столу Broker (RDCB).

> [!Note]  
> В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB. Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.

 

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессиондиректориклустер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессиондиректориклустер** имеет следующие свойства.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя фермы в RDCB.

</dd> <dt>

**нумберофсерверс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество серверов в ферме в RDCB.

</dd> <dt>

**синглесессионмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Односеансовый режим фермы в RDCB.

<dt>

0
</dt> <dd>

Ферма в RDCB не находится в режиме одиночного сеанса.

</dd> <dt>

1
</dt> <dd>

Ферма в RDCB находится в режиме одиночного сеанса.

</dd> </dl>

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

[**\_Сессиондиректорисервер Win32**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**\_Сессиондиректорисессион Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

