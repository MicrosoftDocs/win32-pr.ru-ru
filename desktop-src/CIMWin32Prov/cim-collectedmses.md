---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM коллектедмсес представляет члены объекта GROUPING, класса коллектионофмсес.'
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: Класс CIM_CollectedMSEs (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496410"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a>Класс CIM_CollectedMSEs (поставщики WMI CIMWin32)

Класс сопоставления **CIM \_ коллектедмсес** представляет члены объекта GROUPING, класса [**коллектионофмсес**](cim-collectionofmses.md) .

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ коллектедмсес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ коллектедмсес** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **cm \_ коллектионофмсес**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на объект группирования или контейнера, представляющий коллекцию.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на элемент коллекции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Инструментарий WMI не реализует этот класс. Дополнительные сведения о классах WMI, производных от **CIM \_ коллектедмсес**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




