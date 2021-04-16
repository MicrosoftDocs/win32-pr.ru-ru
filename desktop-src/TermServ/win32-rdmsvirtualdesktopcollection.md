---
title: Класс Win32_RDMSVirtualDesktopCollection
description: Создает коллекцию виртуальных рабочих столов и управляет ею.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSVirtualDesktopCollection, описание
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672613"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>\_Класс Win32 рдмсвиртуалдесктопколлектион

Создает коллекцию виртуальных рабочих столов и управляет ею.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсвиртуалдесктопколлектион** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсвиртуалдесктопколлектион** содержит следующие методы.



| Метод                                                                                            | Описание                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддвиртуалдесктоп**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Добавляет виртуальный рабочий стол в коллекцию виртуальных рабочих столов.<br/>                                                                              |
| [**канцелпатч**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Отменяет задание подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Извлекает значение целочисленного свойства из коллекции виртуальных рабочих столов.<br/>                                                               |
| [**жетпатчпропертиес**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.<br/>             |
| [**жетстрингпроперти**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Извлекает значение свойства строки из коллекции виртуальных рабочих столов.<br/>                                                                 |
| [**провисионинженумератежобс**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Перечисляет задания подготовки виртуальных рабочих столов для этой службы.<br/>                                                                       |
| [**провисионингжобканцел**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Отмена задания подготовки виртуальных рабочих столов.<br/>                                                                                          |
| [**провисионингжобексекуте**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Запускает задание подготовки виртуальных рабочих столов.<br/>                                                                                             |
| [**провисионингжобжетрепорт**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.<br/>                                                                |
| [**провисионингпрепжоб**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Создает задание подготовки виртуальных рабочих столов.<br/>                                                                                          |
| [**ремовевиртуалдесктоп**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.<br/>                                                                         |
| [**счедулепатч**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Обновляет значение целочисленного свойства коллекции виртуальных рабочих столов.<br/>                                                                   |
| [**сетстрингпроперти**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Обновляет значение свойства строки коллекции виртуальных рабочих столов.<br/>                                                                     |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмсвиртуалдесктопколлектион** имеет следующие свойства.

<dl> <dt>

**Псевдоним**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает или задает псевдоним коллекции.

</dd> <dt>

**коллектиондескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает или задает описание коллекции.

</dd> <dt>

**иконконтентс**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает или задает массив значений, указывающих значки для коллекции.

</dd> <dt>

**иша**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значения, указывающие, содержит ли коллекция виртуальные машины высокой доступности. **Значение true** , если коллекция содержит виртуальные машины высокой доступности; в противном случае — **значение false**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значение, указывающее, является ли коллекция управляемой. **Значение true** , если коллекция является управляемой; в противном случае — **значение false**.

</dd> <dt>

**исусерадмин**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значения, указывающие, является ли пользователь администратором виртуальной машины. **Значение true** , если пользователь является администратором на виртуальной машине; в противном случае — **значение false**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает имя коллекции.

</dd> <dt>

**роллбаккенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значения, указывающие, была ли виртуальная машина восстановлена с помощью моментального снимка виртуальной машины. **Значение true** , если виртуальная машина была восстановлена с помощью моментального СНИМКА виртуальной машины. в противном случае — **значение false**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает или задает дескриптор безопасности в формате SSDL, который управляет доступом к коллекции.

</dd> <dt>

**шовинпортал**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значения, указывающие, отображается ли коллекция в Веб-доступ служб терминалов (TS Веб-доступ). **Значение true** , чтобы отобразить коллекцию в службах терминалов веб-доступ; в противном случае — **значение false**.

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает или задает значение, указывающее тип сеансов виртуальных машин, размещенных в коллекции.

Это свойство содержит одно из следующих значений:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**Темпвм** (1)


</dt> <dd>

Временные виртуальные машины.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**Мануалперсоналвм** (2)


</dt> <dd>

Виртуальные машины, созданные вручную.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**Аутоперсоналвм** (3)


</dt> <dd>

Автоматически создаваемые виртуальные машины.

</dd> </dl>

</dd> <dt>

**усервхдсеттинг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает или задает параметр виртуального жесткого диска данных пользователя для коллекции.

</dd> <dt>

**вмфармсеттингс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает или задает параметры рабочего стола для виртуальных машин в коллекции.

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

 

