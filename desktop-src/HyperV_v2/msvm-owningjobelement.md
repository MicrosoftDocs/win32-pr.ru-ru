---
description: Представляет связь между заданием и управляемым элементом, ответственным за создание задания.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Класс Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 144a212a98b6f51b731023b5137b01f1e9d77156bddaaae187ce3f6ff2474efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520984"
---
# <a name="msvm_owningjobelement-class"></a>\_Класс мсвм овнингжобелемент

Представляет связь между заданием и управляемым элементом, ответственным за создание задания.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ овнингжобелемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ овнингжобелемент** имеет следующие свойства.

<dl> <dt>

**овнеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ конкретежоб**](msvm-concretejob.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задание, созданное управляемым элементом.

</dd> <dt>

**овнинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Управляемый элемент, ответственный за создание задания.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

