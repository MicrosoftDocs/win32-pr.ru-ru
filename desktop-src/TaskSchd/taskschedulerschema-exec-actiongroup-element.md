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
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674557"
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
| [**Аргументы**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Задает аргументы, связанные с операцией командной строки.<br/>                               |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | **string** | Указывает исполняемый файл или документ для запуска.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | строка     | Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя | Тип       | Описание                                                    |
|------|------------|----------------------------------------------------------------|
| идентификатор   | **string** | Идентификатор действия, выполняемого задачей.<br/> |



## <a name="remarks"></a>Комментарии

Перечисленные выше дочерние элементы определяются сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .

Для разработки скриптов действие выполнения определяется объектом [**ексекактион**](execaction.md) .

Для разработки на C++ действие выполнения определяется интерфейсом [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .

Если переменные среды используются в [**команде**](taskschedulerschema-command-exectype-element.md), [**аргументах**](taskschedulerschema-arguments-exectype-element.md)или элементах [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , значения переменных среды кэшируются и используются при запуске Taskeng.exe (обработчик задач). Изменения переменных среды, происходящих после запуска обработчика задач, не будут использоваться обработчиком задач.

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей триггер события, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





