---
description: Связывает виртуальную машину и данные параметров экспорта.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Класс Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39e096c466dd4accc1a2c87ececd6ce23ba27cb173e6b5fa0d6728852ad59cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811874"
---
# <a name="msvm_systemexportsettingdata-class"></a>\_Класс мсвм системекспортсеттингдата

Связывает виртуальную машину и данные параметров экспорта. Перед вызовом метода [**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ Виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) можно получить экземпляр [**мсвм \_ виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md) , используя эту ассоциацию.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ системекспортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ системекспортсеттингдата** имеет следующие свойства.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, используется ли на данный момент параметр, на который указывает ссылка, в операции элемента или что эта информация неизвестна. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Значение                                                                        | Значение                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Неизвестно<br/>     |
| <dl> <dt>1</dt> </dl> | Текущий<br/>     |
| <dl> <dt>2</dt> </dl> | Не текущий<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли параметр, на который указывает ссылка, параметром по умолчанию для элемента или что эта информация неизвестна. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Значение                                                                        | Значение                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Неизвестно<br/>     |
| <dl> <dt>1</dt> </dl> | По умолчанию<br/>     |
| <dl> <dt>2</dt> </dl> | Не по умолчанию<br/> |



 

</dd> <dt>

**По подследу**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли параметр, на который указывает ссылка, следующим параметром, который должен быть применен. Например, приложение может выполняться при повторной инициализации, сбросе и перенастройке запроса. Это может быть постоянный параметр или параметр, используемый только один раз, как указано в флаге. Если это постоянный параметр, параметр применяется каждый раз при повторной инициализации управляемого элемента до тех пор, пока этот флаг не будет сброшен вручную. Однако при использовании одного из них флажок автоматически снимается после применения параметров. Кроме того, если этот флаг задан (т. е. задано значение, отличное от 0 (неизвестно)), то он имеет приоритет над всеми параметрами, которые могли быть указаны по умолчанию. Например, если управляемый элемент является компьютерной системой, а значение этого флага равно 1 (далее), этот параметр вступит в силу при следующем сбросе системы. И, если этот флаг не изменится, он будет сохранен при последующих сбросах системы. Однако если для этого флага задано значение 3 (для отдельного использования), этот параметр будет использоваться только один раз, а флаг будет сброшен после этого до 2 (не далее). Таким образом, в приведенном выше примере, если система перезагружается, параметр не будет использоваться при второй перезагрузке.

Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Значение                                                                        | Значение                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Неизвестно<br/>                |
| <dl> <dt>1</dt> </dl> | Далее<br/>                |
| <dl> <dt>2</dt> </dl> | Не далее<br/>            |
| <dl> <dt>3</dt> </dl> | Для одного использования<br/> |



 

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ елементсеттингдата. манажеделемент")
</dt> </dl>

Ссылка на виртуальную машину. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ елементсеттингдата. SettingData")
</dt> </dl>

Ссылка на данные настройки экспорта для виртуальной машины. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ системекспортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

