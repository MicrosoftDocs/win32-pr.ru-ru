---
title: Идлесеттингс (Сеттингстипе), элемент
description: Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- планировщик задач элемента Идлесеттингс
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0a4c3fc978c93d13be8faa62012d3928d47da5b5a214ce50f5506992f1fc8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991223"
---
# <a name="idlesettings-settingstype-element"></a>Идлесеттингс (Сеттингстипе), элемент

Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя. Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

Элемент **идлесеттингс** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент

| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |

## <a name="child-elements"></a>Дочерние элементы

> [!NOTE]
> Параметры *Duration* и *ваиттимеаут* являются устаревшими. Они по-прежнему находятся в пользовательском интерфейсе планировщик задач, а методы интерфейса по-прежнему могут возвращать допустимые значения, но они больше не используются.

| Элемент                                                                                  | Тип     | Описание                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**рестартонидле**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | Логическое  | Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.<br/>       |
| [**стопонидлинд**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | Логическое  | Указывает, что планировщик задач будет прекращать выполнение задачи, если условие простоя заканчивается до завершения задачи.<br/> |
| **Устарело**: [ **Продолжительность**](taskschedulerschema-duration-idlesettingstype-element.md)                | длительность | Указывает, как долго компьютер должен находиться в состоянии простоя перед выполнением задачи.<br/>                              |
| Не **рекомендуется**: [ **ваиттимеаут**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | длительность | Указывает период времени, в течение которого планировщик задач будет ожидать наступления условия простоя.<br/>                |

## <a name="remarks"></a>Remarks

Для разработки скриптов параметры простоя указываются с помощью свойства [**тасксеттингс. идлесеттингс**](tasksettings-idlesettings.md) .

Для разработки на C++ параметры простоя указываются с помощью свойства [**итасксеттингс:: идлесеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, позволяющий планировщик задач ожидать 24 часа в течение неактивного состояния, а затем допускает запуск задачи только через 10 минут {Идледуратион).

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |

## <a name="see-also"></a>См. также

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)

[Планировщик заданий](task-scheduler-start-page.md)
