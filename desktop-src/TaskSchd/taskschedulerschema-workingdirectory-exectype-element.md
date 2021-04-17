---
title: WorkingDirectory (Ексектипе), элемент
description: Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- планировщик задач элемента WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682126"
---
# <a name="workingdirectory-exectype-element"></a>WorkingDirectory (Ексектипе), элемент

Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

Элемент **WorkingDirectory** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                      | Унаследован от                                                 | Описание                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**ексектипе**](taskschedulerschema-exectype-complextype.md) | Указывает действие, выполняющее операцию командной строки.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки скриптов рабочий каталог указывается свойством [**ексекактион. WorkingDirectory**](execaction-workingdirectory.md) .

Для разработки на C++ рабочий каталог определяется свойством [**иексекактион:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

## <a name="examples"></a>Примеры

В следующем коде XML определяется действие выполнения.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



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

 

 





