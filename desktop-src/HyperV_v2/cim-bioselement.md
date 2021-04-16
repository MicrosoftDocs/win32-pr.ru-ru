---
description: Представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Класс CIM_BIOSElement (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664688"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>Класс CIM_BIOSElement (Управление Hyper-V)

Представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы ([**CIM \_ ComputerSystem**](cim-computersystem.md)).

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ биоселемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ биоселемент** имеет следующие свойства.

<dl> <dt>

**куррентлангуаже**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ биоселемент**.**Листофлангуажес**")
</dt> </dl>

Выбранный в данный момент язык для BIOS. Эти сведения можно получить из системы System Management BIOS (SMBIOS), используя атрибут текущего языка структуры типа 13 для индексации в список строк, следующий за структурой. Это свойство форматируется с использованием имени языка ISO 639, за которым может следовать имя территории ISO 3166 и метод Encoding.

</dd> <dt>

**листофлангуажес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список устанавливаемых языков для BIOS. Эти сведения можно получить из SMBIOS в списке строк, который следует за структурой типа 13. Для указания устанавливаемых языков BIOS можно использовать имя языка ISO 639. Кроме того, можно указать имя территории ISO 3166 и метод Encoding, следуя названиям языка.

</dd> <dt>

**лоадедендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,6 ")
</dt> </dl>

Конечный адрес памяти, занимаемой BIOS.

</dd> <dt>

**лоадедстартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,5 ")
</dt> </dl>

Начальный адрес памяти, занимаемой BIOS.

</dd> <dt>

**лоадутилитинформатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,7 ")
</dt> </dl>

Строка произвольной формы, описывающая программу BIOS Flash/Load, необходимую для обновления объекта **CIM \_ биоселемент** . В этом свойстве могут быть указаны версия и другие сведения.

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,2 ")
</dt> </dl>

Производитель программного элемента.

</dd> <dt>

**примарибиос**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,9 ")
</dt> </dl>

Значение true, если это основная BIOS компьютерной системы; в противном случае — значение false.

</dd> <dt>

**регистрюрис**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Расположение публикации реестров атрибутов BIOS, к которым соответствует реализация BIOS.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,8 ")
</dt> </dl>

Дата выпуска BIOS.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,3 ")
</dt> </dl>

Версия операции. Версия операции должна быть в одной из следующих форм:

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СОФТВАРИЛЕМЕНТ CIM**](cim-softwareelement.md)
</dt> </dl>

 

