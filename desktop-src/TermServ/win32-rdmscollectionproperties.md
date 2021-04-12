---
title: Класс Win32_RDMSCollectionProperties
description: Управляет свойствами коллекции виртуальных рабочих столов.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSCollectionProperties службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSCollectionProperties, описание
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415324"
---
# <a name="win32_rdmscollectionproperties-class"></a>\_Класс Win32 рдмсколлектионпропертиес

Управляет свойствами коллекции виртуальных рабочих столов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсколлектионпропертиес** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](/windows)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсколлектионпропертиес** содержит следующие методы.



| Метод                                                                                        | Описание                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**жетпровисионингпропертиес**](getprovisioningproperties-win32-rdmscollectionproperties.md) | Извлекает свойства подготовки коллекции виртуальных рабочих столов.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмсколлектионпропертиес** имеет следующие свойства.

<dl> <dt>

**Псевдоним**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает псевдоним коллекции.

</dd> <dt>

**референцевиртуалдесктопадаптерс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имена виртуальных сетевых адаптеров главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопарчитектуре**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает архитектуру процессора для главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает идентификатор GUID главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктофост**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имя главного сервера для главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопмачиненаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имя компьютера для главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имя главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопосверсион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает версию ОС главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопрамсиземб**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает объем памяти для главной виртуальной машины.

</dd> <dt>

**референцевиртуалдесктопремотефкс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает значение, указывающее, включено ли RemoteFX для главной виртуальной машины. **Значение true** , если RemoteFX включен. в противном случае — **значение false**. Значение этого свойства по умолчанию равно **false**.

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

 

