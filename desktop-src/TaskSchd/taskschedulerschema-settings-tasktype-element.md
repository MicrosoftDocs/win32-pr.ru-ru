---
title: Элемент Settings (taskType)
description: Задает параметры, которые планировщик задач использует для выполнения задачи.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Элемент Settings планировщик задач
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415232"
---
# <a name="settings-tasktype-element"></a>Элемент Settings (taskType)

Задает параметры, которые планировщик задач использует для выполнения задачи.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

Элемент **Settings** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Указывает задачу, которая выполняется службой планировщик задач.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                          | Тип                                                                                              | Описание                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**алловхардтерминате**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | Логическое                                                                                           | Указывает, что задачу можно завершить с помощью Терминатепроцесс.<br/>                                         |
| [**алловстартондеманд**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | Логическое                                                                                           | Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.<br/>                  |
| [**делетикспиредтаскафтер**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | длительность                                                                                          | Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.<br/> |
| [**дисалловстартифонбаттериес**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | Логическое                                                                                           | Указывает, что задача не будет запущена, если компьютер работает от батарей.<br/>                      |
| [**Активировано**](taskschedulerschema-enabled-settingstype-element.md)                                              | Логическое                                                                                           | Указывает, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.<br/>             |
| [**ексекутионтимелимит**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | длительность                                                                                          | Количество времени, отведенное на выполнение задачи.<br/>                                                              |
| [**Служеб**](taskschedulerschema-hidden-settingstype-element.md)                                                | Логическое                                                                                           | Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию.<br/>                                         |
| [**идлесеттингс**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md)                      | Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.<br/>                    |
| [**маинтенанцесеттингс**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Указывает, как планировщик задач выполняет задачи во время автоматического обслуживания.<br/>                             |
| [**мултиплеинстанцесполици**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**мултиплеинстанцесполицитипе**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**приорититипе**](taskschedulerschema-prioritytype-simpletype.md)                               | Задает уровень приоритета для задачи.<br/>                                                                |
| [**рестартонфаилуре**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**рестарттипе**](taskschedulerschema-restarttype-complextype.md)                                | Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.<br/>      |
| [**рунонлифидле**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | Логическое                                                                                           | Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.<br/>                                |
| [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | Логическое                                                                                           | Указывает, что планировщик задач будет выполнять задачу только при доступности сети.<br/>                     |
| [**стартвхенаваилабле**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | Логическое                                                                                           | Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.<br/>     |
| [**Стопифгоингонбаттериес (Сеттингстипе)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | Логическое                                                                                           | Указывает, что задача будет остановлена при переходе компьютера на питание.<br/>                          |
| [**Независимо**](taskschedulerschema-volatile-element.md)                                                         | Логическое                                                                                           | Указывает, будет ли задача автоматически отключена планировщик задач при запуске Windows.<br/>                     |
| [**Вакеторун (Сеттингстипе)**](taskschedulerschema-waketorun-settingstype-element.md)                           | Логическое                                                                                           | Указывает, что планировщик задач будет выводить компьютер из спящего режима во время выполнения задачи.<br/>                     |



## <a name="remarks"></a>Комментарии

Можно выбрать один или несколько дочерних элементов, указанных выше.

Для разработки на C++ сведения о регистрации задачи указываются с помощью [**Свойства Settings объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Для разработки сценариев сведения о регистрации задачи указываются с помощью свойства [**таскдефинитион. Settings**](taskdefinition-settings.md) .

## <a name="examples"></a>Примеры

В следующем примере кода XML определяется элемент Settings, позволяющий жестко завершить задачу.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Дополнительные сведения и полный пример XML для настройки параметров задачи см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





