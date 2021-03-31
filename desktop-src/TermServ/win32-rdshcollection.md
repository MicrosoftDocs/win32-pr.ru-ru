---
title: Класс Win32_RDSHCollection
description: Управляет коллекцией узлов сеансов удаленный рабочий стол.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDSHCollection службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDSHCollection, описание
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490971"
---
# <a name="win32_rdshcollection-class"></a>\_Класс Win32 рдшколлектион

Управляет коллекцией узлов сеансов удаленный рабочий стол.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдшколлектион** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдшколлектион** содержит следующие методы.



| Метод                                                                      | Описание                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshcollection.md)           | Извлекает значение целочисленного свойства объекта **\_ рдшколлектион Win32** .<br/>                                                                                                                  |
| [**жетстрингпроперти**](getstringproperty-win32-rdshcollection.md)         | Извлекает значение свойства строки объекта **Win32 \_ рдшколлектион** .<br/>                                                                                                                    |
| [**кэйвалуекомпареандсет**](win32-rdshcollection-keyvaluecompareandset.md) | Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение. Если ключ не существует, метод вставит ключ в коллекцию.<br/> |
| [**кэйвалуеделете**](win32-rdshcollection-keyvaluedelete.md)               | Удаляет из коллекции указанный ключ (и связанное значение).<br/>                                                                                                                       |
| [**кэйвалуежет**](win32-rdshcollection-keyvalueget.md)                     | Извлекает значение, связанное с указанным ключом в коллекции.<br/>                                                                                                                    |
| [**SetInt32Property**](setint32property-win32-rdshcollection.md)           | Обновляет значение целочисленного свойства объекта **Win32 \_ рдшколлектион** .<br/>                                                                                                                    |
| [**сетстрингпроперти**](setstringproperty-win32-rdshcollection.md)         | Обновляет значение свойства строки объекта **Win32 \_ рдшколлектион** .<br/>                                                                                                                      |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдшколлектион** имеет следующие свойства.

<dl> <dt>

**Псевдоним**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает псевдоним коллекции.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает и задает описание коллекции.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имя коллекции.

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**Windows server 2012 R2 и Windows server 2012:** Это свойство недоступно до Windows Server 2016.

Тип коллекции.

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Обычный** (0)


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

Зарезервировано

</dd> <dt>



 (3)


</dt> <dd>

Зарезервировано

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**Мануалперсонал** (4)


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Автопользователь** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик служб удаленный рабочий стол Management Services](rdms-api-reference.md)
</dt> </dl>

 

