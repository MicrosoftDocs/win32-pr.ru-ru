---
description: Известные места назначения, содержащие собранные данные. Доступно, только если сборщик работает с включенным журналом состояния.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Класс Таржетфорвардингдестинатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495849"
---
# <a name="targetforwardingdestination-class"></a>Класс Таржетфорвардингдестинатион

Известные места назначения, содержащие собранные данные. Доступно, только если сборщик работает с включенным журналом состояния.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

Класс **таржетфорвардингдестинатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **таржетфорвардингдестинатион** имеет следующие свойства.

<dl> <dt>

**коллекторендпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Узел: сведения о порте конечной точки на стороне сборщика.

</dd> <dt>

**Компьютер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя целевого компьютера, определенное сборщиком в соответствии с его конфигурацией.

</dd> <dt>

**коннектедсинце**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Метка времени установления соединения.

</dd> <dt>

**Назначение**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Назначение данных. Это значение зависит от типа сервера пересылки. Может быть именем файла или какой-либо другой идентификацией.

</dd> <dt>

**дестинатионпаттерн**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Шаблон, используемый для создания назначения данных. Это значение зависит от типа и конфигурации сервера пересылки. Для фиксированного назначения значение будет таким же, как и у самого места назначения. Для назначения с поворотом файлов будут содержаться символы шаблона, которые будут заменены фактическим индексом в назначении.

</dd> <dt>

**дисконнектедсинце**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Метка времени отклонения соединения.

</dd> <dt>

**Ошибка**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Сообщение об ошибке при обнаружении ошибки. В противном случае будет пустым.

</dd> <dt>

**форвардертипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Тип сервера пересылки (например, "ETL").

</dd> <dt>

**таржетендпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Сведения о конечной точке конечного компьютера в удобном для человека формате. Это свойство имеет формат "строка *узла*:*порт* ". Например, "127.0.0.1:50000".

</dd> <dt>

**таржетгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

GUID SMBIOS целевого компьютера (если он известен).

</dd> <dt>

**таржетмак**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

MAC-адрес целевого компьютера (если известен).

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



 

