---
title: Сложный тип Сеттингстипе
description: определяет дочерние элементы и сведения о последовательности для элемента Параметры (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- планировщик задач сложного типа Сеттингстипе
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a48a124230a27a0c23cc9c2a9fa983b6ef3088b8ec22e8ac03fc371caadf0f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356356"
---
# <a name="settingstype-complex-type"></a>Сложный тип Сеттингстипе

определяет дочерние элементы и сведения о последовательности для элемента [**Параметры (taskType)**](taskschedulerschema-settings-tasktype-element.md) .

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                             | Тип                                                                                              | Описание                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**алловхардтерминате**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | Логическое                                                                                           | Указывает, допускает ли служба планировщик задач жесткое завершение задачи.<br/>                                                                                                                                                                                                                             |
| [**алловстартондеманд**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | Логическое                                                                                           | Указывает, что задачу можно запустить с помощью команды Run или контекстного меню. <br/>                                                                                                                                                                                                             |
| [**делетикспиредтаскафтер**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | длительность                                                                                          | Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия. Если для этого элемента не указано значение, то служба планировщик задач не удалит задачу.<br/>                                                                                           |
| [**дисалловстартифонбаттериес**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | Логическое                                                                                           | Указывает, что задача не будет запущена, если компьютер работает от аккумулятора.<br/>                                                                                                                                                                                                                 |
| [**дисалловстартонремотеаппсессион**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | Логическое                                                                                           | Указывает, что задача не должна запускаться, если задача запускается в локально интегрированном сеансе с удаленными приложениями.<br/>                                                                                                                                                                     |
| [**Включен**](taskschedulerschema-enabled-settingstype-element.md)                                                 | Логическое                                                                                           | Указывает, что задача включена. Задачу можно выполнить, только если этот параметр имеет **значение true**.<br/>                                                                                                                                                                                                        |
| [**ексекутионтимелимит**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | длительность                                                                                          | Указывает время, в течение которого может завершиться задача.<br/>                                                                                                                                                                                                                                               |
| [**Служеб**](taskschedulerschema-hidden-settingstype-element.md)                                                   | Логическое                                                                                           | Указывает по умолчанию, что задача не будет отображаться в пользовательском интерфейсе.<br/>                                                                                                                                                                                                                     |
| [**идлесеттингс**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md)                      | Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.<br/>                                                                                                                                                                                                                   |
| [**мултиплеинстанцесполици**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**мултиплеинстанцесполицитипе**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи. <br/>                                                                                                                                                                                                     |
| [**нетворкпрофиленаме**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | строка                                                                                            | Указывает имя сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**. Имя используется в целях показа.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md)                | Указывает параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.<br/> |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                               | [**приорититипе**](taskschedulerschema-prioritytype-simpletype.md)                               | Задает уровень приоритета для задачи.<br/>                                                                                                                                                                                                                                                               |
| [**рестартонфаилуре**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**рестарттипе**](taskschedulerschema-restarttype-complextype.md)                                | Указывает, что планировщик задач попытается перезапустить задачу по какой либо причине по ошибке. <br/>                                                                                                                                                                                                          |
| [**рунонлифидле**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | Логическое                                                                                           | Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.<br/>                                                                                                                                                                                                                               |
| [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | Логическое                                                                                           | Указывает, что планировщик задач будет выполнять задачу только при доступности сети.<br/>                                                                                                                                                                                                                    |
| [**стартвхенаваилабле**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | Логическое                                                                                           | Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.<br/>                                                                                                                                                                                                    |
| [**стопифгоингонбаттериес**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | Логическое                                                                                           | Указывает, что задача будет остановлена, если компьютер переключается на питание от аккумулятора. <br/>                                                                                                                                                                                                                      |
| [**усеунифиедсчедулинженгине**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | Логическое                                                                                           | Указывает, что задача выполняется с помощью единого механизма планирования.<br/>                                                                                                                                                                                                                                   |
| [**вакеторун**](taskschedulerschema-waketorun-settingstype-element.md)                                             | Логическое                                                                                           | Указывает, что планировщик задач будет выводить компьютер из спящего режима перед выполнением задачи.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





