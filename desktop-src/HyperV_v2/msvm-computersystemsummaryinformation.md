---
description: Содержит сводку сведений об указанной виртуальной системе компьютера.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Класс Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78ac2b89336a415bedd23e0ca4ecd6589abdefbf75a54900d716c78152d34d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531764"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>\_Класс мсвм компутерсистемсуммаринформатион

Содержит сводку сведений об указанной виртуальной системе компьютера.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ компутерсистемсуммаринформатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ компутерсистемсуммаринформатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) , являющийся экземпляром в нормализованном представлении управляемого ресурса.

> [!Note]
>
> тип данных, обновленный с [**мсвм \_ ComputerSystem**](msvm-computersystem.md) в Windows 10, версия 1703.

 

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ суммаринформатионбасе**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Экземпляр [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющий денормализованное или Статистическое представление управляемого ресурса, представленного [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , на который ссылается свойство Antecedent.

> [!Note]
>
> тип данных, обновленный из [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) в Windows 10, версия 1703.

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЕЛЕМЕНТВИЕВ CIM**](cim-elementview.md)
</dt> </dl>

 

