---
title: Мултиплеинстанцесполици (Сеттингстипе), элемент
description: Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- планировщик задач элемента Мултиплеинстанцесполици
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672733"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Мултиплеинстанцесполици (Сеттингстипе), элемент

Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

Элемент **мултиплеинстанцесполици** определяется простым типом [**мултиплеинстанцесполицитипе**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство мултиплеинстанцес объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. мултиплеинстанцес**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Ограниченные значения

Этот элемент ограничен следующими значениями.

-   Parallel: запускает новый экземпляр во время работы существующего экземпляра.
-   Queue: запускает новый экземпляр Task после завершения всех остальных экземпляров задачи.
-   Игноренев: по умолчанию. Не запускает новый экземпляр, если запущен существующий экземпляр задачи.
-   Стопексистинг: останавливает существующий экземпляр задачи перед запуском нового экземпляра.

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, позволяющий параллельно выполнять несколько экземпляров задачи.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





