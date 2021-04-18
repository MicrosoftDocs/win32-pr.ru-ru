---
title: Стопифгоингонбаттериес (Сеттингстипе), элемент
description: Указывает, что задача будет остановлена при переходе компьютера на питание.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- планировщик задач элемента Стопифгоингонбаттериес
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681844"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Стопифгоингонбаттериес (Сеттингстипе), элемент

Указывает, что задача будет остановлена при переходе компьютера на питание.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

Элемент **стопифгоингонбаттериес** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Значение по умолчанию для этого элемента — false. Обратите внимание, что значение по умолчанию изменилось по сравнению с предыдущими версиями планировщик задач.

Для разработки сценариев этот параметр указывается с помощью свойства [**тасксеттингс. стопифгоингонбаттериес**](tasksettings-stopifgoingonbatteries.md) .

Для разработки на C++ этот параметр указывается с помощью свойства [**итасксеттингс:: стопифгоингонбаттериес**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который разрешает жесткое завершение задачи.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





