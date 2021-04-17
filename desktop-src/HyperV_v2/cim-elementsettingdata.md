---
description: Представляет связь между управляемым элементом и связанными с ним данными параметров. Эта Ассоциация также описывает, является ли этот параметр стандартным или текущим.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Класс CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663482"
---
# <a name="cim_elementsettingdata-class"></a>\_Класс CIM елементсеттингдата

Представляет связь между управляемым элементом и связанными с ним данными параметров. Эта Ассоциация также описывает, является ли этот параметр стандартным или текущим.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ елементсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ елементсеттингдата** имеет следующие свойства.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, используется ли в данный момент параметр, на который указывает ссылка.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**Является текущим** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**Не является текущим** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли параметр параметром по умолчанию для элемента.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

Значение **по умолчанию** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**Не является значением по умолчанию** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**По подследу**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Флаг, указывающий, когда и как часто следует применять этот параметр.

Например, параметр можно применить к запросу повторной инициализации, сброса и перенастройки. Это может быть постоянный параметр или параметр, используемый только один раз, как указано в флаге. Если это постоянный параметр, параметр применяется каждый раз при повторной инициализации управляемого элемента до тех пор, пока этот флаг не будет сброшен вручную. Однако при использовании одного из них флажок автоматически снимается после применения параметров. Кроме того, если для этого флага задано значение, отличное от 0 (неизвестно), то это имеет приоритет над свойством **SettingData** , для которого задано "default".

Если управляемый элемент является компьютерной системой, а значение этого флага — «далее», то параметр вступит в силу при следующем сбросе системы. И, если этот флаг не изменится, он будет сохранен при последующих сбросах системы. Однако если этот флаг имеет значение "Далее для отдельного использования", этот параметр будет использоваться только один раз, а флаг будет сброшен после этого до 2 (не далее). Таким образом, в приведенном выше примере, если система перезагружается, параметр не будет использоваться при второй перезагрузке.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**Следующий** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**Не далее** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**Следующее для отдельного использования** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Управляемый элемент.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Тип данных: **\_ SettingData CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Данные параметра, связанные с элементом.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

