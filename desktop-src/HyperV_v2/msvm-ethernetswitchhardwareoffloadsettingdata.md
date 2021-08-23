---
description: Представляет параметры разгрузки коммутатора.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Класс Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 751e5f3256da82d2b7cae2da17a8b9dfb54bc5331ebf2679e745bc67c0b4d3b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524551"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a>\_Класс мсвм есернетсвитчхардвареоффлоадсеттингдата

Представляет параметры разгрузки коммутатора.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчхардвареоффлоадсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетсвитчхардвареоффлоадсеттингдата** имеет следующие свойства.

<dl> <dt>

**дефаулткуеуевммкенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Задает параметры ВММК для очереди по умолчанию vSwitch.

</dd> <dt>

**дефаулткуеуевммккуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает количество очередей для очереди по умолчанию.

</dd> <dt>

**дефаулткуеуеврссенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Задает параметры VRss для очереди по умолчанию в vSwitch.

</dd> <dt>

**дефаулткуеуеврссексклудепримарипроцессор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, исключается ли основной ЦП VMQ из таблицы косвенных обращений VRSS/ВММК.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**дефаулткуеуеврссиндепенденсостспреадинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, следует ли всегда выполнять распространение VRSS для очереди по умолчанию независимо от состояния RSS внешней впорт.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**дефаулткуеуеврссминкуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает минимальное число очередей, используемых для VRSS/ВММК.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**дефаулткуеуеврсскуеуесчедулингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, каким способом очереди VRSS/ВММК связаны с разными процессорами узла.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




