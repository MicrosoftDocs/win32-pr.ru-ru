---
title: Алловхардтерминате (Сеттингстипе), элемент
description: Указывает, что задачу можно завершить с помощью Терминатепроцесс.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Элемент Алловхардтерминате (Сеттингстипе) планировщик задач
- планировщик задач элемента Алловхардтерминате
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681815"
---
# <a name="allowhardterminate-settingstype-element"></a>Алловхардтерминате (Сеттингстипе), элемент

Указывает, что задачу можно завершить с помощью Терминатепроцесс.

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

Элемент **алловхардтерминате** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                 | Описание                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на C++ см. в описании [**Свойства алловхардтерминате объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. алловхардтерминате**](tasksettings-allowhardterminate.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, которая допускает жесткое завершение работы, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





