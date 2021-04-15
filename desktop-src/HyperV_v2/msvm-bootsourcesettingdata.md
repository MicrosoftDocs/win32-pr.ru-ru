---
description: Представляет параметры для задания источника загрузки виртуальной машины.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Класс Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682936"
---
# <a name="msvm_bootsourcesettingdata-class"></a>\_Класс мсвм бутсаурцесеттингдата

Представляет параметры для задания источника загрузки виртуальной машины. Этот класс является производным [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ бутсаурцесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ бутсаурцесеттингдата** имеет следующие свойства.

<dl> <dt>

**бутсаурцедескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание источника загрузки, предоставленное встроенным по.

</dd> <dt>

**бутсаурцетипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение перечисления, указывающее тип источника загрузки.

Допустимые значения:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

**Диск** (1)


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

**Сеть** (2)


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

**Файл** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Краткое текстовое описание объекта.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание объекта.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя для этого экземпляра SettingData. Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса. (Примечание. имя не обязательно должно быть уникальным в пределах пространства имен.)

</dd> <dt>

**фирмваредевицепас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Собственный путь, который используется встроенным по для описания устройства.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

В пределах области создания экземпляра пространства имен InstanceID непрозрачно и уникально идентифицирует экземпляр этого класса. Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма: *OrgID*:*LocalId* , где *OrgID* и *LocalID* разделяются двоеточием (:), и там, где *OrgID* необходимо включать уникальное имя, которое принадлежит бизнес-сущности, которая создает или определяет InstanceId или является зарегистрированным идентификатором, назначенным бизнес-сущности в известном Глобальном центре сертификации. (Это требование похоже на объект *SchemaName* \_ . Структура *className* имен классов схемы.) Кроме того, чтобы обеспечить уникальность, *OrgID* не должен содержать двоеточия (:). При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между *OrgID* и *LocalId*. *LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов. Если указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра. Для экземпляров, определяемых DMTF, необходимо использовать "предпочтительный" алгоритм с *OrgID* , для которого задано значение CIM.

</dd> <dt>

**оптионалдата**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Индексировано")
</dt> </dl>

Необязательные данные, предоставляемые встроенным по.

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**осерлокатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Другие сведения о расположении (если таковые имеются), используемые встроенным по для дальнейшей уникальной идентификации источника загрузки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

