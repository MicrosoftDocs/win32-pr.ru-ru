---
description: Msvm_WiFiDeviceSAPImplementation класс — ассоциация между точкой доступа к службе (SAP) и ее реализацией.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Класс Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 31200fc05e87a15b00463903a21a4e1822df50d9f286162ee75e7bbe4da0daa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980424"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>\_Класс мсвм вифидевицесапимплементатион

Связь между точкой доступа к службе (SAP) и ее реализацией. Кратность этой ассоциации — «многие ко многим». SAP может предоставляться более чем одним логическим устройством, работающим совместно. Любое устройство может предоставлять более одного SAP. Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа. При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP. Эти отдельные экземпляры будут иметь связи с уникальными реализациями.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ вифидевицесапимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ вифидевицесапимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ вифипорт**](msvm-wifiport.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Экземпляр класса [**мсвм \_ вифипорт**](msvm-wifiport.md) , представляющий логическое устройство.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ вифиендпоинт**](msvm-wifiendpoint.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Экземпляр класса [**мсвм \_ вифиендпоинт**](msvm-wifiendpoint.md) , представляющий точку доступа к службе, реализованную с помощью логического устройства.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

