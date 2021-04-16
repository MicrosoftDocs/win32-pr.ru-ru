---
description: Описание виртуальных аспектов виртуальной системы с помощью набора свойств, связанных с виртуализацией. CIM \_ виртуалсистемсеттингдата также используется в качестве класса верхнего уровня конфигураций виртуальных систем.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Класс CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663997"
---
# <a name="cim_virtualsystemsettingdata-class"></a>\_Класс CIM виртуалсистемсеттингдата

Описание виртуальных аспектов виртуальной системы с помощью набора свойств, связанных с виртуализацией. **Модель CIM \_ Виртуалсистемсеттингдата** также используется в качестве класса верхнего уровня конфигураций виртуальных систем.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистемсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ виртуалсистемсеттингдата** имеет следующие свойства.

<dl> <dt>

**аутоматикрековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной системы при сбое программного обеспечения, выполняемого виртуальной системой. Ошибки, устраняемые этим свойством, включают только те, которые обнаруживаются платформой узла, например условие состояния ожидания без перенаправления.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Перезапустить** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Вернуться к моментальному снимку** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**аутоматикшутдовнактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной системы при завершении работы узла.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Выключить (2** )


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Сохранить состояние** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Завершение работы** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**аутоматикстартупактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое в виртуальной системе при запуске узла.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Перезапустить, если ранее активна** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Всегда запуска** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**аутоматикстартупактионделай**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задержка для действия запуска. Это значение является вариантом интервала для типа данных **DateTime** .

</dd> <dt>

**аутоматикстартупактионсекуенценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Порядковый номер активации виртуальной системы при запуске главной системы. Меньшее значение указывает на более раннюю активацию. Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации. Значение "0" указывает, что последовательность зависит от реализации.

</dd> <dt>

**конфигуратиондатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в который хранится информация о конфигурации виртуальной системы. Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**Файл ConfigurationFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь к файлу, где хранятся сведения о конфигурации виртуальной системы. Относительный путь добавляет к значению свойства **конфигуратиондатарут** . Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор конфигурации виртуальной системы.

> [!Note]  
> **ConfigurationID** отличается от **InstanceId** и назначается реализацией для виртуальной системы или конфигурации виртуальной системы. **ConfigurationID** не является ключом, и одно и то же значение может возникать для нескольких экземпляров.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания конфигурации виртуальной системы.

</dd> <dt>

**логдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь к каталогу, в котором хранятся сведения о журнале для виртуальной системы. Относительный путь добавляет к значению свойства **конфигуратиондатарут** . Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий заметки пользователя, связанные с виртуальной системой.

</dd> <dt>

**рековерифиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к файлу, где хранятся сведения о восстановлении виртуальной системы. Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**снапшотдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной системы. Относительный путь добавляет к значению свойства **конфигуратиондатарут** . Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**суспенддатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь к каталогу, в котором хранятся сведения о приостановке, связанные с виртуальной системой. Относительный путь добавляет к значению свойства **конфигуратиондатарут** . Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**свапфиледатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь к каталогу, в котором хранятся файлы подкачки виртуальной системы. Относительный путь добавляет к значению свойства **конфигуратиондатарут** . Формат этого свойства — URI, основанный на RFC 2079.

</dd> <dt>

**виртуалсистемидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное имя системы на платформе виртуализации. **Виртуалсистемидентифиер** не является именем узла, назначенным экземпляру операционной системы, работающему в виртуальной системе, и не является IP-адресом или MAC адресом, назначенным ни одному из сетевых портов.

**Виртуалсистемидентифиер** может содержать правила реализации, такие как простые шаблоны или регулярное выражение, которые могут интерпретироваться реализацией при задании **виртуалсистемидентифиер**.

</dd> <dt>

**виртуалсистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип виртуальной системы.

> [!Note]  
> Если тип виртуальной системы неизвестен, это значение должно быть равно "DMTF: Unknown".

 

Это свойство форматируется с использованием следующего формата Backus Наура Form (ABNF):

VS-Type = DMTF-value/другое-org-value/устаревшее значение; DMTF-value = "DMTF:", "определение-org": "org-VS-Type; другое-org-value = определение-org ":" org-VS-Type;

Значение приведенного выше формата ABNF:

-   *DMTF-value*   значение свойства, определенное DMTF и определяемое в описании этого свойства.
-   *другое-org-value*   — это значение свойства, определяемое бизнес-сущностью, отличной от DMTF, и не определена в описании этого свойства.
-   *устаревшее значение*   . значение свойства, определенное бизнес-сущностью, отличной от DMTF, и не определено в описании этого свойства. Эти значения разрешены, но рекомендуется использовать с течением времени.
-   *Определение-org*   идентификатор для бизнес-сущности, определяющей тип виртуальной системы. Он должен включать в себя авторские права, охраняемые товарные знаки или уникальные имена, принадлежащие бизнес-сущности. Значение должно быть не "DMTF" и не содержать двоеточия.
-   *org-VS — введите*   идентификатор для типа виртуальной системы в определяющей бизнес-сущности. Оно должно быть уникальным в рамках определения-org. org-VS-Type может использовать любой символ, разрешенный для строк CIM, за исключением следующих: u0000-U001F (элементы управления Юникода C0), U0020 (пробел), U007F (элементы управления Юникода C0) или U0080-U009F (элементы управления Юникода C1).
-   Если необходимо структурировать значение по сегментам, сегменты должны быть разделены одним двоеточием.
-   Значения этого свойства должны обрабатываться с учетом регистра. Они предназначены для обработки программным способом, а не для отображаемого имени и должны быть короткими.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




