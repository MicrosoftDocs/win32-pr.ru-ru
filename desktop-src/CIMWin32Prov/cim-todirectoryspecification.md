---
description: '\_Ассоциация ТОДИРЕКТОРИСПЕЦИФИКАТИОН CIM определяет целевой каталог для действия с файлом.'
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Класс CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e079a5012760507adfd9bff6b9716a6828e1f3e9b516ec252895ab8e93e801d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118677390"
---
# <a name="cim_todirectoryspecification-class"></a>\_Класс CIM тодиректориспеЦификатион

Ассоциация **\_ тодиректориспеЦификатион CIM** определяет целевой каталог для действия с файлом. При использовании этой ассоциации предполагается, что целевой каталог уже существует. Эта ассоциация не может существовать с [**Ассоциацией \_ тодиректоряктион CIM**](cim-todirectoryaction.md) , так как действие файла может содержать только один целевой каталог.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ тодиректориспеЦификатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ тодиректориспеЦификатион** имеет следующие свойства.

<dl> <dt>

**дестинатиондиректори**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ директориспеЦификатион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Ссылка на каталог назначения.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ копифилеактион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Ссылка на имя файла.

</dd> </dl>

## <a name="remarks"></a>Remarks

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

