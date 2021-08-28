---
title: Exec (actionGroup), элемент
description: Указывает действие, выполняющее операцию командной строки.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Элемент Exec планировщик задач
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 709cded1238654fffcf8ce75e5cba85c6139eb6264592e99684462e0a9cb2661
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072494"
---
# <a name="exec-actiongroup-element"></a>Exec (actionGroup), элемент

Указывает действие, выполняющее операцию командной строки.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

Элемент **exec** определяется [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                         | Унаследован от                                                       | Описание                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Действия**](taskschedulerschema-actions-tasktype-element.md) | [**актионстипе**](taskschedulerschema-actionstype-complextype.md) | Содержит действия, выполняемые задачей.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип       | Описание                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Аргументы**](taskschedulerschema-arguments-exectype-element.md)               | **строка** | Задает аргументы, связанные с операцией командной строки.<br/>                               |
| [**Команда**](taskschedulerschema-command-exectype-element.md)                   | **строка** | Указывает исполняемый файл или документ для запуска.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | строка     | Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя | Тип       | Описание                                                    |
|------|------------|----------------------------------------------------------------|
| идентификатор   | **строка** | Идентификатор действия, выполняемого задачей.<br/> |



## <a name="remarks"></a>Remarks

Перечисленные выше дочерние элементы определяются сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .

Для разработки скриптов действие выполнения определяется объектом [**ексекактион**](execaction.md) .

Для разработки на C++ действие выполнения определяется интерфейсом [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .

Если переменные среды используются в [**команде**](taskschedulerschema-command-exectype-element.md), [**аргументах**](taskschedulerschema-arguments-exectype-element.md)или элементах [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , значения переменных среды кэшируются и используются при запуске Taskeng.exe (обработчик задач). Изменения переменных среды, происходящих после запуска обработчика задач, не будут использоваться обработчиком задач.

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей триггер события, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





