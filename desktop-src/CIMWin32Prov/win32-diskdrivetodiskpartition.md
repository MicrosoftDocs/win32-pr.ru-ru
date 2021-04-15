---
description: '\_Класс WMI взаимосвязей Win32 дискдриветодискпартитион связывает диск и раздел, существующий на нем.'
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Класс Win32_DiskDriveToDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655990"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>\_Класс Win32 дискдриветодискпартитион

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ дискдриветодискпартитион** связывает диск и раздел, существующий на нем.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ дискдриветодискпартитион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ дискдриветодискпартитион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ дискдриве**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дискдриве")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства диска, на котором находится секция.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ дискпартитион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дискпартитион")
</dt> </dl>

Ссылка на экземпляр, представляющий раздел диска, расположенный на диске.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ дискдриветодискпартитион** является производным от [**CIM \_ медиапресент**](cim-mediapresent.md).

Сведения об использовании этого класса см. в статьях [Использование PowerShell для сопоставления дисков и разделов](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) и [как можно сопоставить логические диски и физические диски?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) статьи блога.

## <a name="examples"></a>Примеры

Пример [использования PowerShell для сбора сведений о диске, разделе или точке подключения](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell использует **Win32 \_ дискдриветодискпартитион** для получения сведений о локальных дисках и разделах и точках подключения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МЕДИАПРЕСЕНТ CIM**](cim-mediapresent.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Задачи WMI: диски и файловые системы](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

