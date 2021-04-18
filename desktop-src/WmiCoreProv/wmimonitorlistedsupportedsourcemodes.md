---
description: Список поддерживаемых режимов исходного кода для видеомонитора в дескрипторе монитора (при наличии).
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Класс Вмимониторлистедсуппортедсаурцемодес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712281"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>Класс Вмимониторлистедсуппортедсаурцемодес

**Вмимониторлистедсуппортедсаурцемодес** перечисляет поддерживаемые режимы источника для видеомонитора в дескрипторе монитора, если таковые имеются. Для мониторов, не имеющих описания, этот список режимов создается на основе типа монитора, как указано в драйвере монитора шины.

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>Члены

Класс **вмимониторлистедсуппортедсаурцемодес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **вмимониторлистедсуппортедсаурцемодес** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> <dt>

**мониторсаурцемодес**
</dt> <dd> <dl> <dt>

Тип данных: массив **видеомодедескриптор**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Перечисляет режимы работы с исходным кодом, представленные экземплярами класса [**видеомодедескриптор**](videomodedescriptor.md) .

</dd> <dt>

**нумофмониторсаурцемодес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число перечисленных поддерживаемых режимов отслеживания источника.

</dd> <dt>

**преферредмониторсаурцемодеиндекс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Индекс основного режима источника монитора.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

 




