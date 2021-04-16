---
description: Представляет параметры, относящиеся к хранению для виртуальной системы.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Класс Msvm_StorageSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651206"
---
# <a name="msvm_storagesettingdata-class"></a>\_Класс мсвм сторажесеттингдата

Представляет параметры, относящиеся к хранению для виртуальной системы.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сторажесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сторажесеттингдата** имеет следующие свойства.

<dl> <dt>

**дисаблеинтерруптбатчинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли отключить пакетную обработку прерываний.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) WMI.

</dd> <dt>

**среадкаунтперчаннел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество потоков на канал хранилища для обработки операций ввода-вывода.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**По умолчанию** (0)


</dt> <dd>

Поведение по умолчанию

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкая** (1)


</dt> <dd>

Малое количество потоков на канал хранилища.

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Средний** (2)


</dt> <dd>

Среднее число потоков на канал хранилища.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (3)


</dt> <dd>

Большое количество потоков на канал хранилища.

</dd> </dl>

</dd> <dt>

**виртуалпроцессорсперчаннел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество процессоров на канал хранилища. Число открываемых каналов определяется (число логических процессоров на узле/**виртуалпроцессорсперчаннел**).

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ системкомпонентсеттингдата**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




