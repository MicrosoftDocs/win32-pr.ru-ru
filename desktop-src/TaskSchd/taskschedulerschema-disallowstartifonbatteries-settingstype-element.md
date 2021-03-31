---
title: Дисалловстартифонбаттериес (Сеттингстипе), элемент
description: Указывает, что задача не будет запущена, если компьютер работает от батарей.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- планировщик задач элемента Дисалловстартифонбаттериес
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803982"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Дисалловстартифонбаттериес (Сеттингстипе), элемент

Указывает, что задача не будет запущена, если компьютер работает от батарей.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

Элемент **дисалловстартифонбаттериес** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Значение по умолчанию для этого элемента — true.

Для разработки сценариев эти сведения доступны через свойство [**тасксеттингс. дисалловстартифонбаттериес**](tasksettings-disallowstartifonbatteries.md) .

Для разработки на C++ эта информация доступна через свойство [**итасксеттингс::D исалловстартифонбаттериес**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который не разрешает выполнение задачи, если компьютер работает под управлением батарей.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
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

 

 





