---
description: '\_Ассоциация ТОДИРЕКТОРЯКТИОН CIM определяет целевой каталог для действия с файлом.'
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: Класс CIM_ToDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807937"
---
# <a name="cim_todirectoryaction-class"></a>\_Класс CIM тодиректоряктион

Ассоциация **\_ тодиректоряктион CIM** определяет целевой каталог для действия с файлом. При использовании этой ассоциации предполагается, что целевой каталог был создан предыдущим действием. Эта ассоциация не может существовать с [**Ассоциацией \_ тодиректориспеЦификатион CIM**](cim-todirectoryspecification.md) , так как действие файла может содержать только один целевой каталог.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ тодиректоряктион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ тодиректоряктион** имеет следующие свойства.

<dl> <dt>

**дестинатиондиректори**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ директоряктион**
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

## <a name="remarks"></a>Комментарии

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



 

