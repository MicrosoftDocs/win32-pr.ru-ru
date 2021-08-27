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
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072454"
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



## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





