---
description: '\_Ассоциация МЕДИАПРЕСЕНТ CIM описывает связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.'
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: Класс CIM_MediaPresent (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb23d535c2bb189292281464e35897c5a877d467aac595ab18b3ef4f91d5e6e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507054"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a>Класс CIM_MediaPresent (поставщики WMI CIMWin32)

Ассоциация **\_ медиапресент CIM** описывает связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ медиапресент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ медиапресент** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ медиаакцессдевице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Медиаакцессдевице CIM**](cim-mediaaccessdevice.md) , описывающий устройство доступа к носителю.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сторажеекстент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Сторажеекстент CIM**](cim-storageextent.md) , описывающий экстент хранения, к которому осуществляется доступ с помощью устройства доступа к носителю.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ медиапресент** является производным от [**\_ зависимости CIM**](cim-dependency.md).

Инструментарий WMI не реализует этот класс. Классы, производные от **CIM \_ медиапресент**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

