---
description: Используется в методе Куеригуестклустеринформатион \_ класса мсвм всссервице для получения сведений о гостевом кластере, частью которого является виртуальная машина.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Класс Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682859"
---
# <a name="msvm_guestclusterinformation-class"></a>\_Класс мсвм гуестклустеринформатион

Используется в методе [**куеригуестклустеринформатион**](msvm-vssservice-queryguestclusterinformation.md) класса [**мсвм \_ всссервице**](msvm-vssservice.md) для получения сведений о гостевом кластере, частью которого является виртуальная машина.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ гуестклустеринформатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ гуестклустеринформатион** имеет следующие свойства.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор отказоустойчивого кластера, частью которого является гостевая операционная система виртуальной машины.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество узлов в кластере, частью которого является гостевая операционная система виртуальной машины.

</dd> <dt>

**исактивеактиве**
</dt> <dd> <dl> <dt>

Тип данных: **логический** массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, который указывает, является ли соответствующий дисковый ресурс в гостевом кластере общим для виртуальных машин в активном и активном режиме.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Тип данных: **логический** массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, является ли соответствующий диск ресурсом кластера в гостевом кластере.

</dd> <dt>

**Подключение к Интернету**
</dt> <dd> <dl> <dt>

Тип данных: **логический** массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, находится ли соответствующий дисковый ресурс в гостевом кластере в сети.

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **логический** массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, является ли соответствующий дисковый ресурс в гостевом кластере курренли владельцем этой виртуальной машины.

</dd> <dt>

**ластресаурцемоветиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число тактов часов при последнем перемещении одного из ресурсов общего диска.

> [!Note]  
> Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**шаредвиртуалхарддискпасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив путей к общим виртуальным жестким дискам, подключенных к виртуальной машине.

</dd> <dt>

**шаредвиртуалхарддискс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив данных параметров выделения ресурсов (РАСД), представляющих общие виртуальные жесткие диски, подключенные к виртуальной машине.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

