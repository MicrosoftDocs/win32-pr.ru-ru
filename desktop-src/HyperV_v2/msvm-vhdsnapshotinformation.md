---
description: Предоставляет сведения о моментальном снимке в файле набора виртуальных жестких дисков.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Класс Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898054"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>\_Класс мсвм вхдснапшотинформатион

Предоставляет сведения о моментальном снимке в файле набора виртуальных жестких дисков

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ вхдснапшотинформатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ вхдснапшотинформатион** имеет следующие свойства.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания моментального снимка.

</dd> <dt>

**Равно**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к файлу набора виртуальных жестких дисков.

</dd> <dt>

**парентпасслист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список путей к файлам, представляющих все файлы, от которых зависит этот моментальный снимок. Это поле будет пустым, если не запрашивается специально. Первая запись — это непосредственный родительский элемент файла с последней записью корня.

</dd> <dt>

**ресилиентчанжетраккингид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор отказоустойчивого отслеживания изменений (при наличии), связанный с этим моментальным снимком.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID, который однозначно определяет этот моментальный снимок в файле набора виртуальных жестких дисков.

</dd> <dt>

**снапшотпас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к файлу, представленному этим снимком. Это поле может быть пустым, если с этим моментальным снимком не связан ни один файл.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




