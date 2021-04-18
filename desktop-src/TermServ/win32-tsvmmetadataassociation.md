---
title: Класс Win32_TSVmMetadataAssociation
description: Представляет связь между удаленный рабочий стол виртуальной машиной и ее свойствами метаданных.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVmMetadataAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVmMetadataAssociation, описание
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672480"
---
# <a name="win32_tsvmmetadataassociation-class"></a>\_Класс Win32 тсвмметадатаассоЦиатион

Представляет связь между удаленный рабочий стол виртуальной машиной и ее свойствами метаданных.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсвмметадатаассоЦиатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсвмметадатаассоЦиатион** имеет следующие свойства.

<dl> <dt>

**метадатаитем**
</dt> <dd> <dl> <dt>

Тип данных: **[ **Win32 \_ тсвмметадатаитем**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Экземпляр класса [**Win32 \_ тсвмметадатаитем**](win32-tsvmmetadataitem.md) , который представляет метаданные для виртуальной машины.

</dd> <dt>

**тсвм**
</dt> <dd> <dl> <dt>

Тип данных: **[ **Win32 \_ тсвм**](win32-tsvm.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Экземпляр класса [**Win32 \_ тсвм**](win32-tsvm.md) , представляющий виртуальную машину.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ терминалсервицес<br/>                                                   |
| MOF<br/>                      | <dl> <dt>Тсвмхост. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

