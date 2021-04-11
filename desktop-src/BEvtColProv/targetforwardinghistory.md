---
description: Журнал последних изменений пересылаемых данных для конечного компьютера.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Класс Таржетфорвардингхистори
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142934"
---
# <a name="targetforwardinghistory-class"></a>Класс Таржетфорвардингхистори

Журнал последних изменений пересылаемых данных для конечного компьютера.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Члены

Класс **таржетфорвардингхистори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **таржетфорвардингхистори** имеет следующие свойства.

<dl> <dt>

**коллекторендпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Сведения о конечной точке сервера сборщика. Это свойство имеет формат "строка *узла*:*порт* ".

</dd> <dt>

**Компьютер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя компьютера конечного компьютера.

</dd> <dt>

**коннектедсинце**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Отметка времени, указывающая, когда было установлено соединение для пересылаемых данных.

</dd> <dt>

**Назначение**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Назначение пересылаемых данных, например имя файла.

</dd> <dt>

**дестинатионпаттерн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Формат, используемый для создания назначения для пересылаемых данных.

</dd> <dt>

**дисконнектедсинце**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Отметка времени, указывающая, когда соединение было разорвано.

</dd> <dt>

**Ошибка**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Сообщение об ошибке, описывающее обнаруженную ошибку. Если ошибка не обнаружена, это свойство пусто.

</dd> <dt>

**форвардертипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Тип файла, который содержит данные пересылки, такие как ETL.

</dd> <dt>

**таржетендпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Сведения о конечной точке конечного компьютера в удобном для человека формате. Это свойство имеет формат "строка *узла*:*порт* ". Например, "127.0.0.1:50000".

</dd> <dt>

**таржетгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**Идентификатор GUID** SMBIOS целевого компьютера.

</dd> <dt>

**таржетмак**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

MAC-адрес конечного компьютера.

</dd> <dt>

**вмидатетиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Метка времени записи изменения состояния.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор<br/>                                              |
| MOF<br/>                      | <dl> <dt>Бутевентколлекторвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик WMI сборщика событий загрузки](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

