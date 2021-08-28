---
description: '\_Ассоциация ФРОМДИРЕКТОРИСПЕЦИФИКАТИОН CIM определяет исходный каталог для действия с файлом.'
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: Класс CIM_FromDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bcb08f58e744e9926a3c4734ac1b8ad4fb75e3288b96ae0c0a7622c5e4109b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320914"
---
# <a name="cim_fromdirectoryspecification-class"></a>\_Класс CIM фромдиректориспеЦификатион

Ассоциация **\_ фромдиректориспеЦификатион CIM** определяет исходный каталог для действия с файлом. При использовании этой ассоциации предполагается, что исходный каталог уже существует. Эта ассоциация не может существовать с Ассоциацией [**CIM \_ фромдиректоряктион**](cim-fromdirectoryaction.md) ; действие файла может содержать только один исходный каталог.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ фромдиректориспеЦификатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ фромдиректориспеЦификатион** имеет следующие свойства.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ филеактион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Ссылка на имя файла.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ директориспеЦификатион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Ссылка на исходный каталог.

</dd> </dl>

## <a name="remarks"></a>Remarks

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

