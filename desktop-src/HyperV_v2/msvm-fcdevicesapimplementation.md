---
description: Msvm_FcDeviceSAPImplementation класс — представляет связь между точкой доступа службы и логическим устройством, которое ее реализует.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Класс Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9aafe3bd029960a0b371c3a3d5ab54b66ad4849210189ab2946df2854656c500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523464"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>\_Класс мсвм фкдевицесапимплементатион

Представляет связь между точкой доступа службы и логическим устройством, которое ее реализует. Кратность этой ассоциации — «многие ко многим». Точка доступа к службе (SAP) может предоставляться несколькими логическими устройствами, работающими совместно. Любое устройство может предоставлять более одного SAP. Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа. При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP. Эти отдельные экземпляры будут иметь связи с уникальными реализациями.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ фкдевицесапимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ фкдевицесапимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фкпорт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на класс, производный от **CIM \_ фкпорт** , который представляет логическое устройство.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ фцендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий SAP, использующий **предшествующую задачу**.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

