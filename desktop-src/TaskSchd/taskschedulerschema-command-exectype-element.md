---
title: Элемент Command (Ексектипе)
description: Указывает исполняемый файл или документ для запуска.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Элемент Command планировщик задач
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415952"
---
# <a name="command-exectype-element"></a>Элемент Command (Ексектипе)

Указывает исполняемый файл или документ для запуска.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

Элемент **Command** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                      | Унаследован от                                                 | Описание                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**ексектипе**](taskschedulerschema-exectype-complextype.md) | Указывает действие, выполняющее операцию командной строки.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в описании [**свойства arguments объекта иексекактион**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Сведения о разработке скриптов см. в разделе [**ексекактион. Arguments**](execaction-arguments.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей исполняемое действие, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





