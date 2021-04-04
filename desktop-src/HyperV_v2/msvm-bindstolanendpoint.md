---
description: Эта Ассоциация устанавливает точку доступа к службе (SAP) в качестве запрашивающей службы протокола из конечной точки протокола.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Класс Msvm_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999334"
---
# <a name="msvm_bindstolanendpoint-class"></a>\_Класс мсвм биндстоланендпоинт

Эта Ассоциация устанавливает точку доступа к службе (SAP) в качестве запрашивающей службы протокола из конечной точки протокола. Как правило, эта ассоциация выполняется между SAPs и конечными точками в одной системе. Так как конечная точка протокола является разновидностью SAP, эту привязку можно использовать для установки слоев двух протоколов с верхним уровнем, представленным **зависимым** и нижним слоями, представленными **предшествующей** задачей.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ биндстоланендпоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ биндстоланендпоинт** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на класс [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий порт коммутатора. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ вланендпоинт**](msvm-vlanendpoint.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на [**мсвм \_ вланендпоинт**](msvm-vlanendpoint.md) , связанный с портом коммутатора. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**фраметипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает метод кадрирования для SAP или конечной точки верхнего уровня, привязанной к конечной точке локальной сети. Это свойство наследуется от **CIM \_ биндстоланендпоинт** и всегда имеет значение **null**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

